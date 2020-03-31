OXID eShop 6.1.6
================

Release date: 31/03/2020

-----------------------------------------------------------------------------------------

General information
-------------------
OXID eShop 6.1.6 is provided as a compilation with the following components:

* OXID eShop CE 6.3.7
* OXID eShop PE 6.2.3
* OXID eShop EE 6.2.4
* Theme "Flow" 3.4.1
* Theme "Wave" 1.3.1
* Amazon Pay 3.3.1
* GDPR Opt-In 2.2.0
* Klarna 5.1.3
* Paymorrow 2.0.1
* PAYONE 1.3.1
* PayPal 5.3.1
* Summernote WYSIWIG editor and Media Gallery 2.2.0
* Visual CMS 3.3.3 (PE/EE)

All changes to the compilation can be viewed in the following metapackage: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.1.5...v6.1.6>`_.

The OXID eShop 6.1.6 contains a security fix for the payment module PAYONE. We recommend a quick update to this shop version.

System requirements
^^^^^^^^^^^^^^^^^^^
OXID eShop 6.1.6 runs under PHP 7.0 and 7.1. The supported database is MySQL version 5.5 or 5.7. Using MySQL 5.6 is not recommended as it could cause issues with Enterprise Edition. Please refer to the blog post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Apache 2.2 or 2.4 can be used as a web server on a Linux system.

Installation
^^^^^^^^^^^^
Please follow the instructions in section “Installation”:

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing updates <../../installation/installing-updates/installing-updates>`

Please run the update first in a test or development environment, or a copy of your current shop. Then, test the ordering process and payment and shipping methods. If the shop works correctly, you can replace the shop in the live system with the one from the test or development environment.

The OXID eShop 6.0.* has now reached EOL (End of Life) and is no longer supported. Please run an update if you still use a shop of this series.

-----------------------------------------------------------------------------------------

Improvements and adjustments
----------------------------
The following components have been updated to a new version:

* OXID eShop CE (update from 6.3.6 to 6.3.7), `Changelog 6.3.7 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.3.7/CHANGELOG.md>`_
* OXID eShop PE (update from 6.2.2 to 6.2.3)
* OXID eShop EE (update from 6.2.3 to 6.2.4)
* OXID eShop facts (update from 2.3.1 to 2.3.2), `Changelog 2.3.2 <https://github.com/OXID-eSales/oxideshop-facts/blob/v2.3.2/CHANGELOG.md/>`_
* Theme "Flow" (update from 3.3.0 to 3.4.1), `Changelog 3.4.1 <https://github.com/OXID-eSales/flow_theme/blob/v3.4.1/CHANGELOG.md>`_
* Theme "Wave" (update from 1.2.0 to 1.3.1), `Changelog 1.3.1 <https://github.com/OXID-eSales/wave-theme/blob/v1.3.1/CHANGELOG.md/>`_
* Klarna (update from 4.3.0 to 5.1.3), `Changelog 5.1.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.1.3/CHANGELOG.md>`_
* PAYONE (update from 1.0.10 to 1.3.1), `Changelog v1.3.1 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.3.1/Changelog.txt>`_
* PayPal (update from 5.2.5 to 5.3.1), `Changelog 5.3.1 <https://github.com/OXID-eSales/paypal/blob/v5.3.1/CHANGELOG.md>`_
* Visual CMS (PE/EE, update from 3.3.2 to 3.3.3)

Changes from the previous version of the OXID eShop component can be viewed in the Community Edition repository on GitHub: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.3.6...v6.3.7. Switch to the :guilabel:`Files changed` tab to see the list of all changed files.

-----------------------------------------------------------------------------------------

Corrections
-----------
The bugs fixed with this patch are listed in our bugtrack system.

https://bugs.oxid-esales.com/changelog_page.php?version_id=541


.. Intern: oxbaja, Status: transL