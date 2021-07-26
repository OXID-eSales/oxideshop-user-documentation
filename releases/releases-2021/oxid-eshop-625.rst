OXID eShop 6.2.5
================

Release date: 03/08/2021

-----------------------------------------------------------------------------------------

General information
-------------------
OXID eShop 6.2.5 is provided as a compilation with the following components:

* OXID eShop CE 6.7.2
* OXID eShop PE 6.4.1
* OXID eShop EE 6.5.5
* Theme "Flow" 3.7.2
* Theme "Wave" 1.6.1
* Amazon Pay 3.6.8
* GDPR Opt-In 2.3.3
* Klarna 5.5.1
* OXID Cookie Management powered by usercentrics 1.1.3
* Paymorrow 2.1.0
* PAYONE 1.5.0
* PayPal 6.3.1
* WYSIWYG Editor + Mediathek 2.4.0
* Visual CMS 3.5.3 (PE/EE)

All changes to the compilation can be viewed in the following metapackage: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.2.4...v6.2.5>`_.

System requirements
^^^^^^^^^^^^^^^^^^^
OXID eShop 6.2.5 runs under PHP 7.1 to 7.4.

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

* OXID eShop CE (update from 6.7.0 to 6.7.2), `Changelog 6.7.2 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.7.2/CHANGELOG.md>`_
* Theme "Flow" (update from 3.7.0 to 3.7.2), `Changelog 3.7.2 <https://github.com/OXID-eSales/flow_theme/blob/v3.7.2/CHANGELOG.md>`_
* Theme "Wave" (update from 1.6.0 to 1.6.1), `Changelog 1.6.1 <https://github.com/OXID-eSales/wave-theme/blob/v1.6.1/CHANGELOG.md>`_
* GDPR Opt-In (update from 2.3.2 to 2.3.3), `Changelog 2.3.3 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics (update from 1.1.2 to 1.1.3), `Changelog 1.1.3 <https://github.com/OXID-eSales/usercentrics/blob/v1.1.3/CHANGELOG.md>`_
* Klarna (update from 5.5.0 to 5.5.1), `Changelog 5.5.1 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.1/CHANGELOG.md>`_
* Paymorrow (update from 2.0.3 to 2.1.0), `Changelog 2.1.0 <https://github.com/OXID-eSales/paymorrow-module/blob/v2.1.0/CHANGELOG.md>`_
* PAYONE (update from 1.3.1 to 1.5.0), `Changelog 1.5.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.5.0/Changelog.txt>`_
* PayPal (update from 6.2.2 to 6.3.1), `Changelog 6.3.1 <https://github.com/OXID-eSales/paypal/blob/v6.3.1/CHANGELOG.md>`_
* OXID eShop composer plugin (update from 5.1.0 to 5.2.0), `Changelog 5.2.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.2.0/CHANGELOG.md>`_
* OXID eShop DemoData installer (update from 1.1.3 to 1.2.0)
* OXID eShop facts (update from 2.3.2 to 2.4.0), `Changelog 2.4.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v2.4.0/CHANGELOG.md>`_
* Unified Namespace Generator (update from 2.1.0 to 2.2.0), `Changelog 2.2.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v2.2.0/CHANGELOG.md>`_

Changes from the previous version of the OXID eShop component can be viewed in the Community Edition repository on GitHub: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.7.0...v6.7.2. Switch to the :guilabel:`Files changed` tab to see the list of all changed files.

-----------------------------------------------------------------------------------------

Corrections
-----------
No fixes for OXID eShop 6.2.5


.. Intern: oxbajv, Status: transL