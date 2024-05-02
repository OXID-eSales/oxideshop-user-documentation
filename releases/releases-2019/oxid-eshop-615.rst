OXID eShop 6.1.5
================

Release date: 29/10/2019

-----------------------------------------------------------------------------------------

General information
-------------------
OXID eShop 6.1.5 is provided as a compilation with the following components:

* OXID eShop CE CE 6.3.6
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
* WYSIWYG Editor + Mediathek 2.2.0
* Visual CMS 3.3.2 (PE/EE)

All changes to the compilation can be viewed in the following metapackage: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.1.4...v6.1.5>`_.

With OXID eShop 6.1.5, we have resolved a security issue: with a specially crafted URL, users with administrative rights could unintentionally grant unauthorized users access to the admin panel. Details on the security issue can be found on the following page of OXIDforge: `Security Bulletin 2019-002 <https://oxidforge.org/en/security-bulletin-2019-002.html>`_. We recommend a quick update to this shop version. For instructions on updating the shop, see `Installing updates <https://docs.oxid-esales.com/eshop/en/6.1/installation/installing-updates/installing-updates.html>`_.

System requirements
^^^^^^^^^^^^^^^^^^^
OXID eShop 6.1.5 runs under PHP 7.0 and 7.1. The supported database is MySQL version 5.5 or 5.7. Using MySQL 5.6 is not recommended as it could cause issues with Enterprise Edition. Please refer to the blog post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Apache 2.2 or 2.4 can be used as a web server on a Linux system.

Installation
^^^^^^^^^^^^
Please follow the instructions in section "Installation":

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing updates <../../installation/installing-updates/installing-updates>`

Please run the update first in a test or development environment, or a copy of your current shop. Then, test the ordering process and payment and shipping methods. If the shop works correctly, you can replace the shop in the live system with the one from the test or development environment.

-----------------------------------------------------------------------------------------

Improvements and adjustments
----------------------------
The OXID eShop CE component has been updated from version 6.3.5 to 6.3.6. See `Changelog 6.3.6. <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.3.6/CHANGELOG.md>`_.

-----------------------------------------------------------------------------------------

Corrections
-----------
The bugs fixed with this patch are listed in our bugtrack system.

https://bugs.oxid-esales.com/changelog_page.php?version_id=526

-----------------------------------------------------------------------------------------

Changes from the previous version of the OXID eShop component can be viewed in the Community Edition repository on GitHub: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.3.5...v6.3.6. Switch to the :guilabel:`Files changed` tab to see the list of all changed files.



.. Intern: oxbaja, Status: transL