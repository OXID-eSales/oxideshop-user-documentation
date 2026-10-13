OXID eShop Compilation 7.6.0
============================

Release date: TBD

.. todo: release date

.. note::

   OXID eShop 7.6 continues to support **PHP 8.3, 8.4 and 8.5** (minimum version PHP 8.3);
   the PHP version range remains unchanged compared to 7.5.

Highlights
----------

Content & Media Bundle 12
^^^^^^^^^^^^^^^^^^^^^^^^^^

With OXID eShop 7.6, the new **Content & Media Bundle 12** is preinstalled. It consists of
the following components:

* **Media Library 6**
* **WYSIWYG Editor 8**
* **Visual CMS 12** (Enterprise and Professional Edition only)

* **Visual CMS 12 - Dynamic Blocks (central new feature):** With Dynamic Blocks, CMS
  content can be displayed at defined positions in the theme ("blocks"). Which content
  appears at a block is assigned in the admin area - without editing the template; the
  deciding factor is the **context** of the assignment: global or bound to a specific
  product, category or manufacturer; specific assignments take precedence over general
  ones. Within the block, the familiar Visual CMS visibility controls continue to apply -
  **time-based** (date and time, per row/widget) and **device-specific** (visibility per
  screen size, per widget).

  This way, a promotional banner can appear, for example, only on a specific category
  page, and individual elements within it only during a promotion period or only on
  certain devices. Four blocks (before and after the header and footer) are preconfigured;
  additional blocks can be set up. The feature is disabled by default and is enabled in
  the module settings. For detailed instructions and examples, see the Visual CMS
  documentation.
* **Visual CMS 12 - custom styles now as SCSS:** custom styles in CMS content are
  interpreted as **SCSS** instead of LESS as of Visual CMS 12. You can check existing
  content beforehand with ``./vendor/bin/oe-console ddoevisualcms:migrate:less-to-scss --dry-run``.
* **Media Library 6 - error-free content out of the box:** A bundled fallback image is set
  automatically, so pages render cleanly even when media are missing or deleted - without
  any configuration. The fallback medium is protected against accidental deletion; missing
  media can be found more quickly via diagnostic messages.
* **WYSIWYG Editor 8 - more stable CMS links & media URLs:** CMS ident links are resolved
  correctly (no 404), Twig expressions in the filter are preserved, and media URLs are
  stored as ``oeMediaUrl`` instead of hardcoded.

.. note::

   During the update you choose one of the three offered bundle versions (12, 11 or 8);
   this can be preconfigured as described in the :doc:`update guide <../installation/update>`.
   Older lines (e.g. Visual CMS 9.x/10.x, Media Library 4.x, WYSIWYG 6.x) are not continued;
   existing installations switch to one of the offered versions.

.. note::

   **Note for extensions:** Media Library 6 is a major release. The methods
   ``MediaFacadeInterface::getMedia()`` and ``getMediaUrl()`` received an additional
   optional parameter - calling code remains compatible; modules that implement or decorate
   this interface must be adapted.

Configurable Storefront Rate Limiter
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

New in 7.6 (included in CE v7.6.0): an optional storefront request rate limiter, disabled
by default. It limits the call frequency of storefront actions on a rule basis - from a
coarse, global limit (throttling individual clients that call too often) to targeted rules
for sensitive actions such as login. It responds with ``429`` + ``Retry-After`` /
``X-RateLimit-*``; extension hook ``RateLimitExceededEvent``; console command
``oe:rate-limiter:prune`` (cron). It is a standalone limiter in addition to the API rate
limiter already available since 7.5; the two operate independently of each other.

Security Baseline
^^^^^^^^^^^^^^^^^

Several improvements harden the shop across the entire compilation:

* **Stronger password hashing:** The default bcrypt cost was increased
  (`#0007727 <https://bugs.oxid-esales.com/view.php?id=7727>`_).
* **Trusted proxies:** Remote address resolution now uses Symfony's
  ``Request::getClientIp()``. Proxy headers are **no longer** trusted by default; trusted
  IPs are configured via the DI parameter ``oxid_esales.request.trusted_proxies``.
* **HTTPS behind SSL offloaders** is detected via forwarded headers from trusted proxies.
* **APEX - external product URL secured:** external URLs are escaped and the scheme is
  checked (XSS/scheme injection hardening).
* **GDPR-compliant deletion:** When deleting a user by ID, all related records are now
  removed via cascade
  (`#0007138 <https://bugs.oxid-esales.com/view.php?id=7138>`_).

Modern Foundation - Migrations, Module Lifecycle, Console
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The technical base continues to be modernized within a predictable framework - old methods
remain usable, the new way is shown:

* **Database migrations registerable via DI:** Doctrine migrations can be provided via the
  DI tag ``oxid_esales.migration_path_provider`` (``MigrationPathProviderInterface``). This
  benefits components and is also the future preferred way for modules.
* **New console command** ``oe:database:migrate`` to run the migrations.
* **Services before activation:** Modules can provide selected services via an optional
  ``bootstrap-services.yaml`` - loaded for every installed module, regardless of activation
  state.
* **Clean console return values:** Console commands return consistent exit codes
  (0 = success, 1 = failure) - CI/automation-ready.

.. note::

   **Note for theme and module developers:** The Vite-based asset build was updated (Vite
   version bump, Sass 1.80). As a result, the Node version required for the **asset build**
   increases: **APEX theme** Node 20.19+, the modules of the Content & Media Bundle -
   **Media Library**, **WYSIWYG Editor** and **Visual CMS** - Node 22.12+ or 22.13+
   respectively. This affects only the asset build; shop operation itself does not change.

Continued Modernization (Deprecations)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In the course of modernization, some paths are marked as deprecated; the previous methods
remain usable, the new way is named in each case. Excerpt:

* Module ``metadata.php`` events (``onActivate`` / ``onDeactivate``) → DI event subscriber.
* ``oxid-esales/oxideshop-doctrine-migration-wrapper`` / ``oe-eshop-db_migrate`` →
  ``oe:database:migrate``.
* The BC autoloader for legacy class names (e.g. ``oxarticle``, ``oxorder``) - as well as
  the generation of the corresponding BC class aliases in the Unified Namespace Generator.
* ``Argon2IPasswordHashService``; ``UtilsServer::getRemoteAddress()`` /
  ``ViewConfig::getRemoteAddress()``.

The complete deprecation list can be found in the
`CE changelog 7.6 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.6.0/CHANGELOG-7.6.md>`_.

.. _fixes-760:

Improvements & Bug Fixes
------------------------

* #0006025 Case-sensitive column names in the admin order article search: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=6025>`_
* #0007073 Products already assigned no longer appear under "All available Products" in the category assignment popup: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7073>`_
* #0007770 Endless redirect and wrong URL generation fixed: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7770>`_
* Admin login no longer emits a PHP warning when the request has no ``Accept-Language`` header: `PR-999 <https://github.com/OXID-eSales/oxideshop_ce/pull/999>`_
* Address selection validation in account and checkout corrected.

* APEX #0007703 Product detail tabs render content again: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7703>`_
* APEX #0007880 Price calculation in order summary e-mails corrected: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7880>`_
* APEX #0007866 Missing ``oxwactions`` template added: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7866>`_
* APEX Order history "Shipped" status corrected: `PR-72 <https://github.com/OXID-eSales/apex-theme/pull/72>`_
* APEX #0008006 Recommendation list page (``cl=recommlist``) renders again (leftover Smarty ``->`` syntax removed); heading title, author and search term are escaped: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=8006>`_
* APEX Review page (``cl=review``) renders again when reviews are enabled (product rating in the reviews widget skipped on non-product pages).

* Twig Admin #0007837 Field controls for unsaved/inherited selection lists: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7837>`_
* Twig Admin #0007953 Setting a category as the main category on a product: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7953>`_
* Twig Admin: In the admin AJAX assignment lists (e.g. assigning products, groups or accessories), the display of a column can now be customized via a custom formatter.

* WYSIWYG Editor: CMS ident links/Twig filter fixed, media URLs as ``oeMediaUrl``, image URL cache cross-frame, leading ``<style>`` tag preserved during DOMPurify sanitization.
* WYSIWYG Editor: The migration command ``ddoewysiwyg:migrate:urls-to-ids`` now converts media references in all ``img src`` and ``a href`` attributes (instead of only in marked images), reports every converted and every unresolvable reference, and can output the report as CSV via ``--report-file``.
* Media Library: the requested media ID is preserved in the exception when no fallback is configured, media URL cache frame sharing; uploaded items show the stored file name; newly created folders appear at the top.

* GDPR Opt-In: exported files get a file extension.
* Demodata CE: correct SEO identifiers for "forgot password" pages.

.. _packages-760:

Packages
--------

.. note:: The 7.6 compilation consists of **CE, PE and EE** (B2B is **not** part of the
   initial 7.6 compilation).

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

**With functional 7.6 change:**

* OXID eShop CE **v7.5.1 → v7.6.0**: `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.6.0/CHANGELOG-7.6.md>`_
* APEX Theme **v3.1.0 → v3.2.0**: `Changelog <https://github.com/OXID-eSales/apex-theme/blob/v3.2.0/CHANGELOG-3.x.md>`_
* WYSIWYG Editor Module **v7.0.1 → v8.0.1** (Content & Media Bundle 12; alternatively v7.1.1 for Bundle 11 or v5.0.1 for Bundle 8): `Changelog <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v8.0.1/CHANGELOG.md>`_
* Media Library Module **v5.1.0 → v6.0.0** (Content & Media Bundle 12; alternatively v5.2.0 for Bundle 11 or v3.0.0 for Bundle 8): `Changelog <https://github.com/OXID-eSales/media-library-module/blob/v6.0.0/CHANGELOG.md>`_
* GDPR Opt-In Module **v4.4.0 → v4.5.0**: `Changelog <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.5.0/CHANGELOG.md>`_
* Twig Admin Theme **v3.1.0 → v3.2.0**: `Changelog <https://github.com/OXID-eSales/twig-admin-theme/blob/v3.2.0/CHANGELOG-3.x.md>`_
* Unified Namespace Generator **v5.3.1 → v5.4.0**: `Changelog <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.4.0/CHANGELOG.md>`_
* OXID Cookie Management powered by Usercentrics **v3.3.0 → v3.4.0** *(7.6 compatibility only)*: `Changelog <https://github.com/OXID-eSales/usercentrics/blob/v3.4.0/CHANGELOG.md>`_
* Demodata CE **v8.1.0 → v8.1.1**: `Changelog <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.1.1/CHANGELOG.md>`_
* Doctrine Migration Wrapper **v5.5.0 → v6.0.0** *(package is deprecated - replaced by* ``oe:database:migrate``\ *)*: `Changelog <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v6.0.0/CHANGELOG-6.x.md>`_

**Without functional 7.6 change** (branch initialization / workflow / test adjustments only)
remain on their 7.5 version:

* OXID eShop Composer Plugin v7.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.4.0/CHANGELOG-7.x.md>`_
* Twig Component v2.8.1: `Changelog <https://github.com/OXID-eSales/twig-component/blob/v2.8.1/CHANGELOG-2.x.md>`_
* Demodata Installer v3.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_
* DB Views Generator v2.2.0: `Changelog <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* Facts v4.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.4.0/CHANGELOG-4.x.md>`_

**External:**

* Eye-Able Assist v3.0.3 (unchanged)
* Makaira Connect Essential **2.2.0 → 2.2.1**

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop PE Compilation additionally contains the following packages:

* OXID eShop PE **v7.5.1 → v7.6.0**
* OXID eShop Demodata PE **v8.1.0 → v8.1.1**
* Twig Component PE v2.6.0 (unchanged)
* Visual CMS Module **v10.0.1 → v12.0.0** (Content & Media Bundle 12; alternatively v11.1.0 for Bundle 11 or v8.0.2 for Bundle 8)

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop EE Compilation additionally contains the following packages:

* OXID eShop EE **v7.5.1 → v7.6.0**
* OXID eShop Demodata EE **v8.2.0 → v8.2.1**
* Twig Component EE **v2.6.0 → v2.7.0**

.. COMMENTED OUT - does NOT render:
   B2B is not part of the initial 7.6 compilation (hence no EE-B2B section).

.. COMMENTED OUT - PROVISIONAL, does NOT render (not even in preview):
   Compatible extensions are released AFTER the compilation; no final 7.6 tags exist yet.
   Versions below are PROSPECTIVE - taken from the "Unreleased" changelog headers on each
   module's b-7.6.x branch (graphql-base → v14.0.0, confirmed by PO). The changelog links
   point at these prospective tags and will 404 until the module is actually tagged.
   When a module is provably released: verify its final version, then uncomment its line
   (adjust version/link if the released tag differs). Raw (English) content below:

   Compatible OXID Extensions
   --------------------------

   The compatible extensions are released after the compilation; the following versions are
   prospective (final with the respective module release):

   * OXAPI GraphQL Base Module **v14.0.0** (prospective): `Changelog <https://github.com/OXID-eSales/graphql-base-module/blob/v14.0.0/CHANGELOG-v14.md>`_
   * OXAPI GraphQL Configuration Access Module **v4.1.0** (prospective): `Changelog <https://github.com/OXID-eSales/graphql-configuration-access/blob/v4.1.0/CHANGELOG.md>`_
   * OXAPI GraphQL Storefront Module **v5.1.0** (prospective): `Changelog <https://github.com/OXID-eSales/graphql-storefront-module/blob/v5.1.0/CHANGELOG.md>`_
   * OXAPI GraphQL Storefront Administration Module **v5.0.0** (prospective): `Changelog <https://github.com/OXID-eSales/graphql-storefront-administration/blob/v5.0.0/CHANGELOG.md>`_
   * OXAPI GraphQL Orders Information Module **v2.3.0** (prospective): `Changelog <https://github.com/OXID-eSales/graphql-orders-information-module/blob/v2.3.0/CHANGELOG.md>`_
   * OXID Security Module **v4.1.0** (prospective): `Changelog <https://github.com/OXID-eSales/security-module/blob/v4.1.0/CHANGELOG.md>`_
   * OXID eShop Admin Tools **v2.1.0** (prospective): `Changelog <https://github.com/OXID-eSales/admin-tools-module/blob/v2.1.0/CHANGELOG.md>`_
   * OXID eShop Country VAT Administration **v2.6.0** (prospective): `Changelog <https://github.com/OXID-eSales/country-vat-module/blob/v2.6.0/CHANGELOG.md>`_
   * OXID eShop Geo-Blocking Module **v2.6.0** (prospective): `Changelog <https://github.com/OXID-eSales/geo-blocking-module/blob/v2.6.0/CHANGELOG.md>`_
   * OXID eShop Shipping Cost Compensation Module **v1.4.0** (prospective): `Changelog <https://github.com/OXID-eSales/freeshipping-coupons-module/blob/v1.4.0/CHANGELOG.md>`_
   * OXID eShop eVAT Module **v4.5.0** (prospective): `Changelog <https://github.com/OXID-eSales/vat_tbe_services/blob/v4.5.0/CHANGELOG.md>`_
   * OXID eShop Consistency Check Component **v3.1.0** (prospective): `Changelog <https://github.com/OXID-eSales/consistency-check-tool/blob/v3.1.0/CHANGELOG.md>`_
   * OXID Module Template **v5.3.0** (prospective): `Changelog <https://github.com/OXID-eSales/module-template/blob/v5.3.0/CHANGELOG.md>`_
   * OXID Examples Module **v2.2.0** (prospective): `Changelog <https://github.com/OXID-eSales/examples-module/blob/v2.2.0/CHANGELOG.md>`_
   * OXID ERP Interface (external; version follows with the release)

Update
------

The update procedure is described step by step in our
:doc:`update guide <../installation/update>`.

Installation
------------

If you want to install OXID eShop 7.6 from scratch, please follow our
:doc:`installation guide <../installation/new-installation/index>`.
