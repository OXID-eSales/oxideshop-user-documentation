OXID eShop 6.3.3
================

Release date: 27-02-2024

-----------------------------------------------------------------------------------------

To close a security vulnerability in Composer, install OXID eShop 6.3.3.

For security reasons, OXID eShop 6.3.3 requires Composer version 2.2.23.

For more information, see

* `Composer Version 2.2.23 <https://github.com/composer/composer/releases/tag/2.2.23>`_
* `CVE-2024-24821 <https://nvd.nist.gov/vuln/detail/CVE-2024-24821>`_

.. note::

   **New terms of use of the OXID eShop Community Edition (CE)**

   Note that by installing OXID eShop 6.3.3 you agree to the new terms of use, which are valid from 15.08.2022.

   For more information, see

   * `CE License Terms Update <https://www.oxid-esales.com/ce-lizenzbedingungen-update/>`_
   * `A new era begins for us, too <https://www.oxid-esales.com/blog/auch-fuer-uns-beginnt-ein-neues-zeitalter/>`_

General information
-------------------

OXID eShop 6.3.3 is provided as a compilation. The compilation contains among others the following components.

* OXID eShop CE 6.9.1
* OXID eShop PE 6.5.1
* OXID eShop EE 6.6.1
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


Improvements and adjustments
----------------------------

View the changes to the compilation in the following metapackage: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.3.2...v6.3.3>`_.

The following component has been updated:

* OXID eShop CE (update from 6.9.0 to 6.9.1) `Changelog 6.9.1 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.9.1/CHANGELOG.md>`_

.. todo: #HR: klären

Changes from the previous version of the OXID eShop component can be viewed in the Community Edition repository on GitHub: `<https://github.com/OXID-eSales/oxideshop_ce/compare/v6.9.0...v6.9.1>`_.
|br|
Switch to the :guilabel:`Files changed` tab to see the list of all changed files.


System requirements
-------------------

OXID eShop 6.3.3 runs under PHP 8.0, 7.4 and 7.3.

The supported database is MySQL version 5.5 or 5.7 and MariaDB version 10.4. Using MySQL 5.6 is not recommended as it could cause issues with Enterprise Edition. Please refer to the blog post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_.

Apache 2.2 or 2.4 can be used as a web server on a Linux system.

Composer is supported in versions 1 and 2.

Installation
------------
Please follow the instructions in section “Installation”:

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing updates <../../installation/update/update>`

Run the update first in a test or development environment, or a copy of your current shop. Then, test the ordering process and payment and shipping methods. If the shop works correctly, you can replace the shop in the live system with the one from the test or development environment.





.. Intern: , Status: transL