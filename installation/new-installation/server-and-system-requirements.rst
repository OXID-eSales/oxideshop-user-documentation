Server and system requirements
==============================

OXID eShop can run on different server systems. The choice of a suitable hosting package depends, for example, on the number of products, the expected number of visitors in the shop, and the number of orders. While a shared hosting system is sufficient for a small shop with a few hundred products, a few visitors per month and a manageable order volume, a managed server system should be selected for larger shops. As the load increases, you should consider using a server farm with load balancing and a database cluster. Please contact our `OXID Hosting Partners <https://www.oxid-esales.com/oxid-welt/partner/partner-finden/>`_ for advice and support in selecting the right system. They provide solutions specifically tailored to OXID eShop.

The following system requirements must be met to operate OXID eShop version 6. There are some changes compared to the system requirements for shop versions 4 and 5, including the supported versions for the Apache web server, MySQL database and the server-side PHP scripting and programming language.

Web server
----------

* Apache version 2.2 and 2.4 (on Linux)
* 500 MB of free webspace for Community and Professional Edition
* 750 MB of free webspace for Enterprise Edition
* Installed *mod_rewrite* extension

Please note that even with the *mod_rewrite* extension installed, the system health check may not meet the requirements. Often, one of the reasons for this is the setting for *AllowOverride* in the Apache vhost configuration. This was changed to *AllowOverride None* with Apache 2.3.9.

Zend Guard Loader is no longer needed because OXID eShop 6 is not encrypted.

MySQL
-----

* MySQL 5.5 and 5.7

The database user needs sufficient permission to create a database during the installation if it doesn’t already exist. The user also needs permission to create views.

The transaction isolation level must be left with the default value *REPEATABLE READ* for the InnoDB Storage Engine.

PHP
---

* PHP version 7.0 and 7.1
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

Composer
--------

Composer is required for the installation of OXID eShop and changes in autoloading of files (not at runtime). The requirements for Composer can be found in `https://getcomposer.org/doc/00-intro.md#system-requirements <https://getcomposer.org/doc/00-intro.md#system-requirements>`_.

OpenSSL
-------

Compilation modules require OpenSSL.

* *openssl* >= 1.0.1

.. Intern: oxbaac, Status:
