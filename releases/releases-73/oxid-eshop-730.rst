OXID eShop 7.3.0
================

.. todo: #HR: Release date: tbd


Changes at a glance
-------------------

.. todo: #HR/#DK: check the following draft, items as per changelog https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.3.x-release/CHANGELOG-7.3.md

Core
^^^^

* Support for PHP 8.4 and PHPUnit 11
* Registration of environment variables via `.env` file
* Controllers can now be registered as dependency injection services
* Raised the minimum required version of Symfony components to 6.4
* Default value of blSkipDebitOldBankInfo set to true


New and updated modules
^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: OXDEV-9193 (Cache clear button)?

* Install the new OXID Admin Tools Module to manually clear the template cache by klicking a button in the admin backend.

  .. todo: #tbd: add URL:

  For more information, see `OXID Admin Tools Module <https://docs.oxid-esales.com/###tbd###/de/1.0/introduction.html>`_ documentation.

  .. todo: #HR: Add new features in :productname:`OXID Security Module`: v2.0 = OXDEV-8930 CAPTCHA)

* :productname:`OXID Security Module` 2.0

  With CAPTCHA protection, secure your OXID eShop form areas against automated bot attacks.

  .. todo: #tbd: Verify URLs:

  For more information, see `OXID Security Module <https://docs.oxid-esales.com/modules/security/de/2.0/releases/security-module-200.html>`_ documentation.

* :productname:`OXID eShop Enterprise B2B Edition` 7.3

  For more information, see `OXID eShop Enterprise B2B Edition <https://docs.oxid-esales.com/b2b/de/7.3/releases/b2b-edition-730.html>`_ documentation.

  .. todo: #tbd: Add URLs:

* The following modules have been updated to be compatible with OXID eShop 7.3:

  * :productname:`OXID Module Shipping Cost Compensation` `1.1 <https://docs.oxid-esales.com/modules/freeshipping-coupons/en/1.1/introduction.html>`_
  * :productname:`OXID eShop eVAT`: `4.2 <https://docs.oxid-esales.com/modules/vat-tbe-services/en/4.2>`_
  * :productname:`OXID ERP Interface`: `4.2 <https://docs.oxid-esales.com/interfaces/erp/en/4.2>`_
  * :productname:`OXID Cookie Management powered by usercentrics`: `3.1 (German) <https://docs.oxid-esales.com/modules/usercentrics/de/3.1/>`_
  * :productname:`GDPR Opt-in`: `4.2 (German) <https://docs.oxid-esales.com/modules/gdpr-optin/de/4.2/>`_
  * :productname:`Geo-blocking`: `2.3 <https://docs.oxid-esales.com/modules/geo-blocking/en/2.3>`_
  * :productname:`Visual CMS`: 7.3



Fixes
-----

`#0007683 <https://bugs.oxid-esales.com/view.php?id=7683>`_
.. todo: #HR/#DK: check: the following as per https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.3.x/CHANGELOG-7.3.md#fixed

* Shop ID resolution now considers SSL language URLs
* Email existence check when switching from customer to guest account `#0006860 <https://bugs.oxid-esales.com/view.php?id=6860>`_
* Shipping cost calculation corrected after login in cart and checkout `#0007682 <https://bugs.oxid-esales.com/view.php?id=7682>`_
* Correct order totals display in admin when using a non-default base currency `#0005922 <https://bugs.oxid-esales.com/view.php?id=5922>`_
* Exception handling if a product is deleted while it is in someone's cart `#0007391 <https://bugs.oxid-esales.com/view.php?id=7391>`_
* Improved module file cache under heavy load
* Fixed class loading error after module removal
* "Add to basket" no longer forces refresh of the order confirmation step `#0007254 <https://bugs.oxid-esales.com/view.php?id=7254>`_


In detail
---------

Visual CMS & Media Library
^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #HR/#MF: Will more info be added?

See changelogs:

* Visual CMS: https://github.com/OXID-eSales/visual_cms_module/blob/b-7.3.x/CHANGELOG-7.x.md
* Media Library: https://github.com/OXID-eSales/media-library-module/blob/b-7.3.x/CHANGELOG.md
* WYSIWYG Editor: https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/b-7.3.x/CHANGELOG.md

New features for developers
^^^^^^^^^^^^^^^^^^^^^^^^^^^

  .. todo: #DK: check: PHP v8.4 support:

* Leverage full compatibility with PHP 8.2 to 8.4.

  The software supports PHP versions up to and including PHP 8.4. However, note changes in floating-point rounding behavior in PHP 8.4, which may result in different calculation outcomes compared to PHP 8.3.

  .. todo: #tbd: verify URLs:

  For more information, see the `Server and System Requirements <https://docs.oxid-esales.com/eshop/de/7.3/installation/new-installation/server-and-system-requirements.html>`_ under `PHP <https://docs.oxid-esales.com/eshop/de/7.3/installation/new-installation/server-and-system-requirements.rst.html#php>`_.

  .. todo: #DK: check: Missing in changelog https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.3.x-release/CHANGELOG-7.3.md ?

* Improve template security with the Twig Sandbox Extension.

  Use the Twig Sandbox Extension with the {% sandbox %} tag to control which tags, filters, and functions are allowed in your templates, enhancing the security of dynamic template rendering.

  .. todo: #tbd: verify link

  For more information, see the developer documentation (English) under `Using the Twig Sandbox Extension <https://docs.oxid-esales.com/developer/en/7.3/development/modules_components_themes/theme/twig_sandbox.html>`_.

  .. todo: #DK: check: Controllers can be registered as DI services

