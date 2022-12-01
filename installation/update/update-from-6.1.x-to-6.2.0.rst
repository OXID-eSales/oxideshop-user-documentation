Update from 6.1.x to 6.2.0
==========================

This document describes the update from OXID eShop 6.1.0 and higher to OXID eShop 6.2.0. It differs from a standard update mainly in that the module configurations are taken from the database.

.. |schritt| image:: ../../media/icons/schritt.jpg
              :class: no-shadow

|schritt| Updating the shop
---------------------------
1. In the file :file:`composer.json`, which is located in the main directory of the shop, version must be changed. This concerns the section "require" and "require-dev".

**OXID eShop Community Edition 6.2.0**

.. code:: json

   "require": {
      "oxid-esales/oxideshop-metapackage-ce": "v6.2.0"
   },
   "require-dev": {
      "oxid-esales/testing-library": "^v7.1.0",
      "incenteev/composer-parameter-handler": "^v2.0",
      "oxid-esales/oxideshop-ide-helper": "^v3.1.2",
      "oxid-esales/azure-theme": "^v1.4.2"
   },

**OXID eShop Professional Edition 6.2.0**

.. code:: json

   "require": {
      "oxid-esales/oxideshop-metapackage-pe": "v6.2.0"
   },
   "require-dev": {
      "oxid-esales/testing-library": "^v7.1.0",
      "incenteev/composer-parameter-handler": "^v2.0",
      "oxid-esales/oxideshop-ide-helper": "^v3.1.2",
      "oxid-esales/azure-theme": "^v1.4.2"
   },

**OXID eShop Enterprise Edition 6.2.0**

.. code:: json

   "require": {
      "oxid-esales/oxideshop-metapackage-ee": "v6.2.0"
   },
   "require-dev": {
      "oxid-esales/testing-library": "^v7.1.0",
      "incenteev/composer-parameter-handler": "^v2.0",
      "oxid-esales/oxideshop-ide-helper": "^v3.1.2",
      "oxid-esales/azure-theme": "^v1.4.2"
   },

2. Clear the directory with the temporary files of the shop, for example by calling a shell in the main directory of the shop and entering the following command:

.. code:: bash

   rm -rf source/tmp/*

3. Execute the following Composer command in the shell to update dependencies. The :command:`--no-dev` parameter is specified when the development-related files are not needed.

.. code:: bash

   composer update --no-plugins --no-scripts --no-dev

4. Now copy the file :file:`overridablefunctions.php` from the directory :file:`/vendor` of the shop into the directory :file:`/source`.

.. code:: bash

    cp vendor/oxid-esales/oxideshop-ce/source/overridablefunctions.php source/

5. With a second Composer command all scripts are executed to get the new compilation. For shop files, themes and modules it must be confirmed that the update will overwrite existing files. If you have included your own modules with ``type": "path"`` in your :file:`composer.json` file, please answer the question for overwriting with No.

.. code:: bash

   composer update --no-dev

6. The third and last Composer command performs the migration of the database.

.. code:: bash

   vendor/bin/oe-eshop-db_migrate migrations:migrate

---------------------------------------------------------------------------------------------------

|schritt| Updating the module configurations
--------------------------------------------
In this step, settings and activation status of the modules belonging to the shop are transferred from the database to configuration files :file:`*.yaml`.

1. With the following Composer commands, which are called in the main directory of the shop, you install the OXID eShop `update component <https://github.com/OXID-eSales/oxideshop-update-component>`__.

.. code:: bash

   composer require --no-update oxid-esales/oxideshop-update-component:"^1.0"
   composer update --no-dev --no-interaction

2. Clear the directory with the temporary files of the shop, for example by calling a shell in the main directory of the shop and entering the following `console command <https://docs.oxid-esales.com/developer/en/6.2/development/tell_me_about/console.html>`__:

.. code:: bash

   rm -rf source/tmp/*
   
3. A default configuration is created for all modules located in the :file:`source/modules` directory. To do this, the new OXID eShop Console is called with the following `console command <https://docs.oxid-esales.com/developer/en/6.2/development/tell_me_about/console.html>`__:

.. code:: bash

   vendor/bin/oe-console oe:oxideshop-update-component:install-all-modules

4. The existing module data (module settings, class extension chains, activation status) are transferred from the database to the configuration files :file:`*.yaml`.

.. code:: bash

   vendor/bin/oe-console oe:oxideshop-update-component:transfer-module-data

   After this step the option `configured = true` should be in the configuration file of all previously active modules. The configuration file now also contains the module settings. They are the same as those defined for the module in the administration panel.

5. To avoid data redundancy and problems when activating modules, their status and settings are removed from the database.

.. code:: bash

   vendor/bin/oe-console oe:oxideshop-update-component:delete-module-data-from-database

6. All modules that were previously active are activated and the module settings are restored.

.. code:: bash

   vendor/bin/oe-console oe:module:apply-configuration

.. hint::

   In an Enterprise Edition environment with at least two shops and active legacy modules the command may trigger an error. The workaround is to run the `console command <https://docs.oxid-esales.com/developer/en/6.2/development/tell_me_about/console.html>`__ per individual shop by using parameter --shop-id.
   
   Example:

   .. code:: bash

    vendor/bin/oe-console oe:module:apply-configuration --shop-id=1
    vendor/bin/oe-console oe:module:apply-configuration --shop-id=2

7. Uninstall the OXID eShop update component

.. code:: bash

   composer remove --no-update oxid-esales/oxideshop-update-component
   composer update --no-dev --no-interaction

---------------------------------------------------------------------------------------------------

|schritt| Removing old files
----------------------------
The file :file:`xd_receiver.htm` from the :file:`/source` directory is no longer needed and should be deleted.

---------------------------------------------------------------------------------------------------

Troubleshooting
---------------

* **Error message: `Module directory of ModuleX could not be installed due to The variable $sMetadataVersion must be
  present in ModuleX/metadata.php and it must be a scalar.`**

  * Up to OXID eShop 6.1, modules without a metadata version in the file :file:`metadata.php` were accepted.
    OXID eShop 6.2 requires to set a
    `metadata version <https://docs.oxid-esales.com/developer/en/6.2/development/modules_components_themes/module/skeleton/metadataphp/version21.html#modules-skeleton-metadata-v21-structure>`__ in ModuleX :file:`metadata.php`.

* **Error message: `The metadata key constrains is not supported in metadata version 2.0.`**

  * Up to OXID eShop 6.1, the array keys `constraints` and `constrains` were accepted in the file :file:`metadata.php`.
    OXID eShop 6.2 only allows the key `constraints`. Please refer to
    `the metadata documentation of settings <https://docs.oxid-esales.com/developer/en/6.2/development/modules_components_themes/module/skeleton/metadataphp/amodule/settings.html>`__.

* **The extension chain in the OXID eShop admin in** :menuselection:`Extension -->  Modules --> Installed Shop Modules` **is
  partly highlighted red and crossed out.**

  * This must not be an error. Up to OXID eShop 6.1, only extensions of active modules were shown. OXID eShop 6.2 shows
    extensions of all installed modules (active and inactive). If a module is inactive, the extensions of this module
    are highlighted red and crossed out. This new behavior means, you can configure the extension chain of modules which
    are not activated yet.

.. Intern: oxbaiy, Status: transL
