OXID eShop 7.0.3
================

Release date: 26-03-2024

Corrections
-----------

* Dedicated template cache for subshops in the :productname:`OXID eShop Enterprise Edition`

  Description: In the :productname:`OXID eShop Enterprise Edition` subshops could overwrite the template cache.

  This behavior happened if main and subshops had different module installations with their own templates. In a scenario in which a subshop had activated a module and built up its template cache, the main shop was able to determine that the corresponding module was not active when accessing the same cache. This resulted in the eShop being put into maintenance mode.

  Solution: With this update, we ensure that subshops use a separate template cache. This change prevents the described behavior by ensuring that differences in module installations and templates used between main and subshops do not cause conflicts in the template cache. This ensures a more stable and reliable operating environment for eShops with multiple subshops.

  We recommend all operators of the :productname:`OXID eShop Enterprise Edition` to implement this update to optimize the integrity and performance of their eShops.

* Performance improvement: Load module extension chains from the cache

  Description: When modules are installed in the OXID eShop, the class chain for these modules was constructed from YAML files. This process caused performance losses because reading YAML files is slower than accessing cached data.

  Solution: We improved module extension chain loading by pulling them directly from the cache, not YAML files. This improves the eShop's performance as accessing the cache is faster and more efficient. The class chains for modules are now stored in the cache when they are first created and loaded from there when required. This reduces load times and improves the general user experience in the eShop.

  Advantage: This optimization leads to an acceleration of the eShops.

  We recommend that all shop owners implement this update in order to benefit from the performance improvements.

Cleaning up outdated services and methods
-----------------------------------------

Certain services and methods are outdated. We have replaced them with more powerful and modern alternatives.

So, in our ongoing optimizations, we removed these components:

* :code:`TemplateCacheServiceInterface`: This service is now obsolete, we have replaced it with newer caching mechanisms.
* :code:`BasicContextInterface::getTemplateCacheDirectory()`: This method is no longer needed as the template cache is now managed via improved methods.

This cleanup improves our code's maintainability and boosts the OXID eShop's performance.

Updates and optimizations in detail
-----------------------------------

Find the changes to the compilation in the metapackage under `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v7.0.2...v7.0.3>`_.

Find the corrections in the `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.4/CHANGELOG-7.0.md>`_.

Updated components
^^^^^^^^^^^^^^^^^^

We have updated the following components and modules:

* OXID eShop CE (update from 7.0.3 to 7.0.4): `Changelog 7.0.4 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.4/CHANGELOG-7.0.md>`_

Components of the compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The compilation contains the following components:

* `OXID eShop CE 7.0.4 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.4/CHANGELOG-7.0.md>`_
* `OXID eShop PE 7.0.0 <https://github.com/OXID-eSales/oxideshop_pe/blob/v7.0.0/CHANGELOG.md>`_
* `OXID eShop EE 7.0.1 <https://github.com/OXID-eSales/oxideshop_ee/blob/v7.0.1/CHANGELOG.md>`_
* `Apex theme 1.2.1 <https://github.com/OXID-eSales/apex-theme/blob/v1.2.1/CHANGELOG.md>`_
* `Twig admin theme 2.3.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.3.0/CHANGELOG.md>`_
* `Twig component CE 2.3.0 <https://github.com/OXID-eSales/twig-component/blob/v2.3.0/CHANGELOG.md>`_
* `Twig component PE 2.3.0 <https://github.com/OXID-eSales/twig-component-pe/blob/v2.3.0/CHANGELOG.md>`_
* `Twig component EE 2.3.0 <https://github.com/OXID-eSales/twig-component-ee/blob/v2.3.0/CHANGELOG.md>`_

* `OXID eShop composer plugin 7.1.1 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.1.1/CHANGELOG.md>`_
* `OXID eShop Views Generator 2.1.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.1.0/CHANGELOG.md>`_
* `OXID eShop demo data installer 3.1.1 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.1.1/CHANGELOG.md>`_
* `OXID eShop demo data CE/PE 8.0.1 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.1/CHANGELOG.md>`_
* `OXID eShop demo data EE 8.0.2 <https://github.com/OXID-eSales/oxideshop_demodata_ee/blob/v8.0.2/CHANGELOG.md>`_
* `OXID eShop doctrine migration integration 5.1.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.1.0/CHANGELOG.md>`_
* `OXID eShop facts 4.1.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.1.0/CHANGELOG.md>`_
* `Unified Namespace Generator 4.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v4.1.0/CHANGELOG.md>`_

* `GDPR Opt-In 3.0.1 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v3.0.1/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 2.0.2 <https://github.com/OXID-eSales/usercentrics/blob/v2.0.2/CHANGELOG.md>`_
* `Visual CMS 4.0.2 <https://github.com/OXID-eSales/visual_cms_module/blob/v4.0.2/CHANGELOG-4.0.md>`_ (PE/EE)
* `WYSIWYG Editor + Media Library 3.0.2 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v3.0.2/CHANGELOG.md>`_
* `Makaira 2.1.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.2/CHANGELOG.md>`_

Installation
------------

To install or update, follow the instructions in the *Installation* section:

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing a patch update <../../installation/update/patch-update>`

.. Intern: , Status: