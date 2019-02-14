OXID eShop 6.1.0
================

Release date: 31/07/2018

-----------------------------------------------------------------------------------------

General information
-----------
OXID eShop 6.1.0 is provided as a compilation with the following components:

* OXID eShop CE 6.3.0
* OXID eShop PE 6.2.0
* OXID eShop EE 6.2.0
* Theme "Flow" 3.0.2
* AmazonPay 3.1.4
* GDPR Opt-In 2.1.1
* Klarna 4.0.1
* Paymorrow 2.0.1
* PAYONE 1.0.8
* PayPal 5.2.2
* Visual CMS 3.2.1 (PE/EE)
* WYSIWIG editor and summernote 2.1.1 media library

All changes to the compilation can be viewed in the following metapackage: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.0.3...v6.1.0>`_.

With OXID eShop 6.1.0, we have resolved two security issues. One of the two security issues is only relevant if the Paymorrow payment method is actively used in the shop. Details on both security issues can be found on the following pages of OXIDforge: `Security Bulletin 2018-002 <https://oxidforge.org/en/security-bulletin-2018-002.html>`_ and `Security Bulletin 2018-003 <https://oxidforge.org/en/security-bulletin-2018-002.html>`_. We recommend a quick update to this shop version (6.1.0) and to the provided Paymorrow 2.0.1 module. For instructions on updating the shop, see :doc:`Installing updates <../../installation/installing-updates/index>`.

System requirements
^^^^^^^^^^^^^^^^^^^^^
OXID eShop 6.1.0 runs under PHP 7.0 and 7.1. PHP 5.6 is no longer supported. The supported database is MySQL version 5.5 or 5.7. Using MySQL 5.6 is not recommended as it could cause issues with Enterprise Edition. Please refer to the blog post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Apache 2.2 or 2.4 can be used as a web server on a Linux system.

Installation
^^^^^^^^^^^^
Please follow the instructions in Section "Installation":

:doc:`Reinstallation <../../installation/new-installation/reinstallation>` |br|
:doc:`Installing updates <../../installation/installing-updates/installing-updates>`

Please run the update first in a test or development environment, or a copy of your current shop. Then, test the ordering process and payment and shipping methods. If the shop works correctly, you can replace the shop in the live system with the one from the test or development environment.

-----------------------------------------------------------------------------------------

New functions
---------------

New components of the OXID eShop compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The OXID eShop compilation has been enhanced with the GDPR Opt-in 2.1.1 and Klarna 4.0.1 modules. The GDPR Opt-in module provides opt-in functions that are required by OXID eShop for the implementation of the General Data Protection Regulation (GDPR). The Klarna module is an additional payment module that shop owners can use, for example, to process payments against invoice, in instalments or by immediate bank transfer via the Klarna financial service provider.

PSR-3 logger
^^^^^^^^^^^^
We have integrated a logger according to PSR-3 specification into OXID eShop. The standardised interface for automatically creating and saving the logs replaces the shop’s previous logging mechanism.

-----------------------------------------------------------------------------------------

Improvements and adjustments
------------------------------

Updated components of the OXID eShop compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The following components have been updated to a new version:

* OXID eShop CE (update from 6.2.0 to 6.3.0), `Changelog 6.3.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.3.0/CHANGELOG.md>`_
* OXID eShop PE (update from 6.1.0 to 6.2.0)
* OXID eShop EE (update from 6.1.1 to 6.2.0)
* Theme "Flow" (update from 3.0.0 to 3.0.2), `Changelog 3.0.2 <https://github.com/OXID-eSales/flow_theme/blob/v3.0.2/CHANGELOG.md>`_
* AmazonPay (update from 3.0.2 to 3.1.4)
* Paymorrow (update from 2.0.0 to 2.0.1), `Changelog 2.0.1 <https://github.com/OXID-eSales/paymorrow-module/blob/v2.0.1/CHANGELOG.md>`_
* PAYONE (update from 1.0.5 to 1.0.8), `Changelog 1.0.8 <https://github.com/PAYONE-GmbH/oxid-6/blob/1.0.8/Changelog.txt>`_
* PayPal (update from 5.1.6 to 5.2.2), `Changelog 5.2.2 <https://github.com/OXID-eSales/paypal/blob/v5.2.2/CHANGELOG.md>`_
* Visual CMS (PE/EE, update from 3.2.0 to 3.2.1) `Changelog 3.2.1 <https://github.com/OXID-eSales/visual_cms_module/blob/v3.2.1/CHANGELOG.md>`_

Configurable contact form
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Mandatory fields of the contact form can be specified in the Admin panel under :menuselection:`Master Settings --> Core Settings`, in the :guilabel:`Settings` tab, section :guilabel:`Other settings`. Only the activated fields will be validated when submitting the contact form.

These contact form settings have been implemented in the context of the General Data Protection Regulation to allow shop owners to only collect the data necessary to process an enquiry.

Modules can override Smarty plugins
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Modules can now overwrite Smarty Plugins. Version 2.1 of the metadata was introduced for this purpose.

Discontinued features and functions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The test script used for OXID eShop 4 & 5, which checked the integrity of the .php files and templates, is no longer supported. The option of calling the script from the Admin panel by checking the :guilabel:`Run Version checker` box under :menuselection:`Service --> Diagnostics tool` has been removed.

-----------------------------------------------------------------------------------------

Corrections
-----------
The above mentioned security issues have been eliminated. The bugs fixed with this release are identical to those of version 6.0.3. Since bugs in the bugtrack system can’t be marked as fixed for all versions, the list applies to OXID eShop 6.0.3.

https://bugs.oxid-esales.com/changelog_page.php?version_id=433

-----------------------------------------------------------------------------------------

Changes from the previous version of the OXID eShop component can be viewed in the Community Edition repository on GitHub: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.2.0...v6.3.0. Switch to the :guilabel:`Files changed` tab to see the list of all changed files.

.. Intern: oxbail, Status: