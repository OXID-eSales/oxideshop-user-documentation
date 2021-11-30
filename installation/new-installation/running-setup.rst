Running setup
=============

To make your OXID eShop ready, perform the web-based setup..


.. |schritt| image:: ../../media/icons/schritt.jpg
               :class: no-shadow

|schritt| Starting the setup
----------------------------

Ensure that confuguration parameters can be written during the setup, and start the setup.

1. Open a Shell and go to the shop directory.

   .. code:: bash

      cd /var/www/oxideshop/source

2. Ensure the following files are not read-only:

   * :file:`.htaccess`
   * :file:`config.inc.php`

3. Open a browser and open the shop under ``www.myshopurl.de/setup``.

   Replace ``www.myshopurl.de`` with the OXID eShop URL.

.. todo: #tbd: #HR: prüfen: Wo habe ich bei der Installation die IP-Adresse festgelegt?

   The setup starts.


|schritt| Requirements
----------------------

The following icons indicate whether the system requirements have been met:

.. |install-pass| image:: ../../media/icons/install-pass.png
               :class: no-shadow
.. |install-pmin| image:: ../../media/icons/install-pmin.png
               :class: no-shadow
.. |install-fail| image:: ../../media/icons/install-fail.png
               :class: no-shadow
.. |install-null| image:: ../../media/icons/install-null.png
               :class: no-shadow

* |install-pass| The requirement has been met.
* |install-pmin| The requirement hasn’t been met or has been met only partially. OXID eShop still works and can be installed.
* |install-fail| The requirement hasn’t been met. OXID eShop doesn’t work without meeting this requirement and can’t be installed.
* |install-null| The requirement couldn’t be verified.

1. Select the language for the installation.
2. To install OXID eShop and ensure uninterrupted operation, ensure the system requirements are met.
   In case of any configuration issues, contact your OXID Hosting Partner or Internet Service Provider (ISP).
3. Once all system requirements are met (there are no red icons), choose :guilabel:`Proceed with setup`.

|schritt| Welcome
-----------------

1. Specify main shipping country and the shop’s language.
   You can always add other countries and/or languages later on.
2. Recommended: Check the box to have the shop regularly checked for updates.
3. Optional: When installing the Community Edition, help improve product quality by confirming the connection to the OXID servers.
4. Choose :guilabel:`Start installation`.

|schritt| License terms
-----------------------

Check the license terms and confirm them.

|schritt| Database
------------------

Create a database or integrate an existing one.

:guilabel:`Database server hostname or IP address`

   You have the following options:

   * If your database and the webserver share the same server, use the default value `localhost`. This is the standard procedure for most shops.
   * if you have an outsourced database, enter the hostname or the IP address of your database server. If required, enter the port after the hostname and a colon (hostname:port).

:guilabel:`Database Name`

   You have the following options:

   * Enter the name of your outsourced database.
   * If you don't have a database yet, enter a name for a database to be created during the setup.


:guilabel:`Database username` and :guilabel:`Database password`

   Enter the login data for the database. Make sure to keep this login data in a safe place.

:guilabel:`Demodata`

   Decide whether you want to install the shop preconfigured with sample products.

   We recommend demo data if you want to use a test installation to familiarise yourself with the shop first.

   You can always delete the demo data later on if you want to add your own products to the shop.

Choose :guilabel:`Create database now`.

   If you have integrated an existing database, a message appears that the database is being overwritten and the the tables and data required are being saved.

:guilabel:`Database server hostname or IP address`

   You can leave localhost as the default value if the database and the web server are located on the same server.

   If the database is outsourced, the hostname or IP address of the database server will need to be specified. If a port is required, it should be specified after the hostname and a colon (hostname:port).

:guilabel:`Database name`

   Enter the name of the outsourced database or the name of the database to be ceated.
   * Tragen Sie den Namen Ihrer ausgelagerten Datenbank ein.
   * Wenn Sie noch keine Datenbank haben, dann tragen Sie einen Namen für eine Datenbank ein, die das System beim Setup erstellt.

:guilabel:`Database username` and :guilabel:`Database password`

   Enter the login data for the database.

:guilabel:`Demodata`
   You can decide whether you want to install the shop preconfigured with sample products. Demo data is recommended if you want to use a test installation to familiarise yourself with the shop first. You can always delete the demo data later on if you want to add your own products to the shop.

   Click on :guilabel:`Create database now`. Certain configurations allow you to create the database directly so that you don’t have to create it manually beforehand. Since your database already exists, all required tables and data will now be stored in this database.

|schritt| Directories & login
-----------------------------

If required, adjust the adjust the directory settings and define the login data for the shop’s Admin panel.

Note down the following settings and make sure to keep this data in a safe place.

The directories are automatically detected and suggested during setup. In most cases, you don’t need to change anything.

:guilabel:`Shop URL`
   Shows the URL under which your OXID eShop will be accessible.

:guilabel:`Directory for OXID eShop`
   Generates the internal path to the shop on the server.
   Adjust the path if you have multiple shops, for example.
   You will need this path in the last step of the setup.

:guilabel:`Directory for temporary data`
   Names the directory where the shop's temporary files, e.g. for Smarty or SEO cache, are stored.
   Background: Some module will ask you to clear temporary data manually from time to time.

:guilabel:`Administrator E-Mail` und :guilabel:`Administrator Passwort`

   Enter your administrator e-mail and passwort.
   With this login data you will log in to the Admin panel after the setup has been completed.


|schritt| License
-----------------

If you have an Enterprise or Professional Edition, enter the license key you have received when purchasing OXID eShop.

Find the license key on the receipt sent to you by e-mail.

Choose :guilabel:`Save license key`.



|schritt| Finish
----------------

For reasons of security, set the :file:`config.inc.php` file into ``read-only`` mode. Test the shop the shop.

1. Open the shell and go to the shop directory (by default, `/var/www/ocideshop/source/`).
2. Execute the following command:

   .. code:: bash

      chmod 0444 config.inc.php

   Setting :file:`config.inc.php` file to ``read-only`` ensures that the production system cannot be fatally compromised by changes of, for example, the
   database name or the shop URL.

3. To test the shop, open it as a customer and as an adminstrator:

* The link :guilabel:`Zum Shop` leads you to the shop's start page.
* The link :guilabel:`Zur Shop Administration` leads you to the the Admin panel.


.. Intern: oxbaaf, Status: