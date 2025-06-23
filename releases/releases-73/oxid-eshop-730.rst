OXID eShop Compilation 7.3.0
============================

Release date: 17-06-2025

What's New
----------

PHP Support
^^^^^^^^^^^

Support for PHP 8.2, 8.3 and 8.4

.. hint::
  Please note changes in floating-point rounding behavior in PHP 8.4 which may result in different calculation outcomes compared to PHP 8.2 and 8.3.
  
For more information, see `Server and System Requirements <https://docs.oxid-esales.com/eshop/en/7.3/installation/new-installation/server-and-system-requirements.html#php>`_.

Controller Management
^^^^^^^^^^^^^^^^^^^^^

For easier handling, better testability and more flexible controller extensions, alternatively register new OXID controllers as services.

For more information, see `Controller as a service <https://docs.oxid-esales.com/developer/en/7.3/development/tell_me_about/controller_as_service.html>`_ in the developer documentation.

Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Use a `.env` file to define environment variables and securely integrate them into your OXID eShop application, making it easier to manage sensitive configuration values and environment-specific settings.

For more information, see `Environment variables <https://docs.oxid-esales.com/developer/en/7.3/development/modules_components_themes/project/environment.html>`_ in the developer documentation.


Fixes
-----

* Shop ID resolution now considers SSL language URLs
* Email existence check when switching from customer to guest account `#0006860 <https://bugs.oxid-esales.com/view.php?id=6860>`_
* Shipping cost calculation corrected after login in cart and checkout `#0007682 <https://bugs.oxid-esales.com/view.php?id=7682>`_
* Resolved issues when adding a fifth language to the shop `#0007683 <https://bugs.oxid-esales.com/view.php?id=7683>`_
* Correct order totals display in admin when using a non-default base currency `#0005922 <https://bugs.oxid-esales.com/view.php?id=5922>`_
* Exception handling if a product is deleted while it is in someone's cart `#0007391 <https://bugs.oxid-esales.com/view.php?id=7391>`_
* Improved module file cache under heavy load
* "Add to basket" now forces refresh of the order confirmation step `#0007254 <https://bugs.oxid-esales.com/view.php?id=7254>`_

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
* Visual CMS from v7.0.3 to v8.0.1 `Changelog file <https://github.com/OXID-eSales/visual_cms_module/blob/v8.0.1/CHANGELOG-8.x.md>`_
* OXID eShop PE from v7.2.0 to v7.3.0 `Changelog file <https://github.com/OXID-eSales/oxideshop_pe/blob/v7.3.0/CHANGELOG-7.3.md>`_
* OXID eShop demodata EE from v8.0.3 to v8.1.0 `Changelog file <https://github.com/OXID-eSales/oxideshop_demodata_ee/blob/v8.1.0/CHANGELOG.md>`_
* OXID eShop EE from v7.2.0 to v7.3.0 `Changelog file <https://github.com/OXID-eSales/oxideshop_ee/blob/v7.3.0/CHANGELOG-7.3.md>`_

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

Compatible Modules
------------------

For an overview of the related OXID modules, see :doc:`OXID eShop 7.3.0 compatible modules <oxid-eshop-730-modules>`.
