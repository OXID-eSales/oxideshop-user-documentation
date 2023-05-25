OXID eShop 7.0.0
================

Release date: 30-05-2023

The most important changes at a glance
---------------------------------------

* OXID eShop 7.0 natively supports the template engine Twig.

  The previously used template engine Smarty is available as an alternative package.

  However, we recommend switching to the new standard Twig as soon as possible.

* MySQL 8, Composer 2.4 and the image format WebP are supported.
* Module handling has been optimized and adapted.

Technologies
------------

* Support for MySQL version 8.0

* Support for Composer version 2.4

* Switching the default template engine from Smarty to Twig

  For more information, see `Twig Template Engine <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/twig_template_engine/index.html>`_.

  Optionally, you can still use Smarty.
  |br|
  For more information, see `Install smarty template engine <https://github.com/OXID-eSales/developer_documentation/update/eshop_from_65_to_7/install_smarty_engine.html>`_.

  .. todo: #tbd Make link: <link to https://github.com/OXID-eSales/developer_documentation/commit/e9bdc830de0de7c828d0e3b293dd5c9edbc5a24b>

* Automatic HTML escaping in the frontend.

  For more information, see the developer documentation under `Check HTML escaping <https://docs.oxid-esales.com/developer/en/latest/update/eshop_from_65_to_7/modules.html#check-html-escaping>`_.

* Support for WebP image format.

  For more information, see :ref:`configuration/images:image generation and quality`.

* Updating Symfony components to version 6.

Improvement of the module system
--------------------------------

Composer
^^^^^^^^

According to the philosophy of Composer, module files are read exclusively from the :file:`vendor/` directory.

When installing modules, the files are no longer automatically copied to the :file:`source/modules/` directory.

For more information, see our developer documentation at `Module skeleton: metadata, composer and structure <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/skeleton/index.html>`_.

YAML files
^^^^^^^^^^

We have adjusted the structure of the configuration files.

For more information, see

* `Modules configuration and setup <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/module_configuration/modules_configuration.html>`_
* `Troubleshooting <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/installation_setup/troubleshooting.html>`_

When updating to version 7, it is therefore necessary that you transfer your custom modules to the new structure.

For more information, see `Check changes in the module handler <https://docs.oxid-esales.com/developer/en/latest/update/eshop_from_65_to_7/modules.html#port-to-v7-module-handler-20221123>`_.

  .. todo: #tbd: URL verif.

Console
^^^^^^^

The commands for handling modules have changed.

For more information, see

* `Best practice Modul-Setup für die Entwicklung mit Composer <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/tutorials/module_setup.html>`_
* `Uninstall modules <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/uninstall/index.html>`_

New functions
-------------

Tracking URL per shipping method
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Store one tracking URL per shipping method.

As soon as the parcel ID (depending on the shipping provider tracking code, parcel label number, parcel reference, shipment number, etc.) has been entered with the order, the tracking link consisting of the tracking URL and the parcel ID of the order will be available.

For more information, see :ref:`Tracking-URL <tracking-url-shipping-method>`.

Setup via command line
^^^^^^^^^^^^^^^^^^^^^^

To simplify the implementation of your project, as an alternative to the web-based setup, you can create and configure your OXID eShop via the command line.

You have the following options on the OXID eShop console:

* Use ``oe:setup:shop`` to create the database and configure your OXID eShop.
  |br|
  You pass the necessary information for this with parameters.

* Install demo data with ``oe:setup:demodata``.
* Create the store administrator with ``oe:admin:create-user``.
* If you have OXID eShop Professional or Enterprise edition, add license keys with ``oe:license:add``.

  It is technically not possible to replace existing license keys with new ones. Therefore, if you replace an existing license key with another one, delete all license keys first with ``oe:license:clear`` and then add the license keys again.

For more information, see :doc:`setup via command line <../../installation/new-installation/setup-command-line>`.

Clean Up
--------

We have removed the following deprecated functions.

