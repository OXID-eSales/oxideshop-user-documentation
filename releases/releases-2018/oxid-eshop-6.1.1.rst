OXID eShop 6.1.1
================

Release date: 30/10/2018

-----------------------------------------------------------------------------------------

General information
-----------
OXID eShop 6.1.1 is provided as a compilation with the following components:

* OXID eShop CE 6.3.1
* OXID eShop PE 6.2.1
* OXID eShop EE 6.2.0
* Theme "Flow" 3.0.2
* AmazonPay 3.2.1
* GDPR Opt-In 2.1.2
* Klarna 4.2.0
* Paymorrow 2.0.1
* PAYONE 1.0.10
* PayPal 5.2.3
* Visual CMS 3.2.2 (PE/EE)
* WYSIWIG editor and summernote 2.1.1 media library

All changes to the compilation can be viewed in the following metapackage: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.1.0...b-6.1>`_.

System requirements
^^^^^^^^^^^^^^^^^^^^^
OXID eShop 6.1.1 runs under PHP 7.0 and 7.1. PHP 5.6 is no longer supported. The supported database is MySQL version 5.5 or 5.7. Using MySQL 5.6 is not recommended as it could cause issues with Enterprise Edition. Please refer to the blog post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Apache 2.2 or 2.4 can be used as a web server on a Linux system.

Installation
^^^^^^^^^^^^
Please follow the instructions in Section "Installation":

:doc:`Reinstallation <../../installation/new-installation/reinstallation>` |br|
:doc:`Installing updates <../../installation/installing-updates/installing-updates>`

Please run the update first in a test or development environment, or a copy of your current shop. Then, test the ordering process and payment and shipping methods. If the shop works correctly, you can replace the shop in the live system with the one from the test or development environment.

-----------------------------------------------------------------------------------------

Improvements and adjustments
------------------------------

Updated components of the OXID eShop compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The following components have been updated to a new version:

* OXID eShop CE (update from 6.3.0 to 6.3.1), `Changelog 6.3.1 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.3.1/CHANGELOG.md>`_
* OXID eShop PE (update from 6.2.0 to 6.2.1)
* AmazonPay (update from 3.1.4 to 3.2.1)
* GDPR Opt-In (update from 2.1.1 to 2.1.2), `Changelog 2.1.2 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.1.2/CHANGELOG.md>`_
* Klarna (update from 4.0.1 to 4.2.0)
* PAYONE (update from 1.0.8 to 1.0.10), `Changelog 1.0.10 <https://github.com/PAYONE-GmbH/oxid-6/blob/1.0.10/Changelog.txt>`_
* PayPal (update from 5.2.2 to 5.2.3), `Changelog 5.2.3 <https://github.com/OXID-eSales/paypal/blob/v5.2.3/CHANGELOG.md>`_
* Visual CMS (update from 3.2.1 to 3.2.2)

-----------------------------------------------------------------------------------------

Corrections
-----------

The bugs fixed with this patch are listed in our bugtrack system.

https://bugs.oxid-esales.com/changelog_page.php?version_id=462

-----------------------------------------------------------------------------------------

Changes from the previous version of the OXID eShop component can be viewed in the Community Edition repository on GitHub: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.3.0...v6.3.1. Switch to the :guilabel:`Files changed` tab to see the list of all changed files.

.. Intern: oxbaim, Status: