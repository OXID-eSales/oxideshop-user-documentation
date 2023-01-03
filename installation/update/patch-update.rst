Installing a patch update
=========================

Perform a patch update of your OXID eShop if required.

For example, use the following steps to update the compilation from an existing version 6.4.x to version 6.4.2.

.. include:: /_static/reuse/note_dataloss.rst


|procedure|

1. Upgrade Composer to version 2.2.x.

   .. attention::

      Composer 2.3.x is not supported.

      If you have Composer 2.3.x, install Composer 2.2.x as follows, for example:

      .. code:: bash

         sudo composer selfupdate 2.2.12

#. Change to the main store directory (in our example `/var/www/oxideshop/`).

   .. code:: bash

      cd /var/www/oxideshop/

#. In the :file:`composer.json` file located in the main store directory, update the metapackage version.
   |br|
   To do this, do the following:

   a. In the following sample command, adjust the version number of the metapackage according to the new store edition:

      .. code:: bash

         composer require --no-update oxid-esales/oxideshop-metapackage-<edition type: ce, pe, or ee>:v<version number>.

   b. Run the command, in our example for updating a community edition 6.4.1 to 6.4.2:

      .. code:: bash

         composer require --no-update oxid-esales/oxideshop-metapackage-ce:v6.4.2

#. Update the required libraries.
   |br|
   To do this, run the following composer command.
   |br|
   Optional: If you don't need the development-related files, use the :command:`--no-dev` parameter.

   .. code:: bash

      composer update --no-plugins --no-scripts --no-dev

#. Download the new compilation.
   |br|
   To do this, run the following composer command.

   .. code:: bash

      composer update --no-dev

#. For store files, themes and modules, confirm that the update overwrites existing files.

#. To ensure that the cached items do not contain incompatibilities, empty the :file:`/tmp` directory.

   .. code:: bash

      rm -rf source/tmp/*

#. Migrate the database.

   .. code:: bash

      vendor/bin/oe-eshop-db_migrate migrations:migrate

#. Regenerate the database views.
   |br|
   Background: Depending on the changes and store edition, the store may go into maintenance mode after the update.
   |br|
   To prevent this, regenerate the database views with the following command:

   .. code:: bash

      vendor/bin/oe-eshop-db_views_generate

|result|

The update is finished. If you open the store as administrator, the new version is displayed in the upper right corner.


.. Intern: oxbajy, Status:
