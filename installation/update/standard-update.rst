Standard update
===============

This document describes patch updates of OXID eShop. Follow the steps below to upgrade the compilation from an existing version 6.3.x to a newer version 6.3.x.

Updates should always be installed in a test environment, a copy of your current shop. Backup the shop files and the database before updating. Disable all modules and check whether the shop works in general. After updating, test the shop again by paying special attention to the ordering process as well as payment and shipping methods.



.. |schritt| image:: ../../media/icons/schritt.jpg
               :class: no-shadow


|schritt| Specifying the target version of the update
-----------------------------------------------------
In the file :file:`composer.json` located in the shop’s main directory, the version of the metapackage must be updated.

Example of an update for a Community Edition 6.3.0 to 6.3.3:

.. code:: bash

   composer require --no-update oxid-esales/oxideshop-metapackage-ce:v6.3.3

.. hint::

   The name of the metapackage must be adapted to the used shop edition.

|schritt| Updating dependencies
-------------------------------
Open a shell in the shop's main directory and execute the following Composer command. This will update all required libraries. Specify the :command:`--no-dev` parameter if the development-related files are not required.

.. code:: bash

   composer update --no-plugins --no-scripts --no-dev

|schritt| Obtaining new compilation
-----------------------------------
The second Composer command executes all scripts to obtain the new compilation. For shop files, themes and modules, you will need to confirm that the update will overwrite the existing files.

.. code:: bash

   composer update --no-dev

|schritt| Deleting temporary files
----------------------------------
To ensure the cached elements do not contain any incompatibilities the :file:`/tmp` directory needs to be cleared.

.. code:: bash

   rm -rf source/tmp/*

|schritt| Migrating database
-----------------------------
The third and final Composer command will migrate the database if necessary.

.. code:: bash

   vendor/bin/oe-eshop-db_migrate migrations:migrate

|schritt| Optional: Generating views
------------------------------------
Depending on changes and shop edition you might see the maintenance mode in the shop as long as the views are not generated again.

.. code:: bash

   vendor/bin/oe-eshop-db_views_generate

.. hint::

   Usually required when updating an Enterprise Edition.

This completes the updating process.


.. Intern: oxbaix, Status:
