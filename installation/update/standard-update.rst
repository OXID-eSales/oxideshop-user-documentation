Standard Update
===============

Update the OXID eShop.

With the following steps, update the Compilation from an existing version 6.3.x to version 6.4.1, for example.

If you have an Oxid eShop Enterprise Edition to maintain multiple subshops, perform the update for each subshop.

.. ATTENTION::
   **Loss of data**

   Perform the update in a test environment (a copy of your current shop).

   Make sure to backup the shop data and database.

   Before the update, deactivate all modules and check whether the shop is working.

   After the update, activate all modules and test the shop again. In particular, check the ordering process as well as payment and shipping methods.

.. |schritt| image:: ../../media/icons/schritt.jpg
              :class: no-shadow

|schritt| Specifying the target version of the update
-----------------------------------------------------

To perform the update, go to the shop's main directory. In the :file:`composer.json` file, which is in the shop's main directory, update the metapackage version.

1. Go to the shop's main directory (`/var/www/oxideshop/`, in our example).

   .. code:: bash

      cd /var/www/oxideshop

2. In the following sample command, adjust the edition type and the metapackage version number corresponding to the new shop version:

   .. code:: bash

      composer require --no-update oxid-esales/oxideshop-metapackage-<eition type: ce, pe or ee>:v<version number>

3. Execute the command, in our example for an update from a Community Edition 6.3.1 to 6.4.1:

   .. code:: bash

      composer require --no-update oxid-esales/oxideshop-metapackage-ce:v6.4.1



|schritt| Updating dependencies
-------------------------------

Update the required libraries.

To do so, execute the following Composer command.

Optional: If you don't require the development-related files, use the  :command:`--no-dev` parameter.

.. code:: bash

   composer update --no-plugins --no-scripts --no-dev


|schritt| Obtaining the new compilation
---------------------------------------

Execute the scripts to obtain the new compilation.

For the shop files, themes, and modules, confirm the update overwrites existing files.


.. code:: bash

   composer update --no-dev


|schritt| Deleting temporary files
----------------------------------

To ensure the cached elements do not contain any incompatibilities, clear the :file:`/tmp` directory.

.. code:: bash

   rm -rf source/tmp/*

|schritt| Migrating the database
--------------------------------

Migrate the database.

.. code:: bash

   vendor/bin/oe-eshop-db_migrate migrations:migrate

If there are no changes that require a migration, the following message appears: ``PHP Warning:  require_once(migrate.php): failed to open stream: No such file or directory in /var/www/oxides``.

|schritt| If required: Generating database views
------------------------------------------------

Depending on the changes and your shop edition type, it's possible that you see the maintenance mode in the shop.

If the shop is in maintenance mode after the update, generate the database views again. To do so, execute the following command.

.. code:: bash

   vendor/bin/oe-eshop-db_views_generate


The update is finished. When you access the shop as an administrator, the new version is displayed in the upper right corner.


.. Intern: oxbaix, Status: transL