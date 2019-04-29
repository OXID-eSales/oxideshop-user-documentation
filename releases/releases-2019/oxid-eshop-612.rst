OXID eShop 6.1.2
================

Release date: 29/01/2019

-----------------------------------------------------------------------------------------

General information
-------------------
OXID eShop 6.1.2 is provided as a compilation with the following components:

* OXID eShop CE 6.3.2
* OXID eShop PE 6.2.2
* OXID eShop EE 6.2.1
* Theme "Flow" 3.1.0
* Theme "Wave" 1.0.1
* Amazon Pay 3.2.2
* GDPR Opt-In 2.1.2
* Klarna 4.2.1
* Paymorrow 2.0.1
* PAYONE 1.0.10
* PayPal 5.2.3
* Summernote WYSIWIG editor and Media Gallery 2.2.0
* Visual CMS 3.3.0 (PE/EE)

All changes to the compilation can be viewed in the following metapackage: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.1.1...v6.1.2>`_.

System requirements
^^^^^^^^^^^^^^^^^^^
OXID eShop 6.1.2 runs under PHP 7.0 and 7.1. PHP 5.6 is no longer supported. The supported database is MySQL version 5.5 or 5.7. Using MySQL 5.6 is not recommended as it could cause issues with Enterprise Edition. Please refer to the blog post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Apache 2.2 or 2.4 can be used as a web server on a Linux system.

Installation
^^^^^^^^^^^^
Please follow the instructions in section "Installation":

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing updates <../../installation/installing-updates/installing-updates>`

Please run the update first in a test or development environment, or a copy of your current shop. Then, test the ordering process and payment and shipping methods. If the shop works correctly, you can replace the shop in the live system with the one from the test or development environment.

-----------------------------------------------------------------------------------------

New Functions
-------------

The theme "Wave" - responsive and based on Bootstrap 4 - is now a new component of the OXID eShop compilation. More information about the theme can be found in the blog post `Introducing Wave theme <https://oxidforge.org/en/introducing-wave-theme.html>`_ on the OXIDforge.

-----------------------------------------------------------------------------------------

Improvements and adjustments
----------------------------

Updated components of the OXID eShop compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The following components have been updated to a new version:

* OXID eShop CE (update from 6.3.1 to 6.3.2), `Changelog 6.3.2 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.3.2/CHANGELOG.md>`_
* OXID eShop PE (update from 6.2.1 to 6.2.2)
* OXID eShop EE (update from 6.2.0 to 6.2.1)
* Theme "Flow" (update from 3.0.2 to 3.1.0) `Changelog 3.1.0 <https://github.com/OXID-eSales/flow_theme/blob/v3.1.0/CHANGELOG.md>`_
* AmazonPay (update from 3.2.1 to 3.2.2), `Changelog 3.2.2 <https://github.com/bestit/amazon-pay-oxid/blob/3.2.2/CHANGELOG.md>`_
* Klarna (update from 4.2.0 to 4.2.1), `Changelog 4.2.1 <https://github.com/topconcepts/OXID-Klarna-6/blob/master/CHANGELOG.md>`_
* Visual CMS (PE/EE, update from 3.2.2 to 3.3.0)

A bug in a function of the Enterprise Edition has been fixed. The correction also required changes in the Community and Professional Editions.

Various adjustments
^^^^^^^^^^^^^^^^^^^
* In the components OXID eShop facts and Doctrine Migration Integration, the tests are no longer delivered via Composer. If these are needed, they can be obtained using the Composer option ``--prefer-source`` or ``git clone`` of the respective repository.
* In Doctrine Migration Wrappers with PR-4 different types of output handlers, such as BufferdOutput, are possible. So far only ConsoleOutput could be processed in the shop. More information can be found in the documentation of the `Symfony API <https://api.symfony.com>`_.
* Due to a security issue in PHPMailer, this class was updated to version 5.2.27.

-----------------------------------------------------------------------------------------

Corrections
-----------
The bugs fixed with this patch are listed in our bugtrack system.

https://bugs.oxid-esales.com/changelog_page.php?version_id=470 and |br|
https://bugs.oxid-esales.com/changelog_page.php?version_id=458

-----------------------------------------------------------------------------------------

Changes from the previous version of the OXID eShop component can be viewed in the Community Edition repository on GitHub: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.2.1...v6.2.2. Switch to the :guilabel:`Files changed` tab to see the list of all changed files.

.. Intern: oxbain, Status: transL