* Optimize OXID controller management.

  Register OXID controllers as services in the Dependency Injection Container (DIC) for easier handling, better testability, and more flexible controller extension.

  .. todo: #tbd: verify link

  For more information, see the developer documentation (English) under `Controller as a service <https://docs.oxid-esales.com/developer/en/7.3/development/tell_me_about/controller_as_service.html>`_.

  .. todo: #DK: check: Registration of environment variables via .env file

* Simplify environment variable management.

  Use a `.env` file to define environment variables and securely integrate them into your OXID eShop application, making it easier to manage sensitive configuration values and environment-specific settings.

  .. todo: #tbd: verify link

  For more information, see the developer documentation (English) under `Environment variables <https://docs.oxid-esales.com/developer/en/7.3/development/modules_components_themes/project/environment.html>`_.

Components
----------

Updated components
^^^^^^^^^^^^^^^^^^

We have updated the following components and modules:

* WYSIWYG Editor + Mediathek from v4.2.0 to v5.0.0 `Changelog file <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v5.0.0/CHANGELOG.md>`__
* APEX Theme from v2.0.0 to v2.1.0 `Changelog file <https://github.com/OXID-eSales/apex-theme/blob/v2.1.0/CHANGELOG-2.x.md>`__
* GDPR opt-in module from v4.1.0 to v4.2.0 `Changelog file <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.2.0/CHANGELOG.md>`__
* Media Library Module from v2.1.1 to v3.0.0 `Changelog file <https://github.com/OXID-eSales/media-library-module/blob/v3.0.0/CHANGELOG.md>`__
* OXID eShop CE from v7.2.0 to v7.3.0 `Changelog file <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.3.0/CHANGELOG-7.3.md>`__
* OXID eShop composer plugin from v7.2.0 to v7.3.0 `Changelog file <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.3.0/CHANGELOG-7.x.md>`__
* OXID eShop doctrine migration integration from v5.3.0 to v5.4.0 `Changelog file <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.4.0/CHANGELOG-5.x.md>`__
* OXID eShop facts from v4.2.0 to v4.3.0 `Changelog file <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.3.0/CHANGELOG-4.x.md>`__
* Unified Namespace Generator from v5.1.0 to v5.2.0 `Changelog file <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.2.0/CHANGELOG.md>`__
* Twig Admin Theme from v2.5.0 to v2.6.1 `Changelog file <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.6.1/CHANGELOG-2.x.md>`__
* Twig component from v2.5.0 to v2.6.0 `Changelog file <https://github.com/OXID-eSales/twig-component/blob/v2.6.0/CHANGELOG-2.x.md>`__
* OXID Cookie Management powered by usercentrics from v3.0.0 to v3.1.0 `Changelog file <https://github.com/OXID-eSales/usercentrics/blob/v3.1.0/CHANGELOG.md>`__
* Visual CMS from v7.0.3 to v8.0.1
* OXID eShop PE from v7.2.0 to v7.3.0
* OXID eShop demodata EE from v8.0.3 to v8.1.0
* OXID eShop EE from v7.2.0 to v7.3.0

Compilation components
^^^^^^^^^^^^^^^^^^^^^^

The compilation includes the following components:

* `OXID eShop CE 7.3.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.3.0/CHANGELOG-7.3.md>`_
* OXID eShop PE 7.3.0
* OXID eShop EE 7.3.0

* `Apex theme 2.1.0 <https://github.com/OXID-eSales/apex-theme/blob/v2.1.0/CHANGELOG-2.x.md>`_

* `Twig admin theme 2.6.1 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.6.1/CHANGELOG-2.x.md>`_
* `Twig component CE 2.6.0 <https://github.com/OXID-eSales/twig-component/blob/v2.6.0/CHANGELOG-2.x.md>`_
* Twig component PE 2.6.0
* Twig component EE 2.6.0

* `OXID eShop composer plugin 7.3.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.3.0/CHANGELOG-7.x.md>`_
* `OXID eShop Views Generator 2.2.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* `OXID eShop demo data installer 3.3.0 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_

* `OXID eShop demo data CE 8.0.2 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.2/CHANGELOG.md>`_
* OXID eShop demo data PE 8.0.2
* OXID eShop demo data EE 8.1.0

* `OXID eShop doctrine migration integration 5.4.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.4.0/CHANGELOG-5.x.md>`_
* `OXID eShop facts 4.3.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.3.0/CHANGELOG-4.x.md>`_
* `Unified Namespace Generator 5.2.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.2.0/CHANGELOG.md>`_

* `GDPR Opt-In 4.2.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.2.0/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 3.1.0 <https://github.com/OXID-eSales/usercentrics/blob/v3.1.0/CHANGELOG.md>`_
* Visual CMS 8.0.1 (PE/EE)

* `WYSIWYG Editor 5.0.0 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v5.0.0/CHANGELOG.md>`_
* `Media Library 3.0.0 <https://github.com/OXID-eSales/media-library-module/blob/v3.0.0/CHANGELOG.md>`_
* `Makaira 2.1.3 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.3/CHANGELOG.md>`_
* `Eye-Able 3.0.3 <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/blob/v3.0.3/CHANGELOG.md>`_

Installation
------------

To install or update, follow the instructions at :doc:`Installation <../../installation/index>`.
