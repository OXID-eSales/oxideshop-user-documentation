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

* SSL configuration usage on shop ID calculation from language URL: `#0007803 <https://bugs.oxid-esales.com/view.php?id=7803>`_
* Email existence check when switching from guest to customer account: `#0006860 <https://bugs.oxid-esales.com/view.php?id=6860>`_
* Shipping cost calculation after login in shopping cart or checkout: `#0007682 <https://bugs.oxid-esales.com/view.php?id=7682>`_
* Adding a fifth language: `#0007683 <https://bugs.oxid-esales.com/view.php?id=7683>`_
* Affection of currency list order on total order sum: `#0005922 <https://bugs.oxid-esales.com/view.php?id=5922>`_
* Exception handling if a product is deleted while it's in someone's shopping cart: `#0007391 <https://bugs.oxid-esales.com/view.php?id=7391>`_
* Order confirmation handling when adding something to basket: `#0007254 <https://bugs.oxid-esales.com/view.php?id=7254>`_
* Module file cache performance under heavy load: `#0007804 <https://bugs.oxid-esales.com/view.php?id=7804>`_

Packages
--------

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop CE compilation includes the following packages:

* APEX Theme from v2.0.0 to v2.1.0: `Changelog <https://github.com/OXID-eSales/apex-theme/blob/v2.1.0/CHANGELOG-2.x.md>`_
* Eye-Able Assist v3.0.3: `Changelog <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/blob/v3.0.3/CHANGELOG.md>`_
* GDPR Opt-In Module from v4.1.0 to v4.2.0: `Changelog <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.2.0/CHANGELOG.md>`_
* Makaira Connect Essential 2.1.3: `Changelog <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.3/CHANGELOG.md>`_
* Media Library Module from v2.1.1 to v3.0.0: `Changelog <https://github.com/OXID-eSales/media-library-module/blob/v3.0.0/CHANGELOG.md>`_
* OXID Cookie Management powered by Usercentrics from v3.0.0 to v3.1.0: `Changelog <https://github.com/OXID-eSales/usercentrics/blob/v3.1.0/CHANGELOG.md>`_
* OXID eShop CE from v7.2.0 to v7.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.3.0/CHANGELOG-7.3.md>`_
* OXID eShop Composer Plugin from v7.2.0 to v7.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.3.0/CHANGELOG-7.x.md>`_
* OXID eShop Demodata CE v8.0.2: `Changelog <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.2/CHANGELOG.md>`_
* OXID eShop Demodata Installer v3.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_
* OXID eShop Doctrine Migration Wrapper from v5.3.0 to v5.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.4.0/CHANGELOG-5.x.md>`_
* OXID eShop Facts from v4.2.0 to v4.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.3.0/CHANGELOG-4.x.md>`_
* OXID eShop Unified Namespace Generator from v5.1.0 to v5.2.0: `Changelog <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.2.0/CHANGELOG.md>`_
* OXID eShop Views Generator v2.2.0: `Changelog <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* Twig Admin Theme from v2.5.0 to v2.6.1: `Changelog <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.6.1/CHANGELOG-2.x.md>`_
* Twig Component from v2.5.0 to v2.6.0: `Changelog <https://github.com/OXID-eSales/twig-component/blob/v2.6.0/CHANGELOG-2.x.md>`_
* WYSIWYG Editor Module from v4.2.0 to v5.0.0: `Changelog <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v5.0.0/CHANGELOG.md>`_

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop PE compilation includes the following packages additionally:

* OXID eShop Demodata PE v8.0.2: `Changelog <https://github.com/OXID-eSales/oxideshop_demodata_pe/blob/v8.0.2/CHANGELOG.md>`_
* OXID eShop PE from v7.2.0 to v7.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop_pe/blob/v7.3.0/CHANGELOG-7.3.md>`_
* Twig Component PE v2.5.0: `Changelog <https://github.com/OXID-eSales/twig-component-pe/blob/v2.5.0/CHANGELOG-2.x.md>`_
* Visual CMS Module from v7.0.3 to v8.0.1: `Changelog <https://github.com/OXID-eSales/visual_cms_module/blob/v8.0.1/CHANGELOG-8.x.md>`_

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop EE compilation includes the following packages additionally:

* OXID eShop Demodata EE from v8.0.3 to v8.1.0: `Changelog <https://github.com/OXID-eSales/oxideshop_demodata_ee/blob/v8.1.0/CHANGELOG.md>`_
* OXID eShop EE from v7.2.0 to v7.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop_ee/blob/v7.3.0/CHANGELOG-7.3.md>`_
* Twig Component EE v2.5.0: `Changelog <https://github.com/OXID-eSales/twig-component-ee/tree/v2.5.0>`_

Installation
------------

To install or update, follow the instructions at :doc:`Installation <../../installation/index>`.

Compatible Modules
------------------

For an overview of the related OXID modules, see :doc:`OXID eShop 7.3.0 compatible modules <oxid-eshop-730-modules>`.
