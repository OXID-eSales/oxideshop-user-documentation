OXID eShop 7.0.0 RC 1
=====================

Release date RC 1: 21.07.2021

-----------------------------------------------------------------------------------------

General information
-------------------
OXID eShop 7.0.0 RC 1 is provided as a compilation with the following components:

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

* OXID eShop 7.0.0 RC 1 runs under PHP 7.4 and 8.0
* MySQL version 5.7 and 8.0 as well as MariaDB version 10.4 are supported as database
* Apache 2.2 or 2.4 can be used as a web server on a Linux system
* Composer is supported in versions 1 and 2
* Metadata is supported in versions 2.0 and 2.1

Installation
^^^^^^^^^^^^
Please follow the instructions in section "Installation":

:doc:`New installation <../../installation/new-installation/new-installation>`

It is not recommended to update OXID eShop to version 7.0.0 RC 1. Update instructions will be available with the release of the final version.

-----------------------------------------------------------------------------------------

New functions
-------------
Setup via command line
^^^^^^^^^^^^^^^^^^^^^^
To complement the web-based setup, OXID eShop can now also be created and configured via the command line. The new command of the OXID eShop console ``oe:setup:store`` creates the database and configures the shop. The necessary information is transferred with parameters. In further steps demo data can be installed with ``oe:setup:demodata`` and the shop administrator can be created with ``oe:admin:create-user``. For OXID eShop Professional and Enterprise Edition, the ``oe:license:add`` command adds a valid license key. See: :doc:`Setup via command line <../../installation/new-installation/setup-command-line>`

Module installation via command line
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Modules can be installed and uninstalled using the new OXID eShop console ``oe:module:install`` and ``oe:module:uninstall`` commands. All information about this can be found in the developer documentation: https://docs.oxid-esales.com/developer/en/7.0-rc.1/development/modules_components_themes/module/tutorials/module_setup.html and https://docs.oxid-esales.com/developer/en/7.0-rc.1/development/modules_components_themes/module/uninstall/index.html.

-----------------------------------------------------------------------------------------

Improvements and adjustments
----------------------------
Updated components
^^^^^^^^^^^^^^^^^^
The following components have been updated to a new version:

* OXID eShop CE (Update von 6.8.0 auf 7.0.0-rc1), `Changelog 7.0.0-rc1 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.0-rc1/CHANGELOG.md>`_
* OXID eShop PE (Update von 6.5.0 auf 7.0.0-rc1)
* OXID eShop EE (Update von 6.6.0 auf 7.0.0-rc1)
* Theme "Flow" (Update von 3.7.0 auf 4.0.0), `Changelog Flow 4.0.0 <https://github.com/OXID-eSales/flow_theme/blob/v4.0.0/CHANGELOG.md>`_
* Theme "Wave" (Update von 1.6.0 auf 2.0.0), `Changelog 2.0.0 <https://github.com/OXID-eSales/wave-theme/blob/v2.0.0/CHANGELOG.md>`_
* OXID eShop composer plugin (Update von 5.2.0 auf 6.0.0), `Changelog 6.0.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v6.0.0/CHANGELOG.md>`_
* OXID eShop Views Generator (Update von 1.3.0 auf 2.0.0)
* OXID eShop DemoData installer (Update von 1.2.0 auf 2.0.0)
* OXID eShop demodata CE/PE/EE (Update von 6.0.4 auf 7.0.0)
* OXID eShop doctrine migration integration (Update von 3.2.0 auf 4.0.0), `Changelog 4.0.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v4.0.0/CHANGELOG.md>`_
* OXID eShop facts (Update von 2.4.0 auf 3.0.0), `Changelog OXID eShop facts 3.0.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v3.0.0/CHANGELOG.md>`_
* Unified Namespace Generator (Update von 2.2.0 auf 3.0.0), `Changelog 3.0.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v3.0.0/CHANGELOG.md>`_

Tracking URL per shipping method
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Until now, one tracking URL could be defined per shop. It is entered in the Admin panel under :menuselection:`Master Settings --> Core Settings --> Settings --> Other settings`. This tracking URL is now the default tracking URL and can be replaced with a custom tracking URL per shipping method.

As soon as the package ID (depending on the shipping service provider tracking code, parcel label number, package reference, shipment number, etc.) is entered with the order, the tracking link, consisting of the tracking URL and the package ID of the order, is available. It will be sent to the customer as a tracking link in the e-mail informing him/her of the shipment. The tracking link is also displayed in the customer's order history in the frontend.

Credit card no longer supported as a payment method
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The credit card payment method implemented in OXID eShop is no longer supported. Shop owners who need this payment method should use modules from the appropriate payment providers.

Newsletter sending removed
^^^^^^^^^^^^^^^^^^^^^^^^^^
Newsletters are a fast and easy way to notify online shop customers of current topics, give tips, announce campaigns and promote products. Customers can still subscribe to the newsletter, but the actual sending has been removed from the OXID eShop. In the future, only newsletter services, cloud-based newsletter tools or newsletter software should be used for this. OXID eShop offers the possibility to export a list of newsletter subscribers, which can then be transferred to an external provider. See: :doc:`Newsletter <../../operation/newsletters/newsletters>`

News removed
^^^^^^^^^^^^
Messages could already be accessed with "Flow", default theme since OXID eShop 6.0.0, only via a link in the footer. Now this little-used feature has been completely removed from the shop.

Modules changes
^^^^^^^^^^^^^^^

* Native Composer support for modules: Files remain entirely in the :file:`/vendor` directory. They are not copied to :file:`/source/modules`.
* Caching for module assets, the static files required by modules in the frontend (CSS, JavaScript or image files), has been optimized. See: https://github.com/OXID-eSales/oxideshop_ce/pull/493

No encoded values in database
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Encoding of database values has been removed as functionality is no longer supported by MySQL 8.0.

-----------------------------------------------------------------------------------------

Corrections
-----------
Corrections 7.0.0 RC 1: https://bugs.oxid-esales.com/changelog_page.php?version_id=344


.. Intern: oxbajt, Status: transL