OXID eShop 6.3.0
================

Release date: 08/04/2021

-----------------------------------------------------------------------------------------

General information
-------------------
OXID eShop 6.3.0 is provided as a compilation with the following components:

* OXID eShop CE ???
* OXID eShop PE ???
* OXID eShop EE ???
* Theme "Flow" 3.7.0
* Theme "Wave" 1.6.0
* Amazon Pay 3.6.8
* GDPR Opt-In 2.3.2
* Klarna 5.4.0
* OXID Cookie Management powered by usercentrics 1.1.2
* Paymorrow 2.0.3
* PAYONE 1.3.1
* PayPal 6.2.2
* WYSIWYG Editor + Mediathek 2.4.0
* Visual CMS 3.5.3 (PE/EE)

All changes to the compilation can be viewed in the following metapackage: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.2.3...v6.3.0>`_.

System requirements
^^^^^^^^^^^^^^^^^^^
OXID eShop 6.3.0 runs under PHP 8.0, 7.4 and 7.3.

The supported database is MySQL version 5.5 or 5.7 and MariaDB version 10.4. Using MySQL 5.6 is not recommended as it could cause issues with Enterprise Edition. Please refer to the blog post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_.

Apache 2.2 or 2.4 can be used as a web server on a Linux system.

Composer is supported in versions 1 and 2.

Installation
^^^^^^^^^^^^
Please follow the instructions in section “Installation”:

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing updates <../../installation/update/update>`

Please run the update first in a test or development environment, or a copy of your current shop. Then, test the ordering process and payment and shipping methods. If the shop works correctly, you can replace the shop in the live system with the one from the test or development environment.

-----------------------------------------------------------------------------------------

New functions
-------------
PHP 8.0 supported
^^^^^^^^^^^^^^^^^
OXID eShop 6.3.0 now also runs under PHP 8.0. Support for PHP 7.1 and 7.2 was dropped.

New component of OXID eShop compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
OXID eShop compilation has been enhanced with the OXID Cookie Management powered by usercentrics 1.1.2 module. The module provides functions to bring the web tracking technologies used in OXID eShop in line with legal requirements. This is implemented by integrating the Content Management Platform (CMS) from Usercentrics.


-----------------------------------------------------------------------------------------

Improvements and adjustments
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The following components have been updated to a new version:

* ??? OXID eShop CE (update from 6.6.0 to 6.6.x), `Changelog 6.6.x <https://github.com/OXID-eSales/oxideshop_ce/blob/dev-b-6.2.x/CHANGELOG.md>`_
* ??? OXID eShop PE (update from 6.4.1 to 6.4.x)
* ??? OXID eShop EE (update from 6.5.4 to 6.5.x)
* Theme "Flow" (update from 3.6.0 to 3.7.0), `Changelog 3.7.0 <https://github.com/OXID-eSales/flow_theme/blob/v3.7.0/CHANGELOG.md>`_
* Theme "Wave" (update from 1.5.0 to 1.6.0), `Changelog 1.6.0 <https://github.com/OXID-eSales/wave-theme/blob/v1.6.0/CHANGELOG.md>`_
* GDPR Opt-In (update from 2.3.1 to 2.3.2), `Changelog 2.3.2 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.2/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics 1.1.2, `Changelog 1.1.2 <https://github.com/OXID-eSales/usercentrics/blob/v1.1.2/CHANGELOG.md>`_
* OXID eShop DemoData installer (update from 1.1.2 to 1.1.3)
* Amazon Pay (update from 3.6.4 to 3.6.8), `Changelog 3.6.8 <https://github.com/bestit/amazon-pay-oxid/blob/3.6.8/CHANGELOG.md>`_
* PayPal (update from 6.2.1 to 6.2.2), `Changelog 6.2.2 <https://github.com/OXID-eSales/paypal/blob/v6.2.2/CHANGELOG.md>`_
* Klarna (update from 5.3.0 to 5.4.0), `Changelog 5.4.0 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.4.0/CHANGELOG.md>`_

Changes from the previous version of the OXID eShop component can be viewed in the Community Edition repository on GitHub: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.6.0…v6.6.x. Switch to the :guilabel:`Files changed` tab to see the list of all changed files.

-----------------------------------------------------------------------------------------

Corrections
-----------
The bugs fixed with this patch are listed in our bugtrack system. |br|
https://bugs.oxid-esales.com/changelog_page.php?version_id=???


.. Intern: oxbajs, Status: