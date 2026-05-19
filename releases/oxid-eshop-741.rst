OXID eShop Compilation 7.4.1
============================

Release date: TBD

Improvements & Bug Fixes
-------------------------

Composer 2.9 Compatibility
^^^^^^^^^^^^^^^^^^^^^^^^^^

Composer 2.9 performs an automatic security audit and aborts
the installation if packages with known security issues are
included. With the OXID eShop 7.4.0 compilation, this could
cause the installation to fail when using the default
settings of Composer 2.9.

In the 7.4.1 compilation, the affected packages have been
updated so that the installation works without issues using
the default settings of Composer 2.9.

The affected packages have been updated:

* ``composer/composer`` from 2.8.12 to 2.9.8
* ``symfony/process`` from v7.3.4 to v7.4.8

OXID eShop 7.4.1 can be installed without issues using both
Composer CLI 2.8 and Composer CLI 2.9.

Content & Media Bundle
^^^^^^^^^^^^^^^^^^^^^^

**WYSIWYG Editor** (v6.0.1 to v6.0.3):

* Fixed: Summernote toolbar dropdowns not opening due to
  Bootstrap 5 event delegation conflict
* Fixed: Content deleted when emojis are used in text
  widgets (`#0007619 <https://bugs.oxid-esales.com/view.php?id=7619>`_)
* Fixed: Incorrect Bootstrap style imports affecting shop
  styles

**Visual CMS** (v9.1.0 to v9.2.1, Professional and
Enterprise Edition only):

* New: Nested activity groups with AND/OR logic for complex
  time-based widget visibility rules
* New: Exclusion periods for activity time ranges
* Fixed: Column widget properties not shown when editing
  another widget and the column widget simultaneously
* Fixed: During the
  ``ddoevisualcms:migrate:veparse-to-vetree`` command, the
  "widget mode" flag is now enabled for converted "veparse"
  contents
* Fixed: Content deleted when emojis are used in text
  widgets (`#0007619 <https://bugs.oxid-esales.com/view.php?id=7619>`_)
* Fixed: Media URLs in text widgets are now migrated during
  the ``ddoevisualcms:migrate:urls-to-ids`` command
* Fixed: Date pickers now respect the shop's configured
  date format setting
* Fixed: Carousel widget loses images and links after
  re-opening the edit dialog

**Media Library Module** (v4.1.0 to v4.2.0, or v3.0.0
remaining):

* New: SVG upload content validation — files containing
  scripts, foreign objects, ``on*`` event handlers, or
  ``javascript:``/``data:`` URLs are rejected
* New: MIME-type validation on every upload — files whose
  sniffed content type does not match the declared
  extension are rejected
* New: Raster-image content validation for jpg, jpeg, gif,
  png, webp, avif — files that do not parse as a valid
  image are rejected
* New: ``FileFormatRegistry`` mapping allowed extensions to
  accepted MIME types; integrators can register additional
  formats via service configuration
* New: ``ContentValidatorInterface`` for per-format content
  checks; tagged services are auto-discovered by the upload
  chain
* New: ``FilePathInterface::getExtension()`` returns the
  lowercased file extension
* Changed: Consistent filename sanitization across upload
  and rename
* Changed: ``composer.json`` now declares ``ext-dom``
* Security: Reject path-traversal characters (``/``, ``\``,
  ``..`` segments, null bytes) in upload filenames
* Fixed: Ctrl+click multi-select was not working due to
  wrong event button check

Note for integrators:

* The upload validator chain now adds ``MimeTypeValidator``
  and ``ContentValidatorChain`` after
  ``FileExtensionValidator``. Modules that fully replace
  ``UploadedFileValidatorChainInterface`` need to list both
  validators in the same order to retain the upload-content
  protection.
* ``FilePathInterface`` adds a new method ``getExtension()``.
  Modules implementing this interface themselves need to add
  the method, returning the lowercased file extension.

Developer Tools
^^^^^^^^^^^^^^^

**OXID eShop Unified Namespace Generator** (v5.2.0 to
v5.2.1):

* Fixed: File path normalizing for sub-namespaces containing
  backslashes

.. _packages-741:

Packages
--------

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop CE compilation contains the following
packages:

* APEX Theme v3.0.2
* Eye-Able Assist v3.0.3
* GDPR Opt-In Module v4.3.0
* Makaira Connect Essential 2.1.4
* Media Library Module v4.2.0 (or v3.0.0 remaining)
* OXID Cookie Management powered by Usercentrics v3.2.1
* OXID eShop CE from v7.4.0 to v7.4.2
* OXID eShop Composer Plugin v7.3.0
* OXID eShop Demodata CE v8.1.0
* OXID eShop Demodata Installer v3.3.0
* OXID eShop Doctrine Migration Wrapper v5.4.0
* OXID eShop Facts v4.3.0
* OXID eShop Unified Namespace Generator v5.2.1
* OXID eShop Views Generator v2.2.0
* Twig Admin Theme v3.0.1
* Twig Component v2.7.0
* WYSIWYG Editor Module from v6.0.1 to v6.0.3 (or v5.0.1 remaining): `Changelog <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v6.0.3/CHANGELOG.md>`_

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop PE compilation additionally contains the
following packages:

* OXID eShop Demodata PE v8.1.0
* OXID eShop PE from v7.4.0 to v7.4.2
* Twig Component PE v2.5.0
* Visual CMS Module from v9.1.0 to v9.2.1 (or v8.0.2 remaining)

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop EE compilation additionally contains the
following packages:

* OXID eShop Demodata EE v8.2.0
* OXID eShop EE from v7.4.0 to v7.4.2
* Twig Component EE v2.5.0

OXID eShop EE B2B Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop EE B2B compilation additionally contains the
following packages:

* OXID eShop B2B Approval Procedure Module from v7.4.0 to v7.4.1
* OXID eShop B2B Basket Module v7.4.0
* OXID eShop B2B Budget Module v7.4.0
* OXID eShop B2B Bulk Orders Module v7.4.0
* OXID eShop B2B Buying Agent Module v7.4.0
* OXID eShop B2B Custom Prices Module v7.4.0
* OXID eShop B2B Offers Module v7.4.0
* OXID eShop B2B Quick Orders Module v7.4.0
* OXID eShop B2B Scheduled Orders Module v7.4.0
* OXID eShop B2B Service Products Module v7.4.0
* OXID eShop B2B Services Module v7.4.0

For more information about B2B Edition releases, see the
(password-protected) `OXID eShop Enterprise B2B Edition
<https://docs.oxid-esales.com/b2b/en/7.4/releases/b2b-edition-740.html>`_
documentation.

Compatible OXID Extensions
--------------------------

The compatible OXID extensions are the same as for version
7.4.0. For more information, see the `Release Notes for
OXID eShop Compilation 7.4.0 <oxid-eshop-740>`_.

Update
------

Run the following commands to update your OXID eShop from
7.4.0 to 7.4.1:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate
