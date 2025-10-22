Update from 7.x to 7.4
======================

This document describes the update procedure from any previous minor version of the OXID eShop 7 series, 7.x, to the minor release 7.4. This update can involve additional steps due to the possibility of choosing one out of two versions of the preinstalled **Content & Media Bundle**.

Preparation
-----------

#. Verify you are at least on any 7.x version older than 7.4.
#. Verify what OXID eShop edition you are running (Enterprise, Professional or Community).
#. Do a backup of your database.
#. Do a backup of your filesystem.
#. Decide what Content & Media Bundle you want to use after the update.

    OXID eShop 7.4 has the new **Content & Media Bundle 9** preinstalled. This includes the following extensions:

        * Media Library 4
        * WYSIWYG Editor 6
        * Visual CMS 9 (Enterprise and Professional Edition only)

    Using the new bundle, requires migration of existing content. If you do not want to use the updated extensions, you can preconfigure your update to stay on the last major edition of the **Content & Media Bundle**. This includes the following extensions:

        * Media Library 3.0.0
        * WYSIWYG Editor 5.0.1
        * Visual CMS 8.0.2 (Enterprise and Professional Edition only)

    To decide which bundle version to use, please refer to our :doc:`Release Notes <../releases/oxid-eshop-740>`.

Procedure
---------

Depending on your edition and decision about the **Content & Media Bundle**, the update procedure consists of up to four steps:

* :ref:`Step 1: Preconfigure the Content & Media Bundle <step-1-preconfigure-the-content-and-media-bundle>`
* :ref:`Step 2: Set the Target Version <step-2-set-the-target-version>`
* :ref:`Step 3: Run the Update Process <step-3-run-the-update-process>`
* :ref:`Step 4: Migrate Content and Media <step-4-migrate-content-and-media>`

.. _step-1-preconfigure-the-content-and-media-bundle:

Step 1: Preconfigure the Content & Media Bundle
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you decide for the new **Content & Media Bundle 9**, you can skip this step and continue with :ref:`Step 2: Set the Target Version <step-2-set-the-target-version>`.

If you decide to keep the **Content & Media Bundle 8** and you have an **OXID eShop Enterprise or Professional Edition**, run the following three commands:

.. code:: shell

   composer require oxid-esales/media-library-module:^3.0 --no-update
   composer require ddoe/wysiwyg-editor-module:^5.0 --no-update
   composer require ddoe/visualcms-module:^8.0 --no-update

If you decide to keep the **Content & Media Bundle 8** and you have an **OXID eShop Community Edition**, run the following two commands:

.. code:: shell

   composer require oxid-esales/media-library-module:^3.0 --no-update
   composer require ddoe/wysiwyg-editor-module:^5.0 --no-update

.. _step-2-set-the-target-version:

Step 2: Set the Target Version
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you have **OXID eShop Enterprise Edition**, run the following command:

.. code:: shell

   composer require oxid-esales/oxideshop-metapackage-ee:v7.4.0 --no-update

If you have **OXID eShop Professional Edition**, run the following command:

.. code:: shell

   composer require oxid-esales/oxideshop-metapackage-pe:v7.4.0 --no-update

If you have **OXID eShop Community Edition**, run the following command:

.. code:: shell

   composer require oxid-esales/oxideshop-metapackage-ce:v7.4.0 --no-update

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

.. _step-4-migrate-content-and-media:

Step 4: Migrate Content and Media
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you decided to keep the **Content & Media Bundle 8**, you can skip this step. Your Update is finished.

If you decided for the new **Content & Media Bundle 9** and you are running an **OXID eShop Enterprise or Professional Edition**, please see the section `Update <https://github.com/OXID-eSales/vcms-documentation/blob/9.0-en/update.rst#update>`__ in our **Content & Media Bundle** documentation to finish your update.

If you decided for the new **Content & Media Bundle 9** and you are running an **OXID eShop Community Edition**, please see the section `Introduction of Media IDs <https://github.com/OXID-eSales/vcms-documentation/blob/9.0-en/update.rst#introduction-of-media-ids>`__ in our **Content & Media Bundle** documentation to finish your update.
