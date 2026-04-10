Update from 7.x to 7.5
======================

This document describes the update procedure from any previous minor version of the OXID eShop 7 series, 7.x, to the minor release 7.5. This update can involve additional steps due to the possibility of choosing one out of three versions of the preinstalled **Content & Media Bundle**.

Preparation
-----------

#. Verify you are at least on any 7.x version older than 7.5.
#. Verify what OXID eShop edition you are running (Enterprise, Professional or Community).
#. Do a backup of your database.
#. Do a backup of your filesystem.
#. Decide what Content & Media Bundle you want to use after the update.

    OXID eShop 7.5 has the new **Content & Media Bundle 10** preinstalled. This includes the following extensions:

        * Media Library 5
        * WYSIWYG Editor 7
        * Visual CMS 10 (Enterprise and Professional Edition only)

    Alternatively, you can stay on the **Content & Media Bundle 9**:

        * Media Library 4.1.0
        * WYSIWYG Editor 6.0.2
        * Visual CMS 9.2.0 (Enterprise and Professional Edition only)

    Or stay on the **Content & Media Bundle 8**:

        * Media Library 3.0.0
        * WYSIWYG Editor 5.0.1
        * Visual CMS 8.0.2 (Enterprise and Professional Edition only)

    To decide which bundle version to use, please refer to our :doc:`Release Notes <../releases/oxid-eshop-750>`.

Procedure
---------

Depending on your edition and decision about the **Content & Media Bundle**, the update procedure consists of up to five steps:

* :ref:`Step 1: Preconfigure the Content & Media Bundle <step-1-preconfigure-the-content-and-media-bundle>`
* :ref:`Step 2: Set the Target Version <step-2-set-the-target-version>`
* :ref:`Step 3: Run the Update Process <step-3-run-the-update-process>`
* :ref:`Step 4: Adjust the Rewrite Conditions <step-4-adjust-the-rewrite-conditions>`
* :ref:`Step 5: Migrate Content and Media <step-5-migrate-content-and-media>`

.. _step-1-preconfigure-the-content-and-media-bundle:

Step 1: Preconfigure the Content & Media Bundle
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you decide for the new **Content & Media Bundle 10**, you can skip this step and continue with :ref:`Step 2: Set the Target Version <step-2-set-the-target-version>`.

**Stay on Content & Media Bundle 9**

If you have an **OXID eShop Enterprise or Professional Edition**, run the following three commands:

.. code:: shell

    composer require oxid-esales/media-library-module:^4.0 --no-update
    composer require ddoe/wysiwyg-editor-module:^6.0 --no-update
    composer require ddoe/visualcms-module:^9.0 --no-update

If you have an **OXID eShop Community Edition**, run the following two commands:

.. code:: shell

    composer require oxid-esales/media-library-module:^4.0 --no-update
    composer require ddoe/wysiwyg-editor-module:^6.0 --no-update

**Stay on Content & Media Bundle 8**

If you have an **OXID eShop Enterprise or Professional Edition**, run the following three commands:

.. code:: shell

    composer require oxid-esales/media-library-module:^3.0 --no-update
    composer require ddoe/wysiwyg-editor-module:^5.0 --no-update
    composer require ddoe/visualcms-module:^8.0 --no-update

If you have an **OXID eShop Community Edition**, run the following two commands:

.. code:: shell

    composer require oxid-esales/media-library-module:^3.0 --no-update
    composer require ddoe/wysiwyg-editor-module:^5.0 --no-update

.. _step-2-set-the-target-version:

Step 2: Set the Target Version
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you have **OXID eShop Enterprise Edition**, run the following command:

.. code:: shell

    composer require oxid-esales/oxideshop-metapackage-ee:^7.5 --no-update

If you have **OXID eShop Professional Edition**, run the following command:

.. code:: shell

    composer require oxid-esales/oxideshop-metapackage-pe:^7.5 --no-update

If you have **OXID eShop Community Edition**, run the following command:

.. code:: shell

    composer require oxid-esales/oxideshop-metapackage-ce:^7.5 --no-update

.. hint::
   The constraint ``^7.5`` automatically installs the latest
   available patch version. If you need a specific patch
   version, specify it explicitly, e.g., ``v7.5.0``. We
   recommend using the latest patch version.

.. _step-3-run-the-update-process:

Step 3: Run the Update Process
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In any case, run the following commands to update your OXID eShop:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate

.. _step-4-adjust-the-rewrite-conditions:

Step 4: Adjust the Rewrite Conditions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. note::
   If you are already updating from version 7.4.x or higher,
   you have likely already completed this step. Still, verify
   that the change is present in your **.htaccess** file.

A rewrite condition in OXID eShop versions before 7.4 restricts the use of specific brand names. The OXID eShop's update behavior does not replace your **.htaccess** file with a new one, since this file is typically customized. Therefore, you must modify the file manually.

#. Open the file **source/.htaccess**.
#. Search for the affected rewrite condition:

    .. code::

        RewriteCond %{REQUEST_URI} !(\/admin\/|\/Core\/|\/Application\/|\/export\/|\/modules\/|\/out\/|\/Setup\/|\/tmp\/|\/views\/)

#. Replace the first instance with the following condition:

    .. code::

        RewriteCond %{REQUEST_URI} !^(\/admin\/|\/Core\/|\/Application\/|\/export\/|\/modules\/|\/out\/|\/Setup\/|\/tmp\/|\/views\/)

#. Repeat this for the second affected instance.
#. Save the file.

.. _step-5-migrate-content-and-media:

Step 5: Migrate Content and Media
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you decided to keep the **Content & Media Bundle 8** or **9**, you can skip this step. Your update is finished.

If you decided for the new **Content & Media Bundle 10** and you are running an **OXID eShop Enterprise or Professional Edition**, please see the section `Update <https://docs.oxid-esales.com/modules/vcms/en/10.0/update.html>`__ in our **Content & Media Bundle** documentation to finish your update.

If you decided for the new **Content & Media Bundle 10** and you are running an **OXID eShop Community Edition**, please see the section `Introduction of Media IDs <https://docs.oxid-esales.com/modules/vcms/en/10.0/update.html#introduction-of-media-ids>`__ in our **Content & Media Bundle** documentation to finish your update.

.. todo:: Verify VCMS 10.0 documentation links once published
