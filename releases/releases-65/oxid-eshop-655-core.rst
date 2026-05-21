OXID eShop 6.5.5 Core Edition
=============================

The OXID eShop 6.5.5 Core Edition is an alternative to the
standard 6.5.5 compilation. It contains the same shop core
and its dependencies, but without bundled modules or their
dependencies. This allows you to manage modules independently
via Composer.

Background
----------

The standard OXID eShop 6.5.5 compilation pins the shop core
and all modules to fixed versions. OXID eShop 6.5 receives
critical security fixes on a best-effort basis, but the
compilation as a whole does not receive new releases. This
can prevent you from updating individual modules when
needed.

The 6.5.5 Core Edition addresses this by providing a
metapackage that includes only the shop core and its
infrastructure. You decide which modules to install and at
which version.

What changes
------------

* The standard metapackage
  (``oxid-esales/oxideshop-metapackage-ce``, or PE/EE
  respectively) is replaced by the corresponding Core
  Edition metapackage.
* The shop core remains at the same version — this is not
  an upgrade.
* Modules previously bundled in the compilation must be
  added as explicit Composer requirements if you want to
  keep them.

For the full list of modules not included in the Core
Edition and the migration procedure, see
:doc:`Core Edition <../../installation/core-edition>`.

.. note::

   We recommend updating to the current OXID eShop version
   (7.x) for full support, active maintenance, and the
   latest security improvements. The Core Edition for 6.5
   is intended for shops that cannot migrate to 7.x
   immediately.

Components of the Core Edition (CE)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* OXID eShop CE 6.14.4: `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.14.4/CHANGELOG.md>`_
* OXID eShop Composer Plugin 5.2.2: `Changelog <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.2.2/CHANGELOG.md>`_
* OXID eShop DB Views Generator 1.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v1.3.0/CHANGELOG.md>`_
* OXID eShop Demodata CE 6.0.5: `Changelog <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v6.0.5/CHANGELOG.md>`_
* OXID eShop Demodata Installer 1.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v1.4.0/CHANGELOG.md>`_
* OXID eShop Doctrine Migration Wrapper 3.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v3.4.0/CHANGELOG.md>`_
* OXID eShop Facts 2.4.1: `Changelog <https://github.com/OXID-eSales/oxideshop-facts/blob/v2.4.1/CHANGELOG.md>`_
* OXID eShop Unified Namespace Generator 2.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v2.3.0/CHANGELOG.md>`_
* Theme "Flow" 3.8.1: `Changelog <https://github.com/OXID-eSales/flow_theme/blob/v3.8.1/CHANGELOG.md>`_
* Theme "Wave" 1.8.0: `Changelog <https://github.com/OXID-eSales/wave-theme/blob/v1.8.0/CHANGELOG.md>`_

Requires Composer 2.7.7. Infrastructure dependencies
(Symfony, Doctrine, Monolog, PHPMailer, Smarty, etc.)
are pinned in the metapackage.

The following modules and their dependencies from the
standard 6.5.5 compilation are **not included**:

* WYSIWYG Editor + Mediathek 2.4.2
* Klarna 5.5.3
* Makaira 1.4.5
* GDPR Opt-In 2.3.3
* PayPal 6.5.0
* Cookie Management powered by Usercentrics 1.2.1
* PAYONE 1.9.0

Components of the Core Edition (PE)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Includes everything from the CE Core Edition, plus:

* OXID eShop PE 6.5.3
* OXID eShop Demodata PE 6.0.5

Not included (in addition to the CE modules above):

* Visual CMS 3.7.0

Components of the Core Edition (EE)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Includes everything from the PE Core Edition, plus:

* OXID eShop EE 6.8.1
* OXID eShop Demodata EE 6.0.5

Not included (in addition to the CE and PE modules
above):

* Unzer Payment for OXID 1.2.1 and its dependencies

Migration
---------

To migrate an existing 6.5.5 shop to the Core Edition,
follow the instructions in the
:doc:`Core Edition migration guide
<../../installation/core-edition>`.
