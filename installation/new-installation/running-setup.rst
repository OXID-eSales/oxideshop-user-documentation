Running setup
=============

OXID eShop is installed and configured through the web-based setup. Open a browser and go to ``www.yourshopurl.com/setup``. Replace ``www.yourshopurl.com`` with the URL under which your OXID eShop will be accessible.

The setup will start. It consists of 6 or 7 steps. An additional step is required to enter the license key for Enterprise and Professional Edition.

Certain values are written into :file:`.htaccess` and :file:`config.inc.php` during installation. Both files are located in the main shop directory and shouldn’t be read-only for the duration of the setup.

.. |schritt| image:: ../../media/icons/schritt.jpg
               :class: no-shadow

|schritt| Requirements
----------------------
System requirements are checked in the first step of the setup process. Select the language for the installation. The display will switch to the selected language right away.

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

Make sure that all system requirements have been met in order to install OXID eShop and ensure uninterrupted operation. Please contact your OXID Hosting Partner or Internet Service Provider (ISP) in case of any configuration issues. Once all system requirements have been met (there are no red icons), click on :guilabel:`Proceed with setup`.

|schritt| Welcome
-----------------
The main shipping country and the shop’s language can be set in the second step of the setup. You can always add other countries and/or languages later on.

Check the box to have it regularly check for updates. When installing Community Edition, please also confirm the connection to the OXID servers in order to improve product quality. Click on :guilabel:`Start installation`.

|schritt| License terms
-----------------------
This setup page displays the license terms. Please familiarise yourself with the license terms for your OXID eShop. If you agree, select :guilabel:`I accept license conditions` and click :guilabel:`Continue`.

|schritt| Database
------------------
The fourth step of the setup process requires the data for the database you created.

:guilabel:`Database server hostname or IP address`
   You can leave localhost as the default value if the database and the web server are located on the same server. This is the standard procedure for most shops. If the database is outsourced, the hostname or IP address of the database server will need to be specified. If a port is required, it should be specified after the hostname and a colon (hostname:port).

:guilabel:`Database name`
   Enter the name of the database you created earlier.

:guilabel:`Database username` and :guilabel:`Database password`
   Enter the login data for the database.

:guilabel:`Demodata`
   You can decide whether you want to install the shop preconfigured with sample products. Demo data is recommended if you want to use a test installation to familiarise yourself with the shop first. You can always delete the demo data later on if you want to add your own products to the shop.

Click on :guilabel:`Create database now`. Certain configurations allow you to create the database directly so that you don’t have to create it manually beforehand. Since your database already exists, all required tables and data will now be stored in this database.

|schritt| Directories & login
-----------------------------
The next step of the setup process allows you to adjust the directory settings and define the login data for the shop’s Admin panel. The directories are automatically detected and suggested during setup. In most cases, you don’t need to change anything.

:guilabel:`Shop URL`
   Shows the URL under which your OXID eShop will be accessible.

:guilabel:`Directory for OXID eShop`
   Generates the internal path to the shop on the server.

:guilabel:`Directory for temporary data`
   Names the directory where the shop's temporary files, e.g. for Smarty or SEO cache, are stored.

You will also need to enter the administrator's e-mail address and password. You can use this data to log in to the Admin panel after the setup has been completed. Make sure to keep this login data in a safe place.

|schritt| License
-----------------
This is where shop owners with Enterprise or Professional Edition can enter the license key they received when they purchased OXID eShop. The license key can be found on the receipt sent to you by e-mail. Next, click on :guilabel:`Save license key`.

|schritt| Finish
----------------
The setup is now completed. Click on the :guilabel:`To Shop` link to get to your shop’s start page. The link :guilabel:`To admin interface` will take you directly to the Admin panel.


.. Intern: oxbaaf, Status: