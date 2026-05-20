OXID eShop Core Edition
=======================

Starting with OXID eShop 6.5, a **Core Edition** is available as
an alternative to the standard compilation. It contains the shop
core and all its dependencies, but without bundled modules or
their dependencies. This gives you full control over which
modules to install and update.

Why Core Edition?
-----------------

The standard OXID eShop compilation ships as a tested snapshot:
the shop core and all included modules are pinned to exact
versions that have been verified together. This ensures
stability, but it also means that updating a single module
requires a new compilation release.

OXID eShop 6.5 is in **legacy support** status. While the shop
core continues to receive critical security fixes, the
compilation as a whole does not receive new releases. This can
create situations where individual modules need updates —
security patches, compatibility fixes, or replacements — but
the compilation's pinned dependencies prevent you from
installing them independently.

The Core Edition solves this by separating the shop core from
the modules:

* **Shop core**: Continues to receive critical security
  updates on a best-effort basis.
* **Modules**: You manage them individually via Composer —
  install, update, replace, or remove as needed.

.. note::

   We recommend updating to the current OXID eShop version
   (7.x) for full support, active maintenance, and access to
   the latest features and security improvements.

   OXID eShop 7.x runs on current PHP versions (8.3–8.5),
   MySQL 8.0/8.4, and MariaDB 11. It includes improved
   security measures and an architecture where module code
   is no longer directly accessible from the web.

   The Core Edition for 6.5 is intended for shops that cannot
   migrate to 7.x immediately but need to maintain or update
   individual modules.

   For information about updating to the current version,
   see the `update guide <https://docs.oxid-esales.com/developer/en/7.0/update/eshop_from_65_to_7/index.html>`_.

What is included
----------------

The Core Edition contains the shop core and infrastructure
packages — everything needed to run OXID eShop without bundled
modules:

* OXID eShop core (same version as in the standard compilation)
* Themes (Flow, Wave)
* Composer plugin, database views generator, migration wrapper
* All required Symfony and PHP dependencies

What is not included
--------------------

The following modules and their dependencies from the
standard CE compilation are **not included** in the Core
Edition metapackage:

* WYSIWYG Editor + Mediathek
  (``ddoe/wysiwyg-editor-module``)
* Klarna (``fatchip-gmbh/oxid-klarna-6``)
* Makaira (``makaira/oxid-connect-essential``)
* GDPR Opt-In (``oxid-esales/gdpr-optin-module``)
* PayPal (``oxid-esales/paypal-module``)
* Cookie Management powered by Usercentrics
  (``oxid-professional-services/usercentrics``)
* PAYONE (``payone-gmbh/oxid-6``)

.. warning::

   When you switch the metapackage and run
   ``composer update``, Composer will **remove** any package
   that is no longer required — directly or transitively —
   by the new dependency tree. This includes **active,
   running modules** — not just deactivated ones.

   This affects the modules and their dependencies that
   were bundled with the standard compilation metapackage.
   Modules that you or your agency installed separately
   are already explicit requirements in your
   ``composer.json`` and will remain installed.

   Before switching, identify which of the compilation's
   bundled modules your shop actually uses. The migration
   guide in the developer documentation provides detailed
   instructions for this.

.. note::

   PE and EE compilations include additional modules (e.g.
   Visual CMS for PE/EE, Unzer Payment for EE). The same
   principle applies — the Core Edition for each edition
   contains only the shop core and its dependencies. All
   modules must be explicitly required.

Editions
--------

The Core Edition is available for all three OXID eShop editions:

* CE: ``oxid-esales/metapackage-ce-core``
* PE: ``oxid-esales/metapackage-pe-core``
* EE: ``oxid-esales/metapackage-ee-core``

Migrating to Core Edition
--------------------------

.. important::

   This is a critical change to your shop's dependency
   structure. **Always perform the migration on a development
   or staging environment first.** Verify that the shop works
   correctly — including all modules, payment methods, and
   checkout flows — before applying the change to your
   production system.

The migration requires two things in a single step: replacing
the metapackage **and** explicitly requiring every module your
shop currently has installed — even modules you eventually want
to remove. Do not run ``composer update`` after only swapping
the metapackage — this will remove your modules. Once the
migration is complete, drop unwanted modules cleanly with
``composer remove`` (see "Managing modules after migration"
below).

Overview
^^^^^^^^

1. **Backup** your shop — database, files, and
   ``composer.json``.
2. **Save** your ``composer.lock`` — it is the complete
   record of all currently installed packages and their
   exact versions.
3. **Edit** ``composer.json``: replace the standard metapackage
   with the Core Edition metapackage, and add every module
   currently installed in your shop as an explicit requirement
   with its current version — even modules you eventually want
   to remove. You can drop those cleanly with ``composer remove``
   after the migration is complete.
4. **Run** ``composer update`` on your development or staging
   system.
5. **Verify** that all expected packages are still present
   in the expected versions and the shop functions
   correctly.
6. **Test** the shop thoroughly — frontend, checkout, payment,
   admin — before deploying to production.

The detailed step-by-step procedure with exact Composer
commands is described in the `developer documentation <https://docs.oxid-esales.com/developer/en/6.5/update/migrate-to-core-edition.html>`_.

Managing modules after migration
----------------------------------

After switching to the Core Edition, modules are no longer
locked by the compilation metapackage. You can manage them
individually:

**Updating a module:**

.. code:: bash

   composer update vendor/module-name

**Removing a module:**

.. code:: bash

   composer remove vendor/module-name

**Installing a replacement module:**

.. code:: bash

   composer require vendor/new-module-name

.. important::

   After any module change, clear the shop cache and regenerate
   views:

   .. code:: bash

      vendor/bin/oe-console oe:cache:clear
      vendor/bin/oe-console oe:module:activate module-id
      vendor/bin/oe-console oe:database:generateviews
