OXID eShop Compilation 7.3.0
============================

Release date: 17-06-2025

New
---

PHP Support
^^^^^^^^^^^

Support for PHP 8.2, 8.3 and 8.4.

.. hint::
  Please note changes in floating-point rounding behavior in PHP 8.4 which may result in different calculation outcomes compared to PHP 8.2 and 8.3.
  
For more information, see `Server and System Requirements <https://docs.oxid-esales.com/eshop/en/7.3/installation/new-installation/server-and-system-requirements.html#php>`_.

Controller Management
^^^^^^^^^^^^^^^^^^^^^

For easier handling, better testability and more flexible controller extensions, alternatively register new OXID controllers as services.

For more information, see `Controller as a Service <https://docs.oxid-esales.com/developer/en/7.3/development/tell_me_about/controller_as_service.html>`_ in the developer documentation.

Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Use a `.env` file to define environment variables and securely integrate them into your OXID eShop application, making it easier to manage sensitive configuration values and environment-specific settings.

For more information, see `Environment Variables <https://docs.oxid-esales.com/developer/en/7.3/development/modules_components_themes/project/environment.html>`_ in the developer documentation.

Fixes
-----

* #0005922 Affection of currency list order on total order sum: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=5922>`_
* #0006860 Email existence check when switching from guest to customer account: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=6860>`_
* #0007254 Order confirmation handling when adding something to basket: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7254>`_
* #0007391 Exception handling if a product is deleted while in shopping cart: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7391>`_
* #0007682 Shipping cost calculation after login in shopping cart or checkout: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7682>`_
* #0007683 Adding a fifth language: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7683>`_
* #0007803 SSL configuration usage on shop ID calculation from language URL: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7803>`_
* #0007804 Module file cache performance under heavy load: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7804>`_

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

Compatible OXID Extensions
--------------------------

* OXAPI GraphQL Base Module 11.0: `Documentation <https://docs.oxid-esales.com/interfaces/graphql/en/11.0/>`_
* OXAPI GraphQL Configuration Access Module 2.1: `Documentation <https://docs.oxid-esales.com/interfaces/graphql/en/11.0/>`_
* OXAPI GraphQL Storefront Module 4.1: `Documentation <https://docs.oxid-esales.com/interfaces/graphql/en/11.0/>`_
* OXID ERP Interface 4.2: `Documentation <https://docs.oxid-esales.com/interfaces/erp/en/4.2>`_
* [NEW] OXID eShop Admin Tools 1.0: `Documentation <https://docs.oxid-esales.com/modules/admin-tools/en/1.0/>`_
* [NEW] OXID eShop Consistency Check Tool 1.0: `Documentation <https://github.com/OXID-eSales/consistency-check-tool/tree/v1.0.0>`_
* OXID eShop Country VAT Administration 2.3: `Documentation <https://github.com/OXID-eSales/country-vat-module/blob/v2.3.0/README.md>`_
* OXID eShop Geo-Blocking Module 2.3: `Documentation <https://docs.oxid-esales.com/modules/geo-blocking/en/2.3>`_
* [NEW] OXID eShop Security Module 2.0: `Documentation <https://docs.oxid-esales.com/modules/security/de/2.0/releases/security-module-200.html>`_
* OXID eShop Shipping Cost Compensation Module 1.1: `Documentation <https://docs.oxid-esales.com/modules/freeshipping-coupons/en/1.1/introduction.html>`_
* OXID eShop eVAT Module 4.2: `Documentation <https://docs.oxid-esales.com/modules/vat-tbe-services/en/4.2>`_

OXID eShop Enterprise B2B Edition 7.3
-------------------------------------
.. todo: move to other section/page:

Allow the the chief buyer to set a secondary limit to allow buyers to place smaller orders directly without requiring approval, thereby reducing your workload.

.. todo: #tbd: Verify URLs:

For more information, see `OXID eShop Enterprise B2B Edition <https://docs.oxid-esales.com/b2b/de/7.3/releases/b2b-edition-730.html>`_ documentation.

Installation
------------

To install or update, follow the instructions at :doc:`Installation <../../installation/index>`.
