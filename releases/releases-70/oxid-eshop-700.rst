OXID eShop 7.0.0
================

Release date: 24-05-2023

Features
--------

Security
^^^^^^^^

* Supported MySQL Version: 8.0

  With MySQL 8.0, improve security in particular, but also performance:

  * faster searching and indexing
  * better scalability
  * improved support for NoSQL operations
  * improved support for spatial data
  * improved support for transactions, making development and maintenance easier

  .. note::
     **MySQL 5.7**

     Using MySQL 5.7 is possible, but we recommend MySQL 8.0.


* Supported PHP versions: 8.0 and 8.1

* Supported Composer version: 2.4

  With Composer 2.4, you also have better support for plugins, and it makes it easier to diagnose and deal with error messages.

* Symfony components are updated to Symfony version 6.

* Automatic HTML escaping in the frontend.

  Interpreting certain HTML tags no longer happens centrally in the :code:`Field` class, but automatically in the frontend by the Twig template engine or GraphQL.

  Twig and GraphQL automatically bypass these characters and render them safely. This ensures that no malicious JavaScript code can be executed. Cross-site scripting (XSS) attacks are prevented.

  .. important::

     If you use Smarty or build custom solutions, make sure you have HTML escaping turned on.

     .. todo: #tbd: verify URL: (https://docs.oxid-esales.com/developer/en/7.0-rc.2/update/eshop_from_65_to_7/modules.html#check-html-escaping)

     For more information, see `Check HTML escaping <https://docs.oxid-esales.com/developer/en/latest/update/eshop_from_65_to_7/modules.html#check-html-escaping>`_ in the developer documentation.

* Metadata version 2.0 or higher

  For more information about metadata, see the developer documentation under `metadata.php <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/skeleton/metadataphp/index.html>`_.


Performance
^^^^^^^^^^^

* To increase browser speed, we support the WebP image format.

  Optional: You can automatically convert your images that are in other formats.

  To do this, under :menuselection:`Master Data --> Basic Settings --> System --> Images`, check the :guilabel:`Convert images to WebP format automatically` checkbox.

  See :ref:`configuration/images:image generation and quality`.

Development
^^^^^^^^^^^

* Use Twig, our default template engine. Twig is widely used, well maintained and has a large developer community where you can find support.

  For more information, see `Twig Template Engine <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/twig_template_engine/index.html>`_.

* Not native to Twig, but important if you develop your own modules: Twig template multiple inheritance for modules allows you to quickly change the visual appearance of your OXID eShop without affecting internal business logic and code base. If a module changes, the layout automatically adapts.

  For more information, see `Understanding the OXID eShop template hierarchy and override system <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/theme/theme_template_hierarchy.html>`_.


* The names in the controller templates are independent of the template engine.

  This makes it easier for you to include alternative template engines, for example Smarty.

  Because the Template Engine finds the correct extension automatically.

  Example: Controller::$_sThisTemplate='page/content' instead of 'page/content.tpl'.

Operation
^^^^^^^^^

* To make it easier for you to install, configure and maintain your OXID eShop, we have changed the structure of the OXID eShop configuration file.

  For more information^, see

  * `Modules configuration and setup <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/module_configuration/modules_configuration.html>`_
  * `Troubleshooting <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/installation_setup/troubleshooting.html>`_

* To also make it easier for you to install, configure and run modules, we have changed the module handler so that all module-specific information is stored in YAML files rather than in the database.

  For more information, see `Check changes in the module handler <https://docs.oxid-esales.com/developer/en/latest/update/eshop_from_65_to_7/modules.html#port-to-v7-module-handler-20221123>`_.

  .. todo: #tbd: URL verif.

Modules changes
---------------

Native Composer support for modules
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Files remain in the :file:`/vendor` directory. They are not copied to :file:`/source/modules`.

This makes it easier for you to develop and maintain your own modules and projects.

For more information, see the developer documentation under `Module skeleton: metadata, composer and structure <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/skeleton/index.html>`_.


New functions
-------------

Tracking URL per shipping method
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #tbd: Docu in corresponding chap. erg: :menuselection:`Master data --> Basic settings --> Settings. --> Other settings` :menuselection:`Master Settings --> Core Settings --> Settings --> Other Settings`, :guilabel:`Standard shipping provider tracking URL`

Store one tracking URL per shipping method.

As soon as the parcel ID (depending on the shipping provider the tracking code, parcel label number, parcel reference, shipment number, etc.) has been entered with the order, the tracking link consisting of the tracking URL and the parcel ID of the order will be available.

For more information, see :ref:`Tracking-URL <tracking-url-shipping-method>`.

Setup via command line
^^^^^^^^^^^^^^^^^^^^^^

To simplify the implementation of your project, as an alternative to the web-based setup, you can create and configure your OXID eShop via the command line.

You have the following options on the OXID eShop Console:

* Use ``oe:setup:shop`` to create the database and configure your OXID eShop.
  |br|
  You pass the necessary information for this with parameters.

* Install demo data with ``oe:setup:demodata``.
* Create the store administrator with ``oe:admin:create-user``.
* If you have OXID eShop Professional or Enterprise edition, add license keys with ``oe:license:add``.

  It is technically not possible to replace existing license keys with new ones. Therefore, if you replace an existing license key with another one, delete all license keys first with ``oe:license:clear`` and then add the license keys again.

For more information see :doc:`Setup via command line <../../installation/new-installation/setup-command-line>`.

Module installation via command line
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Install or uninstall modules using the new OXID eShop Console commands ``oe:module:install`` and ``oe:module:uninstall``.

For more information, see the developer documentation under

.. todo: #tbd: Verify URLs.
        * https://docs.oxid-esales.com/developer/en/7.0-rc.1/development/modules_components_themes/module/tutorials/module_setup.html
        * https://docs.oxid-esales.com/developer/en/7.0-rc.1/development/modules_components_themes/module/uninstall/index.html.

* `Best practice module setup for development with composer <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/tutorials/module_setup.html>`_
* `Uninstall modules <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/uninstall/index.html>`_

Streamlining
------------

We have removed the following technically obsolete functionalities:

Test Library
^^^^^^^^^^^^

Use the native PHPUnit and Codeception functionality instead of the test library.

For more information, see the developer documentation under `Testing <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/testing/codeception/index.html>`_.

RSS functionality
^^^^^^^^^^^^^^^^^^

The RSS functionality has been dropped.

Login via LDAP
^^^^^^^^^^^^^^

If you have an LDAP environment, you need to implement a custom login solution.

Credit card as payment method
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

For security reasons, we no longer support the credit card payment method implemented in OXID eShop.

To offer credit card payment to your customers, use a payment provider module.

Newsletter dispatch
^^^^^^^^^^^^^^^^^^^

We have removed the rudimentary basic newsletter feature for sending a newsletter from the OXID eShop.

Customers can still subscribe to newsletters.

To use the data in a professional marketing tool, export the list of your newsletter subscribers.

For more information, see :doc:`Newsletters <../../operation/newsletters/newsletters>`.

News removed
^^^^^^^^^^^^

With the introduction of the Flow theme (OXID eShop 6.0.0), you could already access news under :menuselection:`Admin --> Customer Information --> News` only via a link in the footer.

To present news or offers, we recommend to implement landing pages with Visual CMS (for Professional and Enterprise Edition).

Encrypted values in the database
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We removed the native encryption of the store configuration in the :code:`oxconfig` table, because MySQL 8.0 does not support this feature anymore.

Module information is stored in separate YAML files and can be encrypted individually by module.

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