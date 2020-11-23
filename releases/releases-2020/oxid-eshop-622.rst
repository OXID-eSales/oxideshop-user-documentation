OXID eShop 6.2.2
================

Release date: 28/07/2020

-----------------------------------------------------------------------------------------

General information
-------------------
OXID eShop 6.2.2 is provided as a compilation with the following components:

* OXID eShop CE 6.5.6
* OXID eShop PE 6.4.1
* OXID eShop EE 6.5.3
* Theme "Flow" 3.5.0
* Theme "Wave" 1.4.0
* Amazon Pay 3.6.4
* GDPR Opt-In 2.3.1
* Klarna 5.1.4
* Paymorrow 2.0.3
* PAYONE 1.3.1
* PayPal 6.2.0
* WYSIWYG Editor + Mediathek 2.3.0
* Visual CMS 3.4.0 (PE/EE)

All changes to the compilation can be viewed in the following metapackage: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.2.1...v6.2.2>`_.

System requirements
^^^^^^^^^^^^^^^^^^^
OXID eShop 6.1.2 runs under PHP 7.1 to 7.4. The supported database is MySQL version 5.5 or 5.7 and MariaDB version 10.4. Using MySQL 5.6 is not recommended as it could cause issues with Enterprise Edition. Please refer to the blog post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Apache 2.2 or 2.4 can be used as a web server on a Linux system.

Installation
^^^^^^^^^^^^
Please follow the instructions in section "Installation":

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing updates <../../installation/update/update>`

Please run the update first in a test or development environment, or a copy of your current shop. Then, test the ordering process and payment and shipping methods. If the shop works correctly, you can replace the shop in the live system with the one from the test or development environment.

-----------------------------------------------------------------------------------------

Improvements and adjustments
----------------------------
The following components have been updated to a new version:

* OXID eShop CE (update from 6.5.4 to 6.5.6), `Changelog 6.5.6 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.5.6/CHANGELOG.md>`_
* OXID eShop PE (update from 6.4.0 to 6.4.1)
* OXID eShop EE (update from 6.5.2 to 6.5.3)
* Theme "Flow" (update from 3.4.1 to 3.5.0), `Changelog 3.5.0 <https://github.com/OXID-eSales/flow_theme/blob/v3.5.0/CHANGELOG.md>`_
* Theme "Wave" (update from 1.3.1 to 1.4.0), `Changelog 1.4.0 <https://github.com/OXID-eSales/wave-theme/blob/v1.4.0/CHANGELOG.md>`_
* GDPR Opt-In (update from 2.3.0 to 2.3.1), `Changelog 3.3.1 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.1/CHANGELOG.md>`_
* PayPal (update from 6.1.0 to 6.2.0), `Changelog 6.2.0 <https://github.com/OXID-eSales/paypal/blob/v6.2.0/CHANGELOG.md>`_
* WYSIWYG Editor + Mediathek (update from 2.2.0 to 2.3.0), `Changelog 2.3.0 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v2.3.0/CHANGELOG.md>`_
* Visual CMS, PE/EE (update from 3.3.3 to 3.4.0)
* OXID eShop composer plugin (update from 4.1.1 to 5.0.1), `Changelog 5.0.1 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.0.1/CHANGELOG.md>`_

Changes from the previous version of the OXID eShop component can be viewed in the Community Edition repository on GitHub: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.5.4...v6.5.6. Switch to the :guilabel:`Files changed` tab to see the list of all changed files.

Price alert becomes wished price
--------------------------------
The function that allows customers to specify a price for a product from the shop at which they would buy it has been renamed. The price alert is now :doc:`Wished price <../../operation/wished-price/wished-price>`.

-----------------------------------------------------------------------------------------

Corrections
-----------
The bugs fixed with this patch are listed in our bugtrack system. |br|
https://bugs.oxid-esales.com/changelog_page.php?version_id=554


.. Intern: oxbajp, Status: transL