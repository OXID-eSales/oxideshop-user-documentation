OXID eShop 6.3.1
================

Release date: 03/08/2021

-----------------------------------------------------------------------------------------

General information
-------------------
OXID eShop 6.3.1 is provided as a compilation with the following components:

* OXID eShop CE
* OXID eShop PE
* OXID eShop EE
* Theme "Flow"
* Theme "Wave"
* Amazon Pay
* GDPR Opt-In
* Klarna
* OXID Cookie Management powered by usercentrics
* Paymorrow
* PAYONE
* PayPal
* WYSIWYG Editor + Mediathek
* Visual CMS  (PE/EE)

All changes to the compilation can be viewed in the following metapackage: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.3.0...v6.3.1>`_.

System requirements
^^^^^^^^^^^^^^^^^^^
OXID eShop 6.3.1 runs under PHP 8.0, 7.4 and 7.3.

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

Improvements and adjustments
----------------------------
The following components have been updated to a new version:

* OXID eShop CE (update from xxx to xxx), `Changelog xxx <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.8.0/CHANGELOG.md>`_
* OXID eShop PE (update from xxx to xxx)
* OXID eShop EE (update from xxx to xxx)
* Theme "Flow" (update from xxx to xxx), `Changelog xxx <https://github.com/OXID-eSales/flow_theme/blob/v3.7.0/CHANGELOG.md>`_
* Theme "Wave" (update from xxx to xxx), `Changelog xxx <https://github.com/OXID-eSales/wave-theme/blob/v1.6.0/CHANGELOG.md>`_
* GDPR Opt-In (update from xxx to xxx), `Changelog xxx <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics xxx, `Changelog xxx <https://github.com/OXID-eSales/usercentrics/blob/v1.1.3/CHANGELOG.md>`_
* OXID eShop DemoData installer (update from xxx to xxx)
* Amazon Pay (update from xxx to xxx), `Changelog xxx <https://github.com/bestit/amazon-pay-oxid/blob/3.6.8/CHANGELOG.md>`_
* Klarna (update from xxx to xxx), `Changelog xxx <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.0/CHANGELOG.md>`_
* Paymorrow (update from xxx to xxx) `Changelog xxx <https://github.com/OXID-eSales/paymorrow-module/blob/v2.0.4/CHANGELOG.md>`_
* PayPal (update from xxx to xxx), `Changelog xxx <https://github.com/OXID-eSales/paypal/blob/v6.2.3/CHANGELOG.md>`_
* OXID eShop composer plugin (update from xxx to xxx) `Changelog xxx <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.2.0/CHANGELOG.md>`_
* OXID eShop DemoData installer (update from xxx to xxx)
* OXID eShop doctrine migration integration (update from xxx to xxx) `Changelog xxx <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v3.2.0/CHANGELOG.md>`_
* Unified Namespace Generator (update from xxx to xxx) `Changelog xxx <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v2.2.0/CHANGELOG.md>`_

Changes from the previous version of the OXID eShop component can be viewed in the Community Edition repository on GitHub: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.6.0...v6.8.0. Switch to the :guilabel:`Files changed` tab to see the list of all changed files.

-----------------------------------------------------------------------------------------

Corrections
-----------
The bugs fixed with this patch are listed in our bugtrack system. |br|
https://bugs.oxid-esales.com/changelog_page.php?version_id=626


.. Intern: oxbajw, Status: transL