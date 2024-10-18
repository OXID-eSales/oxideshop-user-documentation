Server and system requirements
==============================

You can run OXID eShop on different server systems.

The choice of a suitable hosting package depends, for example, on the number of products, the expected number of visitors in the shop, and the number of orders.

You have the following options:

* Use a shared hosting system for a small shop with a few hundred products, a few visitors per month, and a manageable order volume.
* Use a managed server system for larger shops.
* As the load increases, a server farm with load balancing and a database cluster is recommended.

For advice and support in selecting the right system, contact our `OXID Hosting Partners <https://www.oxid-esales.com/oxid-welt/partner/partner-finden/>`_. They provide solutions specifically tailored to OXID eShop.

----------------------------------------------------------------------------------------

The following system requirements must be met to operate OXID eShop version 6.

Webserver
---------

* Apache version 2.2 or 2.4 (on Linux)
* 500 MB of free webspace for Community and Professional Edition
* 750 MB of free webspace for Enterprise Edition
* Installed *mod_rewrite* extension

.. hint::

   After finishing the installation, you go to the web-based shop setup.

   Before you can start the setup, the system checks whether the system requirements are met.

   Under :guilabel:`Server Configuration`, the *Apache mod_rewrite Module* bay be marked as defective, even with the *mod_rewrite* extension installed.

   Often, one of the reasons for this is the setting for *AllowOverride* in the Apache vhost configuration.

   If you have Apache 2.3.9, ensure that the *AllowOverride* parameter has the value *None*.

Zend Guard Loader is not needed because OXID eShop 6 is not encrypted.

Database
--------

* MySQL 5.5 and 5.7
* MariaDB Support (tested with MariaDB 10.4)

The database user needs sufficient permission to create a database during the installation if it doesn’t already exist. The user also needs permission to create views.

The transaction isolation level must be left with the default value *REPEATABLE READ* for the InnoDB Storage Engine.

PHP
---

* PHP version 7.4, 8.0, or 8.1
* Recommended *memory_limit* is 60 MB, but it should be no less than 32 MB
* PHP setting *session.auto_start* in :file:`php.ini` should be disabled (OFF)
* File uploads should be enabled in PHP
* Enabled *allow_url_fopen* and *fsockopen* on port 80
* Apache server variables *REQUEST_URI* or *SCRIPT_URI* must be available
* *ini_set* allowed

PHP extensions that need to be installed:

* *GD LIB* version 2.x
* *PDO_MySQL*
* *BC Math*
* *JSON*
* *iconv*
* *tokenizer*
* *mbstring*
* *cURL*
* *SOAP*
* *DOM*

.. note:: To run PHP 8, we strongly recommend setting the the error_reporting of PHP to ``error_reporting = E_ALL & ~E_NOTICE & ~E_WARNING & ~E_DEPRECATED``. Otherwise you will get a lot of warnings.

Composer
--------

* Composer 2.7

You need Composer for the installation of OXID eShop and changes in autoloading of files (not at runtime). Find the requirements for Composer at `https://getcomposer.org/doc/00-intro.md#system-requirements <https://getcomposer.org/doc/00-intro.md#system-requirements>`_.

OpenSSL
-------

Compilation modules require OpenSSL.

* *openssl* >= 1.0.1


.. Intern: oxbaac, Status:
