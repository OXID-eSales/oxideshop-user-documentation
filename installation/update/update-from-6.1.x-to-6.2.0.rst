Update from 6.1.x to 6.2.0
==========================

This document describes the update from OXID eShop 6.1.0 and higher to OXID eShop 6.2.0. It differs from a standard update mainly in that the module configurations are taken from the database.

.. |schritt| image:: ../../media/icons/schritt.jpg
              :class: no-shadow

|schritt| Updating the shop
---------------------------
1. In the file :file:`composer.json`, which is located in the main directory of the shop, version must be changed. This concerns the section "require" and "require-dev". Example for an OXID eShop Community Edition 6.2.0:

.. code:: json

   "require": {
      "oxid-esales/oxideshop-metapackage-ce": "v6.2.0"
   },
   "require-dev": {
      "oxid-esales/testing-library": "^v7.0.1",
      "incenteev/composer-parameter-handler": "^v2.0.0",
      "oxid-esales/oxideshop-ide-helper": "^v3.1.2",
      "oxid-esales/azure-theme": "^v1.4.2"
   },

You can find the values for your shop edition in the respective repository of the OXID eShop project:

* Community Edition: https://github.com/OXID-eSales/oxideshop_project/blob/b-6.2-ce/composer.json
* Professional Edition: https://github.com/OXID-eSales/oxideshop_project/blob/b-6.2-pe/composer.json
* Enterprise Edition: https://github.com/OXID-eSales/oxideshop_project/blob/b-6.2-ee/composer.json

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
In this step, settings and activation status of the modules belonging to the shop are transferred from the database to configuration files :file:`*.yml`.

1. With the following Composer commands, which are called in the main directory of the shop, you install the OXID eShop update component.

.. code:: bash

   composer require --no-update oxid-esales/oxideshop-update-component
   composer update --no-dev --no-interaction

2. A default configuration is created for all modules located in the :file:`source/modules` directory. To do this, the new OXID eShop Console is called with the following command:

.. code:: bash

   vendor/bin/oe-console oe:oxideshop-update-component:install-all-modules

3. The existing module data (module settings, class extension chains, activation status) are transferred from the database to the configuration files :file:`*.yml`.

.. code:: bash

   vendor/bin/oe-console oe:oxideshop-update-component:transfer-module-data

After this step the option `configured = true` should be in the configuration file of all previously active modules. The configuration file now also contains the module settings. They are the same as those defined for the module in the administration panel.

4. To avoid data redundancy and problems when activating modules, their status and settings are removed from the database.

.. code:: bash

   vendor/bin/oe-console oe:oxideshop-update-component:delete-module-data-from-database

5. All modules that were previously active are activated and the module settings are restored.

.. code:: bash

   vendor/bin/oe-console oe:module:apply-configuration

6. Uninstall the OXID eShop update component

.. code:: bash

   composer remove --no-update oxid-esales/oxideshop-update-component
   composer update --no-dev --no-interaction

---------------------------------------------------------------------------------------------------

|schritt| Removing old files
----------------------------
The file :file:`xd_reciever.htm` from the :file:`/source` directory is no longer needed and should be deleted.

---------------------------------------------------------------------------------------------------

Troubleshooting
---------------
Hints on possible problems with the transfer of status and settings of the modules can be found in the document `Update from 6.1.x to 6.2.0 <https://docs.oxid-esales.com/developer/en/6.2/update/#troubleshooting>`_ of the developer documentation.


.. Intern: oxbaiy, Status: transL