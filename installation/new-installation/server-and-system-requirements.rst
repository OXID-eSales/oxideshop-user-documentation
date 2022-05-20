Server and system requirements
==============================

OXID eShop can run on different server systems. The choice of a suitable hosting package depends, for example, on the number of products, the expected number of visitors in the shop, and the number of orders. While a shared hosting system is sufficient for a small shop with a few hundred products, a few visitors per month and a manageable order volume, a managed server system should be selected for larger shops. As the load increases, you should consider using a server farm with load balancing and a database cluster. Please contact our `OXID Hosting Partners <https://www.oxid-esales.com/oxid-welt/partner/partner-finden/>`_ for advice and support in selecting the right system. They provide solutions specifically tailored to OXID eShop.

The following system requirements must be met to operate OXID eShop version 6.

Web server
----------

* Apache version 2.2 and 2.4 (on Linux)
* 500 MB of free webspace for Community and Professional Edition
* 750 MB of free webspace for Enterprise Edition
* Installed *mod_rewrite* extension

Please note that even with the *mod_rewrite* extension installed, the system health check may not meet the requirements. Often, one of the reasons for this is the setting for *AllowOverride* in the Apache vhost configuration. This was changed to *AllowOverride None* with Apache 2.3.9.

Zend Guard Loader is no longer needed because OXID eShop 6 is not encrypted.

Database
--------

* MySQL 5.5 and 5.7
* MariaDB Support (tested with MariaDB 10.4)

The database user needs sufficient permission to create a database during the installation if it doesn’t already exist. The user also needs permission to create views.

The transaction isolation level must be left with the default value *REPEATABLE READ* for the InnoDB Storage Engine.

PHP
---

* PHP version 8.0, 7.4 und 7.3
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

.. note:: To run PHP 8 we strongly recommend to set the the error_reporting of PHP to ``error_reporting = E_ALL & ~E_NOTICE & ~E_WARNING & ~E_DEPRECATED`` otherwise you will get a lot of warnings.

.. _server_requirements_composer:

Composer
--------

OXID eShop uses Composer as a dependency manager and classes autoloader.
Recommended Composer versions are:

* v1 or v2 (up to v2.2.x) for OXID eShop 6.3.0 and older
* v2 (up to v2.2.x) for OXID eShop 6.3.1 and newer.

.. warning::
    It's not possible to use Composer v2.3.x or newer with the current version of OXID eShop.
    The issue will be mitigated in the upcoming minor release of OXID eShop.
    Meanwhile, you can install any previous version of `Composer <https://getcomposer.org/download/>`_,
    or set the existing one to the latest compatible version to make sure it's fully operational with OXID eShop.
    E.g. by running the following in terminal:
.. code:: bash

   composer selfupdate 2.2.12

""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
Why it might be necessary to use an older version of Composer?
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

Composer, being a PHP application, utilizes `Symfony components <https://symfony.com/components>`_ for its internal operation.
Starting with v2.3.0, Composer bundles versions of these components that conflict with the ones used in OXID eShop
(`see discussion with the similar issue <https://github.com/composer/composer/issues/10671>`_)

OpenSSL
-------

Compilation modules require OpenSSL.

* *openssl* >= 1.0.1


.. Intern: oxbaac, Status:
