INSTALL THE SHOP VIA COMMAND LINE
=================================

This section tells you how to install OXID eShop 7 via command line, which is a tools in addition to the graphical way. The installation is no longer based on installation packages. The files required for the shop are provided by Composer, a dependency manager for PHP.

We have three commands to install and prepare the shop:
    - :ref:`Install the shop<install-the-shop>`
    - :ref:`Install demo data<install-demo-data>`
    - :ref:`Add admin user<add-admin-user>`

.. important::

    After installing the shop via command line, you should add an admin user via a separate command which is provided for this purpose and will be explained in this page.
    But the most important thing is, we should run it as the last command. First install the shop, then if we want we can install the demodata and at the end we should add shop admin user.

SERVER AND SYSTEM REQUIREMENTS
------------------------------

Server, shared hosting, managed server, server farm with load balancing and database cluster, Linux, web server, Apache 2.2 + 2.4, MySQL 5.7 + 8.0, MariaDB 10.4, PHP from 7.3 to 7.4, Composer, OpenSSL

Read more: https://docs.oxid-esales.com/eshop/en/6.2/installation/new-installation/server-and-system-requirements.html


PREPARING FOR INSTALLATION
--------------------------

Installing Composer, providing shop files, configuring Apache, customising file and directory permissions, creating database

Read more: https://docs.oxid-esales.com/eshop/en/6.2/installation/new-installation/preparing-for-installation.html

.. _install-the-shop:

RUNNING SETUP COMMAND
---------------------

Now you can run the setup-command via command line to install the shop.

How to run the command:

.. code::

    vendor/bin/oe-console oe:setup:shop --db-host DB-HOST --db-port DB-PORT --db-name DB-NAME --db-user DB-USER --db-password DB-PASSWORD --shop-url SHOP-URL --shop-directory SHOP-DIRECTORY --compile-directory COMPILE-DIRECTORY [--language [LANGUAGE]]

Which:
	- <db-host> is the database host
	- <db-port> is the database port
        - <db-name> is the database name
	- <db-user> is the database username
        - <db-password> is the database password
	- <shop-url> is the complete address of shop url (It must start with http or https)
	- <shop-directory> is the source path of the shop
	- <compile-directory> is the compile directory or temp directory path
	- [<language>] (optional) you can specify your shop language by language codes like "de" or "en"


Example:

.. code::

    vendor/bin/oe-console oe:setup:shop --db-host=localhost --db-port=3306 --db-name=oxid --db-user=oxid --db-password=oxid --shop-url=http://www.oxideshop.local --shop-directory=/var/www/oxideshop/source --compile-directory=/var/www/oxideshop/source/tmp/ --language=en

.. _install-demo-data:

INSTALL DEMO DATA
=================

To have some demo data in our installed shop, you must follow the instruction below after shop installation via :ref:`command line<install-the-shop>`.

* First based on your editions (Community, Professional or Enterprise) add demodata to your project. You should do that via composer and oxideshop_demodata repositories in github. For example to add Community edition demodata, following commands must be run:

.. code::

    composer config repositories.oxid-esales/oxideshop-demodata-ce vcs https://github.com/OXID-eSales/oxideshop_demodata_ce
    composer require oxid-esales/oxideshop-demodata-ce:v6.2.4

* Then run the following command to import demodata to your database:

.. code::

    vendor/bin/oe-console oe:setup:demodata

.. important::

    It would be better to install demodata immediatly after shop installation, because if you make any changes in database, then you may lose some part of your data due to overwrittening by demodata.

.. _add-admin-user:

ADD ADMIN USER
==============

Run the following command to add admin user account with 'malladmin' rights: 

.. code::

    vendor/bin/oe-console oe:admin:create-user --admin-email ADMIN-EMAIL --admin-password ADMIN-PASSWORD

Which:
	- <admin-email> is admin username which must be a valid email
	- <admin-password> is admin password which must following your security rules

Example:

.. code::

    vendor/bin/oe-console oe:admin:create-user --admin-email=admin@gmail.com --admin-password=123456