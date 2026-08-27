OXID eShop Compilation 7.5.0
============================

Release date: June 2, 2026

Highlights
----------

Content & Media Bundle 10
^^^^^^^^^^^^^^^^^^^^^^^^^^

OXID eShop 7.5 ships with the new **Content & Media
Bundle 10**. This includes the following extensions:

* Media Library 5
* WYSIWYG Editor 7
* Visual CMS 10 (Professional and Enterprise Edition only)

**Media Library 5:**

* **Search by media ID:** The search field now matches
  against media ID in addition to filename.
* **QueryBuilder:** Repository layer migrated to
  QueryBuilder.
* **Bootstrap Icons** replace Font Awesome.
* **File upload validation:** Content and MIME-type checks
  on every upload. SVGs containing scripts, foreign
  objects, ``on*`` event handlers, or ``javascript:``/
  ``data:`` URLs are rejected; raster images (jpg, jpeg,
  gif, png, webp, avif) must parse as a valid image.
* **Path safety:** Path-traversal characters (``/``, ``\``,
  ``..`` segments, null bytes) in upload filenames are
  rejected; consistent filename sanitization across upload
  and rename.
* **FileFormatRegistry and ContentValidatorInterface:**
  Integrators can register additional file formats via
  service configuration and hook in per-format content
  checks.
* **Fixed (by the validations above):**
  `#0007937 <https://bugs.oxid-esales.com/view.php?id=7937>`_
  and `#0007938 <https://bugs.oxid-esales.com/view.php?id=7938>`_.
* **Fixed:** Ctrl+click multi-select now works again (was
  broken due to a wrong event-button check).

Note for Media Library integrators:

* The upload validator chain now adds ``MimeTypeValidator``
  and ``ContentValidatorChain`` after
  ``FileExtensionValidator``. Modules that fully replace
  ``UploadedFileValidatorChainInterface`` need to list both
  validators in the same order to retain the upload-content
  protection.
* ``FilePathInterface`` adds a new method
  ``getExtension()``. Modules implementing this interface
  themselves need to add the method, returning the
  lowercased file extension.

**WYSIWYG Editor 7:**

* **Extensible by modules:** New Twig blocks
  ``ddoe_wysiwyg_plugins`` and
  ``ddoe_wysiwyg_summernote_options`` allow modules to
  extend the editor with custom plugins and options.
* **DOMPurify integration:** Normalizes HTML content in the
  editor.
* **Configurable:** New Twig block
  ``ddoe_wysiwyg_dompurify_config`` lets modules customize
  DOMPurify options.
* **Alt text migration:** New command
  ``ddoewysiwyg:migrate:alt-texts`` replaces missing or
  empty alt attributes on media images.
* **Bootstrap Icons** replace Font Awesome.
* **Fixed:** Incorrect Bootstrap style imports that affected
  shop styles (carried over from v6.0.3).

**Visual CMS 10** (Professional and Enterprise Edition only):

Visual CMS 10 is the consistent evolution of the
architecture introduced with Visual CMS 9. Key highlights:

* **"Anything-First" editing:** Choose any device as your
  starting point for design. Adjust widget sizes explicitly
  for each device — full control over all breakpoints.
* **Per-device widget sizes:** Separate configuration for
  smartphone, tablet (portrait/landscape), desktop, and
  large screens.
* **Device type switcher** in the editor for quick viewport
  changes.
* **Nested activity groups:** AND/OR logic for complex
  time-based widget visibility rules, including exclusion
  periods.
* **Localized date/time display** in activity settings,
  12h/24h support.
