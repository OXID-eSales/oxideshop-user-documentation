Setup via command line
======================

OXID eShop can be installed and configured with a web-based setup or via command line. This document describes the setup via command line.

Certain values are written into :file:`.htaccess` and :file:`config.inc.php` during installation. Both files are located in the main shop directory and shouldn’t be read-only for the duration of the setup.

.. |schritt| image:: ../../media/icons/schritt.jpg
              :class: no-shadow

|schritt| Creating and configuring the shop
-------------------------------------------
OXID eShop is created with the command ``oe:setup:shop`` for OXID eShop console. The following parameters are passed:

* ``--db-host=`` - Host name or IP address of the database server. Default: ``localhost`` (database and web server on the same server)
* ``--db-port=`` - Port of the database server. Default: 3306
* ``--db-name=`` - Database name
* ``--db-user=`` - Database user
* ``--db-password=`` - Password for the database user
* ``--shop-url`` - URL through which the store will be accessible
* ``--shop-directory`` - Internal path to the shop on the server
* ``--compile-directory`` - Directory for the temporary files of the shop
* ``--language`` - Language for the shop, language abbreviation according to ISO 639-1

Example: Creating and configuring the shop
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code:: bash

   bin/oe-console oe:setup:shop --db-host=localhost --db-port=3306 --db-name=CE700 --db-user=root --db-password=oxid --shop-url=http://ce700.local --shop-directory=/var/www/oxideshop/source --compile-directory=/var/www/oxideshop/source/tmp --language=de

|schritt| Installing demo data
------------------------------
To add demo data to the store, it must first be obtained via Composer from the GitHub repository corresponding to the shop edition. Then the demo data is installed using the command ``oe:setup:demodata`` for OXID eShop console.

Example
^^^^^^^

.. code:: bash

   ./vendor/bin/oe-console oe:setup:demodata

|schritt| Creating a shop administrator
---------------------------------------
The command ``oe:admin:create-user`` creates the shop administrator and uses the following parameters:

* ``--admin-email=`` - E-mail of the shop administrator, access data for the administration panel
* ``--admin-password=`` - Password of the shop administrator, access data for the administration panel

Example: Creating a shop administrator
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code:: bash

   bin/oe-console oe:admin:create-user --admin-email=max.mustermann@oxid-esales.com --admin-password=******

|schritt| Deposit license for PE/EE
-----------------------------------
OXID eShop Professional and Enterprise Edition require a valid license key for productive operation. This can be added with the ``oe:license:add`` command for OXID eShop console. The license key is passed as a parameter.

.. code:: bash

   vendor/bin/oe-console oe:license:add <license-key>

With the command ``oe:license:clear`` all license keys of a shop can be deleted.

|schritt| Installing modules
----------------------------
Modules can be installed using the ``oe:module:install`` command of the OXID eShop console. The ``oe:module:uninstall`` command removes a specified module from the shop. All information about this can be found in the developer documentation: https://docs.oxid-esales.com/developer/en/7.0-rc.1/development/modules_components_themes/module/tutorials/module_setup.html and https://docs.oxid-esales.com/developer/en/7.0-rc.1/development/modules_components_themes/module/uninstall/index.html.


.. Intern: oxbaju, Status: transL