Test library
^^^^^^^^^^^^

Use the native PHPUnit and Codeception functionality instead of the test library.

For more information, see the developer documentation under `Testing <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/testing/codeception/index.html>`_.

RSS functionality
^^^^^^^^^^^^^^^^^

The RSS functionality has been dropped.

Login via LDAP
^^^^^^^^^^^^^^

If you have an LDAP environment, you need to implement your own login solution.

Credit card as payment method
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We no longer support the credit card payment method implemented in OXID eShop for security reasons.

Use the module of a payment provider to offer credit card payment to your customers.

Newsletter dispatch
^^^^^^^^^^^^^^^^^^^

We have removed the rudimentary basic newsletter feature for sending a newsletter from OXID eShop.

Customers can still subscribe to newsletters.

To use the data in a professional marketing tool, export the list of your newsletter subscribers in the administration area.

For more information, see :doc:`Newsletters <../../operation/newsletters/newsletters>`.

News
^^^^

With the introduction of the Flow theme (OXID eShop 6.0.0), you could already access news under :menuselection:`Admin --> Customer information --> News` only via a link in the footer.

To present news or offers, we recommend to implement landing pages with Visual CMS (for Professional and Enterprise Edition) in the future.

Encrypted values in the database
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We have removed the native encryption of the store configuration in the :code:`oxconfig` table, because MySQL 8.0 does not support this feature anymore.


Components
----------

Components of the compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The compilation contains the following components:

* `OXID eShop CE 7.0.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.0/CHANGELOG.md>`_
* `OXID eShop PE 7.0.0 <https://github.com/OXID-eSales/oxideshop_pe/blob/v7.0.0/CHANGELOG.md>`_
* `OXID eShop EE 7.0.0 <https://github.com/OXID-eSales/oxideshop_ee/blob/v7.0.0/CHANGELOG.md>`_
* `Apex theme 1.0.0 <https://github.com/OXID-eSales/apex-theme/blob/v1.0.0/CHANGELOG.md>`_
* `Twig theme 2.1.0 <https://github.com/OXID-eSales/twig-theme/blob/v2.1.0/CHANGELOG.md>`_
* `Twig admin theme 2.1.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.1.0/CHANGELOG.md>`_
* `Twig component 2.1.0 <https://github.com/OXID-eSales/twig-component/blob/v2.1.0/CHANGELOG.md>`_

* `OXID eShop composer plugin 7.1.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.1.0/CHANGELOG.md>`_
* `OXID eShop Views Generator 2.1.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.1.0/CHANGELOG.md>`_
* `OXID eShop DemoData installer 3.1.0 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.1.0/CHANGELOG.md>`_
* `OXID eShop demodata CE/PE/EE 8.0.0 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.0/CHANGELOG.md>`_
* `OXID eShop doctrine migration integration 5.1.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.1.0/CHANGELOG.md>`_
* `OXID eShop facts 4.1.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.1.0/CHANGELOG.md>`_
* `Unified Namespace Generator 4.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v4.1.0/CHANGELOG.md>`_

* `GDPR Opt-In 3.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 2.0.2 <https://github.com/OXID-eSales/usercentrics/blob/v2.0.2/CHANGELOG.md>`_
* `WYSIWYG Editor + Media Library 3.0.1 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v3.0.1/CHANGELOG.md>`_
* `Makaira 2.1.0 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.0/CHANGELOG.md>`_


System requirements
^^^^^^^^^^^^^^^^^^^

For the system requirements, see :ref:`installation/new-installation/server-and-system-requirements:Server and system requirements`.

Installation
^^^^^^^^^^^^

To install, follow the instructions under :ref:`installation/index:Installation`.

Corrections
-----------

* https://bugs.oxid-esales.com/changelog_page.php?version_id=344
* https://bugs.oxid-esales.com/changelog_page.php?version_id=630
* https://bugs.oxid-esales.com/changelog_page.php?version_id=728


.. Intern: oxbajt, Status: transL