* **TypeScript:** JavaScript files migrated to TypeScript.
* **Bootstrap Icons** replace Font Awesome in the admin area.
* **Fixed:** WidgetModal — internal reference corrected
  (``public $modal`` → ``private #$modal``).
* **Fixed:** Responsive layout settings are now hidden in
  the widget edit modal when editing a row.
* **Fixed:** CMS pages with an expired "Active until" date
  are no longer displayed in the frontend.
* **Fixed:** Date pickers now respect the shop's configured
  date format setting (carried over from v9.2.1).
* **Fixed:** Carousel widget now retains images and links
  after re-opening the edit dialog (carried over from
  v9.2.1).

If you want to keep a previous version, you can preconfigure
your update. For more information, see our
:doc:`Update guide <../installation/update>`.

PHP 8.5 Support
^^^^^^^^^^^^^^^

The OXID eShop 7.5 compilation and all extensions listed
below have been tested with **PHP 8.3, 8.4, and 8.5**.
The minimum version is PHP 8.3. PHP 8.2 is no longer
supported.

API Entrypoint
^^^^^^^^^^^^^^

A new API layer (``api.php``) based on Symfony HttpKernel
allows exposing any shop functionality as API endpoints.
Routing uses PHP 8 ``#[Route]`` attributes. The API is
JSON-based and stateless. Four authentication models are
available: public, JWT token, frontend session, and admin
session.

Together with OXAPI (GraphQL), the shop now offers two
complementary interfaces: OXAPI for the rich product and
commerce data model, and custom API endpoints for individual
requirements.

New Search Service
^^^^^^^^^^^^^^^^^^

OXID eShop 7.5 provides a new, pluggable search
architecture. The new ``ProductSearchServiceInterface``
allows replacing the built-in SQL search with external
search engines such as Meilisearch or Elasticsearch. If
the external search fails, the shop automatically falls
back to the SQL search.

For more information, see the
`Developer documentation <https://docs.oxid-esales.com/developer/en/7.5/>`_.

New Email Service
^^^^^^^^^^^^^^^^^

OXID eShop 7.5 includes a new email service based on
Symfony Mailer. The service provides clean interfaces and
an extensible architecture that enables the integration of
additional mail transports via the available Symfony Mailer
configurations — without core modifications. In the 7.x
series, the new service runs as an alternative to the
existing system; ``Core/Email`` continues to work, and new
modules can use the ``MailerInterface`` directly.

HTML Sanitizer
^^^^^^^^^^^^^^

OXID eShop 7.5 includes an integrated HTML sanitizer as a
framework building block for cleaning HTML content. It is
based on the Symfony HtmlSanitizer and is **disabled by
default** — projects activate it explicitly via a service
parameter, define allow/deny rules, and use the new Twig
filter ``sanitize_html`` in the templates where it should
take effect. This allows the XSS attack vector for CMS
content to be addressed systematically, without
automatically changing existing shops.

Security Improvements
^^^^^^^^^^^^^^^^^^^^^

Several improvements strengthen the shop's security:

* **Sensitive GET parameters removed:** State-changing
  operations (e.g., adding items to the wishlist, removing
  vouchers) have been converted from GET links with session
  tokens in the URL to POST forms with hidden fields.
  Session IDs and CSRF tokens are no longer visible in URLs.
* **Bootstrap 3 cleanup:** Remaining Bootstrap 3 CSS classes
  in the APEX theme have been removed. Templates now
  exclusively use Bootstrap 5 classes.
* **HTML Sanitizer:** See above.

Performance Improvements
^^^^^^^^^^^^^^^^^^^^^^^^

Several targeted optimizations improve page load times:

* Empty baskets are detected early — no unnecessary
  calculations on every page load.
* Deactivated modules no longer affect shop frontend
  rendering time.
* Unnecessary instantiations of the basket component
  have been eliminated.
* Configuration lookups no longer trigger a full shop
  bootstrap.
* Module lookups as well as edition and cache directory
  lookups are cached to avoid repeated filesystem access.
* The template chain cache speeds up resolution of
  template extension chains — particularly relevant for
  shops with many active modules that override templates.
  The cache is automatically cleared when the shop cache is
  cleared via ``./vendor/bin/oe-console oe:cache:clear``.

.. _fixes:

Improvements & Bug Fixes
-------------------------

* #0007881 Model extension chain bypass: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7881>`_
* #0007877 composer/composer incorrectly in require instead of require-dev: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7877>`_
* #0007907 Discount quantity help text clarified: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7907>`_
* #0007178 Category dropdown no longer shown when all subcategories are hidden: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7178>`_
* #0007921 Template extensions for module templates now render correctly: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7921>`_

* Menu item counter for vendor-specific menu sections fixed: `PR-10 <https://github.com/OXID-eSales/twig-admin-theme/pull/10>`_
* Wrong product picture counter showing 13 instead of 12 fixed: `PR-14 <https://github.com/OXID-eSales/twig-admin-theme/pull/14>`_

* #0007922 Product gallery and grid listing images now respect the blConvertImagesToWebP setting, hover image on mobile viewports no longer broken: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7922>`_

* #0007751 Adding license keys via the command line no longer drops previously added keys (PE and EE): `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7751>`_

* #0007182 Wrong subquery in PE to EE migration for xxx2shop tables fixed (EE only): `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7182>`_

* Unified Namespace Generator: File path normalizing for sub-namespaces containing backslashes fixed

.. _packages:

Packages
--------

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop CE compilation contains the following
packages:

* APEX Theme v3.1.0: `Changelog <https://github.com/OXID-eSales/apex-theme/blob/v3.1.0/CHANGELOG-3.x.md>`_
* Eye-Able Assist v3.0.3
* GDPR Opt-In Module v4.4.0: `Changelog <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.4.0/CHANGELOG.md>`_
* Makaira Connect Essential 2.2.0: `Changelog <https://github.com/MakairaIO/oxid-connect-essential/blob/2.2.0/CHANGELOG.md>`_
* Media Library Module v5.1.0 (or v4.2.0 or v3.0.0 remaining): `Changelog <https://github.com/OXID-eSales/media-library-module/blob/v5.1.0/CHANGELOG.md>`_
* OXID Cookie Management powered by Usercentrics v3.3.0: `Changelog <https://github.com/OXID-eSales/usercentrics/blob/v3.3.0/CHANGELOG.md>`_
* OXID eShop CE v7.5.1: `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.5.1/CHANGELOG-7.5.md>`_
* OXID eShop Composer Plugin v7.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.4.0/CHANGELOG-7.x.md>`_
* OXID eShop Demodata CE v8.1.0
* OXID eShop Demodata Installer v3.3.0
* OXID eShop Doctrine Migration Wrapper v5.5.0: `Changelog <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.5.0/CHANGELOG-5.x.md>`_
* OXID eShop Facts v4.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.4.0/CHANGELOG-4.x.md>`_
* OXID eShop Unified Namespace Generator v5.3.1: `Changelog <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.3.1/CHANGELOG.md>`_
* OXID eShop Views Generator v2.2.0
* Twig Admin Theme v3.1.0: `Changelog <https://github.com/OXID-eSales/twig-admin-theme/blob/v3.1.0/CHANGELOG-3.x.md>`_
* Twig Component v2.8.1: `Changelog <https://github.com/OXID-eSales/twig-component/blob/v2.8.1/CHANGELOG-2.x.md>`_
* WYSIWYG Editor Module v7.0.1 (or v6.0.3 or v5.0.1 remaining): `Changelog <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v7.0.1/CHANGELOG.md>`_

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop PE compilation additionally contains the
following packages:

* OXID eShop Demodata PE v8.1.0
* OXID eShop PE v7.5.1
* Twig Component PE v2.6.0
* Visual CMS Module v10.0.1 (or v9.2.1 or v8.0.2 remaining)

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop EE compilation additionally contains the
following packages:

* OXID eShop Demodata EE v8.2.0
* OXID eShop EE v7.5.1
* Twig Component EE v2.6.0

OXID eShop EE B2B Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop EE B2B compilation additionally contains the
following packages:

* OXID eShop B2B Approval Procedure Module v7.5.0
* OXID eShop B2B Basket Module v7.5.0
* OXID eShop B2B Budget Module v7.5.0
* OXID eShop B2B Bulk Orders Module v7.5.0
* OXID eShop B2B Buying Agent Module v7.5.0
* OXID eShop B2B Custom Prices Module v7.5.0
* OXID eShop B2B Offers Module v7.5.0
* OXID eShop B2B Quick Orders Module v7.5.0
* OXID eShop B2B Scheduled Orders Module v7.5.0
* OXID eShop B2B Service Products Module v7.5.0
* OXID eShop B2B Services Module v7.5.0

For more information about B2B Edition releases, see the
(password-protected) `OXID eShop Enterprise B2B Edition
<https://docs.oxid-esales.com/b2b/en/7.5/releases/b2b-edition-750.html>`_
documentation.

Compatible OXID Extensions
--------------------------

* OXAPI GraphQL Base Module 13.0: `Documentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/7.5/>`_
* OXAPI GraphQL Configuration Access Module 4.0: `Documentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/7.5/>`_
* OXAPI GraphQL Storefront Module 5.0: `Documentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/7.5/>`_
* OXAPI GraphQL Storefront Administration Module 4.0: `Documentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/7.5/>`_
* OXID ERP Interface 4.4: `Documentation [en] (password-protected) <https://docs.oxid-esales.com/interfaces/erp/en/4.4>`_
* OXID eShop Admin Tools 2.0: `Documentation <https://docs.oxid-esales.com/modules/admin-tools/en/2.0/>`_
* OXID eShop Country VAT Administration 2.5: `Documentation [en] (GitHub) <https://github.com/OXID-eSales/country-vat-module/blob/v2.5.0/README.md>`_
* OXID eShop Geo-Blocking Module 2.5: `Documentation <https://docs.oxid-esales.com/modules/geo-blocking/en/2.5>`_
* OXID eShop Security Module 4.0: `Documentation <https://docs.oxid-esales.com/modules/security/en/4.0/>`_
* OXID eShop Shipping Cost Compensation Module 1.3: `Documentation <https://docs.oxid-esales.com/modules/freeshipping-coupons/en/1.3/>`_
* OXID eShop eVAT Module 4.4: `Documentation <https://docs.oxid-esales.com/modules/vat-tbe-services/en/4.4>`_
* OXID Cookie Management powered by Usercentrics 3.3: `Documentation <https://docs.oxid-esales.com/modules/usercentrics/de/3.3/>`_
* GDPR Opt-In Module 4.4: `Documentation <https://docs.oxid-esales.com/modules/gdpr-optin/de/4.4/>`_
* OXID eShop Consistency Check Component 3.0: `Documentation [en] (GitHub) <https://github.com/OXID-eSales/consistency-check-tool/blob/v3.0.0/README.md>`_
* OXID Module Template 5.2: `Documentation (GitHub) <https://github.com/OXID-eSales/module-template/blob/v5.2.0/README.md>`_
* OXID Examples Module 2.1: `Documentation (GitHub) <https://github.com/OXID-eSales/examples-module/blob/v2.1.0/README.md>`_

Update
------

The update procedure is described step by step in our
:doc:`Update guide <../installation/update>`.

Installation
------------

If you want to install OXID eShop 7.5 from scratch, please
follow our
:doc:`Installation guide <../installation/new-installation/index>`.
