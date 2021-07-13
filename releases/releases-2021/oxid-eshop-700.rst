OXID eShop 7.0.0
================

Release date RC 1: 27.07.2021

-----------------------------------------------------------------------------------------

General information
-------------------
OXID eShop 6.3.0 is provided as a compilation with the following components:

* OXID eShop CE 7.0.0-rc1
* OXID eShop PE 7.0.0-rc1
* OXID eShop EE 7.0.0-rc1
* Theme "Flow" 4.0.0
* Theme "Wave" 2.0.0
* OXID eShop composer plugin 6.0.0
* OXID eShop Views Generator 2.0.0
* OXID eShop DemoData installer 2.0.0
* OXID eShop demodata CE/PE/EE 7.0.0
* OXID eShop doctrine migration integration 4.0.0
* OXID eShop facts 3.0.0
* Unified Namespace Generator 3.0.0

Modules, such as those for the payment methods, the WYSIWYG Editor + Mediathek or Visual CMS for the Professional and Enterprise Edition will be provided with the final release.

System requirements
^^^^^^^^^^^^^^^^^^^
OXID eShop 7.0.0 runs under PHP 8.0, 7.4 and 7.3.

The supported database is MySQL version 5.5 or 5.7 and MariaDB version 10.4. Using MySQL 5.6 is not recommended as it could cause issues with Enterprise Edition. Please refer to the blog post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_.

Apache 2.2 or 2.4 can be used as a web server on a Linux system.

Composer is supported in versions 1 and 2.

Installation
^^^^^^^^^^^^
Please follow the instructions in section "Installation":

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing updates <../../installation/update/update>`

Please run the update first in a test or development environment, or a copy of your current shop. Then, test the ordering process and payment and shipping methods. If the shop works correctly, you can replace the shop in the live system with the one from the test or development environment.

-----------------------------------------------------------------------------------------

New functions
-------------
Setup via command line
^^^^^^^^^^^^^^^^^^^^^^
To complement the web-based setup, OXID eShop can now also be created and configured via the command line. The new command of the OXID eShop console ``oe:setup:store`` creates the database and configures the shop. The necessary information is transferred with parameters. In further steps demo data can be installed with ``oe:setup:demodata`` and the shop administrator can be created with ``oe:admin:create-user``. For OXID eShop Professional and Enterprise Edition, the ``oe:license:add`` command adds a valid license key. See: :doc:`Setup via command line <../../installation/new-installation/setup-command-line>`

-----------------------------------------------------------------------------------------

Improvements and adjustments
----------------------------
Updated components
^^^^^^^^^^^^^^^^^^

The following components have been updated to a new version:

* OXID eShop CE (Update von 6.8.0 auf 7.0.0-rc1), `Changelog 7.0.0-rc1 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.0-rc1/CHANGELOG.md>`_
* OXID eShop PE (Update von 6.5.0 auf 7.0.0-rc1)
* OXID eShop EE (Update von 6.6.0 auf 7.0.0-rc1)
* Theme "Flow" (Update von 3.7.0 auf 4.0.0), `Changelog 4.0.0 <https://github.com/OXID-eSales/flow_theme/blob/v4.0.0/CHANGELOG.md>`_
* Theme "Wave" (Update von 1.6.0 auf 2.0.0), `Changelog 2.0.0 <https://github.com/OXID-eSales/wave-theme/blob/v2.0.0/CHANGELOG.md>`_

* OXID eShop composer plugin (Update von 5.2.0 auf 6.0.0), `Changelog 6.0.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v6.0.0/CHANGELOG.md>`_
* OXID eShop Views Generator (Update von 1.3.0 auf 2.0.0)
* OXID eShop DemoData installer (Update von 1.2.0 auf 2.0.0)
* OXID eShop demodata CE/PE/EE (Update von 6.0.4 auf 7.0.0)
* OXID eShop doctrine migration integration (Update von 3.2.0 auf 4.0.0), `Changelog 4.0.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v4.0.0/CHANGELOG.md>`_
* OXID eShop facts (Update von 2.4.0 auf 3.0.0), `Changelog 3.0.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v3.0.0/CHANGELOG.md>`_
* Unified Namespace Generator (Update von 2.2.0 auf 3.0.0), `Changelog 3.0.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v3.0.0/CHANGELOG.md>`_

Credit card no longer supported as a payment method
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The credit card payment method implemented in OXID eShop is no longer supported. Shop owners who need this payment method should use modules from the appropriate payment providers.

Newsletter sending removed
^^^^^^^^^^^^^^^^^^^^^^^^^^
Newsletters are a fast and easy way to notify online shop customers of current topics, give tips, announce campaigns and promote products. Customers can still subscribe to the newsletter, but the actual sending has been removed from the OXID eShop. In the future, only newsletter services, cloud-based newsletter tools or newsletter software should be used for this. OXID eShop offers the possibility to export a list of newsletter subscribers, which can then be transferred to an external provider. See: :doc:`Newsletter <../../operation/newsletters/newsletters>`

News removed
^^^^^^^^^^^^
Messages could already be accessed with "Flow", default theme since OXID eShop 6.0.0, only via a link in the footer. Now this little-used feature has been completely removed from the shop.

-----------------------------------------------------------------------------------------

Corrections
-----------
No fixes for OXID eShop 7.0.0 RC 1


.. Intern: , Status: transL