Reinstallation
================

This section tells you how to reinstall OXID eShop 6.1. There is one decisive change compared to shop versions 4 and 5: The installation is no longer based on installation packages. The files required for the shop are provided by Composer, a dependency manager for PHP. After that, you can run the web-based setup and install the shop as usual.

.. image:: ../../media/screenshots/oxbaae01.png
    :alt: Setup, Step 1
    :height: 532
    :width: 650

The installation guide in English can be found in the developer documentation: `<https://docs.oxid-esales.com/developer/en/6.1/getting_started/installation/index.html>`_.

-----------------------------------------------------------------------------------------

Server und system requirements
--------------------------------
**Contents**: server, shared hosting, managed server, server farm with load balancing and database cluster, Linux, web server, Apache 2.2 + 2.4, MySQL 5.5 + 5.7, PHP 7.0 and 7.1, Composer, OpenSSL |br|
:doc:`Read article <server-and-system-requirements>` |link|

Preparing for installation
------------------------
**Contents**: installing Composer, providing shop files, configuring Apache, customising file and directory permissions, creating database |br|
:doc:`Read article <preparing-for-installation>` |link|

Running setup
---------------
**Contents**: web-based setup, checking system requirements, selecting main shipping country and shop’s language, license terms, database, database name, specifying database user and password, demo data, shop directories, defining login data for the Admin panel, shop administrator, entering license key (PE and EE) |br|
:doc:`Read article <running-setup>` |link|

Completing installation
------------------------
**Contents**: checking deletion of the setup directory, setting file and directory permissions, write permissions for /out/pictures, /out/media, /log, /export, /tmp, write protection for .htaccess, config.inc.php  |br|
:doc:`Read article <completing-installation>` |link|

.. Intern: oxbaae, Status:
