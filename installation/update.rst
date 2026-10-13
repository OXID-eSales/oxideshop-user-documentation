Update from 7.x to 7.6
======================

This document describes the update procedure from any previous minor version of the OXID eShop 7 series, 7.x, to the minor release **7.6**. This update can involve additional steps due to the possibility of choosing one of three versions of the preinstalled **Content & Media Bundle**.

Preparation
-----------

#. Verify you are at least on any 7.x version older than 7.6.
#. Verify what OXID eShop edition you are running (Enterprise, Professional or Community).
#. Do a backup of your database.
#. Do a backup of your filesystem.
#. Decide which **Content & Media Bundle** you want to use after the update.

    OXID eShop 7.6 has the new **Content & Media Bundle 12** preinstalled. This includes the following extensions:

        * Media Library 6
        * WYSIWYG Editor 8
        * Visual CMS 12 (Enterprise and Professional Edition only)

    Alternatively, you can stay on the **Content & Media Bundle 11**:

        * Media Library 5.2
        * WYSIWYG Editor 7.1
        * Visual CMS 11.1 (Enterprise and Professional Edition only)

    Or stay on the **Content & Media Bundle 8**:

        * Media Library 3.0
        * WYSIWYG Editor 5.0
        * Visual CMS 8.0 (Enterprise and Professional Edition only)

    To decide which bundle version to use, please refer to our :doc:`Release Notes <../releases/oxid-eshop-760>`.

Procedure
---------

Depending on your edition and your decision about the **Content & Media Bundle**, the update procedure consists of up to five steps:

* :ref:`Step 1: Preconfigure the Content & Media Bundle <step-1-preconfigure-the-content-and-media-bundle-760>`
* :ref:`Step 2: Set the Target Version <step-2-set-the-target-version-760>`
* :ref:`Step 3: Run the Update Process <step-3-run-the-update-process-760>`
* :ref:`Step 4: Adjust the .htaccess File <step-4-adjust-the-htaccess-file-760>`
* :ref:`Step 5: Migrate Content and Media <step-5-migrate-content-and-media-760>`

.. _step-1-preconfigure-the-content-and-media-bundle-760:

Step 1: Preconfigure the Content & Media Bundle
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you decide to use the new **Content & Media Bundle 12**, you can skip this step and continue with :ref:`Step 2: Set the Target Version <step-2-set-the-target-version-760>`.

**Staying on Content & Media Bundle 11**

If you are using an **OXID eShop Enterprise or Professional Edition**, run the following three commands:

.. code:: shell

    composer require oxid-esales/media-library-module:^5.0 --no-update
    composer require ddoe/wysiwyg-editor-module:^7.0 --no-update
    composer require ddoe/visualcms-module:^11.0 --no-update

If you are using an **OXID eShop Community Edition**, run the following two commands:

.. code:: shell

    composer require oxid-esales/media-library-module:^5.0 --no-update
    composer require ddoe/wysiwyg-editor-module:^7.0 --no-update

**Staying on Content & Media Bundle 8**

If you are using an **OXID eShop Enterprise or Professional Edition**, run the following three commands:

.. code:: shell

    composer require oxid-esales/media-library-module:^3.0 --no-update
    composer require ddoe/wysiwyg-editor-module:^5.0 --no-update
    composer require ddoe/visualcms-module:^8.0 --no-update

If you are using an **OXID eShop Community Edition**, run the following two commands:

.. code:: shell

    composer require oxid-esales/media-library-module:^3.0 --no-update
    composer require ddoe/wysiwyg-editor-module:^5.0 --no-update

.. _step-2-set-the-target-version-760:

Step 2: Set the Target Version
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you are using the **OXID eShop Enterprise Edition**, run the following command:

.. code:: shell

    composer require oxid-esales/oxideshop-metapackage-ee:^7.6 --no-update

If you are using the **OXID eShop Professional Edition**, run the following command:

.. code:: shell

    composer require oxid-esales/oxideshop-metapackage-pe:^7.6 --no-update

If you are using the **OXID eShop Community Edition**, run the following command:

.. code:: shell

    composer require oxid-esales/oxideshop-metapackage-ce:^7.6 --no-update

.. hint::
   The ``^7.6`` constraint automatically installs the latest available
   patch version. If you need a specific patch version, specify it
   explicitly, e.g. ``v7.6.0``. We recommend using the latest patch
   version.

.. _step-3-run-the-update-process-760:

Step 3: Run the Update Process
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In any case, run the following commands to update your OXID eShop:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-console oe:database:migrate
    ./vendor/bin/oe-eshop-db_views_generate

.. important::
   The order matters: run ``oe-eshop-db_views_generate`` **after** ``oe:database:migrate``.
   The migration can change the database schema (for example, the Visual CMS 12 bundle adds
   tables for Dynamic Blocks) and the database views must be regenerated against the updated
   schema afterwards. Generating the views before the migration leaves them out of date.

.. _step-4-adjust-the-htaccess-file-760:

Step 4: Adjust the .htaccess File
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop update process does not replace your **.htaccess** file, because that file is typically customized for the project and its environment. You must therefore apply the following changes manually. Depending on the OXID eShop version you are updating from, up to two adjustments are relevant:

**4a) Rewrite Condition with Anchor**

A rewrite condition in older OXID eShop versions restricts the use of specific brand names. The corrected condition has been part of the shipped **.htaccess** template since 7.4 - but because your project-customized **.htaccess** file is not replaced during updates, the fix is often missing in existing shops. Verify whether the change is present, and apply it if not.

#. Open the file **source/.htaccess**.
#. Search for the affected rewrite condition:

    .. code::

        RewriteCond %{REQUEST_URI} !(\/admin\/|\/Core\/|\/Application\/|\/export\/|\/modules\/|\/out\/|\/Setup\/|\/tmp\/|\/views\/)

#. Replace the first instance with the following condition:

    .. code::

        RewriteCond %{REQUEST_URI} !^(\/admin\/|\/Core\/|\/Application\/|\/export\/|\/modules\/|\/out\/|\/Setup\/|\/tmp\/|\/views\/)

#. Repeat this for the second affected instance.
#. Save the file.

**4b) New Rules for the API Entrypoint (introduced in 7.5)**

OXID eShop 7.5 introduced a new REST API entrypoint (``api.php``). For requests to ``https://<your-shop>/api/...`` to be routed correctly to this entrypoint, and for the ``Authorization`` header (used for JWT-based authentication) to reach PHP, two additional sections are required in the **.htaccess** file. Without these rules, the API entrypoint and any features built on top of it (JWT authentication, rate limiting) will not work.

#. Open the file **source/.htaccess**.
#. Verify whether the following lines are already present inside the ``<IfModule mod_rewrite.c>`` block:

    .. code::

        RewriteCond %{HTTP:Authorization} .
        RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]

        RewriteRule ^api/(.*)$ api.php/$1 [QSA,NC,L]

#. If the lines are missing, add them as shown below. The ``Authorization`` passthrough belongs immediately after ``RewriteBase /``, the API rewrite rule immediately after the existing ``graphql`` rule:

    .. code::

        <IfModule mod_rewrite.c>
            Options +FollowSymLinks
            RewriteEngine On
            RewriteBase /

            RewriteCond %{HTTP:Authorization} .
            RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]

            RewriteRule ^graphql/?$    widget.php?cl=graphql&skipSession=1   [QSA,NC,L]

            RewriteRule ^api/(.*)$ api.php/$1 [QSA,NC,L]

            ...

#. Save the file.

.. note::
   The ``RewriteCond`` and ``RewriteRule`` lines for ``Authorization`` passthrough are needed because many Apache and FastCGI configurations do not forward the ``Authorization`` header to PHP by default. The two lines copy the header into an environment variable that PHP can read. Without them, every JWT authentication attempt fails with ``401 Unauthorized``.

.. _step-5-migrate-content-and-media-760:

Step 5: Migrate Content and Media
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you decided to keep the **Content & Media Bundle 8** or **11**, you can skip this step. Your update is complete.

If you decided to use the new **Content & Media Bundle 12** and are using an **OXID eShop Enterprise or Professional Edition**, please read the `Update <https://docs.oxid-esales.com/modules/vcms/en/12.0/update.html>`__ section in our **Visual CMS** documentation to complete your update. Note: As of **Visual CMS 12**, custom styles in CMS content are interpreted as **SCSS** instead of LESS; check existing content beforehand with ``./vendor/bin/oe-console ddoevisualcms:migrate:less-to-scss --dry-run``.

For the **OXID eShop Community Edition**, no content migration is required to switch to Bundle 12; your update is complete after Step 3.

.. COMMENTED OUT - internal note, does NOT render:
   Verify the Visual CMS 12.0 docs link (vcms/en/12.0/update.html) once the VCMS 12 docs are published.
