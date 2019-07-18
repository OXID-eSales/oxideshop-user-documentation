OXID eShop 6.1.4
================

Release date: 30/07/2019

-----------------------------------------------------------------------------------------

General information
-------------------
OXID eShop 6.1.4 is provided as a compilation with the following components:

* OXID eShop CE 6.3.5
* OXID eShop PE 6.2.2
* OXID eShop EE 6.2.3
* Theme "Flow" 3.3.0
* Theme "Wave" 1.2.0
* AmazonPay 3.3.1
* GDPR Opt-In 2.2.0
* Klarna 4.3.0
* Paymorrow 2.0.1
* PAYONE 1.0.10
* PayPal 5.2.5
* Summernote WYSIWIG editor und Media Gallery 2.2.0
* Visual CMS 3.3.2 (PE/EE)

All changes to the compilation can be viewed in the following metapackage: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.1.3...v6.1.4>`_.

System requirements
^^^^^^^^^^^^^^^^^^^
OXID eShop 6.1.4 runs under PHP 7.0 and 7.1. The supported database is MySQL version 5.5 or 5.7. Using MySQL 5.6 is not recommended as it could cause issues with Enterprise Edition. Please refer to the blog post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Apache 2.2 or 2.4 can be used as a web server on a Linux system.

Installation
^^^^^^^^^^^^
Please follow the instructions in section "Installation":

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing updates <../../installation/installing-updates/installing-updates>`

Please run the update first in a test or development environment, or a copy of your current shop. Then, test the ordering process and payment and shipping methods. If the shop works correctly, you can replace the shop in the live system with the one from the test or development environment.

-----------------------------------------------------------------------------------------

Improvements and adjustments
----------------------------

Updated components of the OXID eShop compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The following components have been updated to a new version:

* OXID eShop CE (update from 6.3.3 to 6.3.5), `Changelog 6.3.5 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.3.5/CHANGELOG.md>`_
* OXID eShop EE (update from 6.2.2 to 6.2.3)
* Theme "Flow" (update from 3.2.0 to 3.3.0), `Changelog 3.3.0 <https://github.com/OXID-eSales/flow_theme/blob/v3.3.0/CHANGELOG.md>`_
* Theme "Wave" (update from 1.1.0 to 1.2.0), `Changelog 1.2.0 <https://github.com/OXID-eSales/wave-theme/blob/v1.2.0/CHANGELOG.md>`_
* Klarna (update from 4.2.2 to 4.3.0), `Changelog 4.3.0 <https://github.com/topconcepts/OXID-Klarna-6/blob/v4.3.0/CHANGELOG.md>`_
* GDPR Opt-In (Update from 2.1.2 to 2.2.0), `Changelog 2.2.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.2.0/CHANGELOG.md>`_
* Visual CMS (PE/EE, update from 3.3.1 to 3.3.2)

-----------------------------------------------------------------------------------------

Corrections
-----------
The bugs fixed with this patch are listed in our bugtrack system.

https://bugs.oxid-esales.com/changelog_page.php?version_id=504

-----------------------------------------------------------------------------------------

Changes from the previous version of the OXID eShop component can be viewed in the Community Edition repository on GitHub: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.3.3...v6.3.5. Switch to the :guilabel:`Files changed` tab to see the list of all changed files.

.. Intern: oxbaip, Status: transL