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

The following system requirements must be met to operate OXID eShop version 7.

Webserver
---------

* Apache version 2.2 or 2.4 (on Linux)
* 500 MB of free webspace for Community and Professional Edition
* 750 MB of free webspace for Enterprise Edition
* *mod_rewrite* extension installed

  ..  note::

       After finishing the installation, you go to the web-based shop setup.

       Before you can start the setup, the system checks whether the system requirements are met.

       Under :guilabel:`Server Configuration`, the *Apache mod_rewrite Module* bay be marked as defective, even with the *mod_rewrite* extension installed.

       Often, one of the reasons for this is the setting for *AllowOverride* in the Apache vhost configuration.

       If you have Apache 2.3.9, ensure that the *AllowOverride* parameter has the value *None*.

* Cryptographically-sufficient configuration

  ..  note::
      **What is cryptographically-sufficient configuration and how to achieve it?**

      One of the features of a secure web application is the ability to generate cryptographically-strong random values.

      This is why the PHP process needs to have access to an appropriate source of randomness for its CSPRNG (*Cryptographically Secure Pseudorandom Number Generator*) functions (`random_int()`, `random_bytes()`).

      In most cases no additional tweaking from your side will be necessary and application elements should work together out of the box.

      However, if an exception is thrown by one of the PHP functions (`random_int()` or `random_bytes()`), start troubleshooting by looking through the documentation for the functions under `php.net/manual/en/function.random-bytes.php <https://www.php.net/manual/en/function.random-bytes.php>`_ and `php.net/manual/de/function.random-int.php <https://www.php.net/manual/de/function.random-int.php>`_.

Database
--------

* MySQL 5.7 or 8.0
* MariaDB Support (tested with MariaDB 10.4)

The database user needs sufficient permission to create a database during the installation if it doesn’t already exist. The user also needs permission to create views.

The transaction isolation level must be left with the default value *REPEATABLE READ* for the InnoDB Storage Engine.

PHP
---

* PHP version 8.0 or higher
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

.. note:: To run PHP 8, we strongly recommend to set the the error_reporting of PHP to ``error_reporting = E_ALL & ~E_NOTICE & ~E_WARNING & ~E_DEPRECATED``. Otherwise you will get a lot of warnings.

.. note:: The PHP function ``exec()`` uses the standard PHP installation of the server. Under certain circumstances, this differs from the CLI and web server PHP version and can lead to problems during setup or at runtime. In this case it is necessary to consult with the hoster so that the version can be adapted to the system requirements.

Composer
--------

* Composer 2.4

Composer is required for the installation of OXID eShop and changes in autoloading of files (not at runtime). OXID eShop 7.0.0 has been tested with Composer version 2.

Metadata
--------

* Metadata version 2.0 or higher

For more information about metadata versions, in the Developer documentation, see `metadata.php <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/skeleton/metadataphp/index.html>`_.

OpenSSL
-------

Compilation modules require OpenSSL.

* *openssl* >= 1.0.1


.. Intern: oxbaac, Status:
