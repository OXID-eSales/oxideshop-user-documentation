OXID eShop 7.3.0
================

Release date: 2025-04-15

Changes at a glance
-------------------

Core
^^^^

* Support for PHP 8.4

.. todo: #HR/#DK: Add new features

APEX
^^^^

.. todo: #HR/#DK: Add new features

Administration
^^^^^^^^^^^^^^

.. todo: #HR/#DK: Add new features

New and updated modules
^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: OXDEV-9193 (Cache clear button)?

* Install the new OXID Admin Tools Module to manually clear the template cache by klicking a button in the admin backend.

  For more information, see `OXID Admin Tools Module <https://docs.oxid-esales.com/###tbd###/de/1.0/introduction.html>`_.


With OXID eShop 7.3, you can benefit from the features of the following updated modules:

.. todo: #HR: Add new features in :productname:`OXID Security Module`: v2.0 = OXDEV-8930 CAPTCHA)

* :productname:`OXID Security Module` 2.0

  With CAPTCHA protection, secure your OXID eShop form areas against automated bot attacks.

  .. todo: #tbd: Verify URLs:
  .. todo: #HR: Will all modules be released at the same time, so it makes sense to refer to the release notes?

  For more information, see `OXID Security Module <https://docs.oxid-esales.com/modules/security/de/2.0/releases/security-module-200.html>`_.

* :productname:`OXID eShop Enterprise B2B Edition` 7.3

  For more information, see `OXID eShop Enterprise B2B Edition <https://docs.oxid-esales.com/b2b/de/7.3/releases/b2b-edition-730.html>`_.

* :productname:`OXID ERP Interface` 4.2
* :productname:`OXID eShop eVAT` 4.2
* :productname:`Visual CMS`
* :productname:`OXID Cookie Management powered by usercentrics` 3.1
* :productname:`GDPR Opt-in` 4.2
* :productname:`Geo-blocking` 2.3

.. todo: #HR/#MF: Add VCMS updates

Fixes
-----

.. todo: #HR: Add bug IDs and changelog references:
`#0007683 <https://bugs.oxid-esales.com/view.php?id=7683>`_
`Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.3.x/CHANGELOG-7.3.md>`_.

In detail
---------

User Experience
^^^^^^^^^^^^^^^

.. todo: #HR/#DK: Is there anything coming?

Improve your ...

More information is available at :ref:`tbd:tbd`.

Security & Reliability
^^^^^^^^^^^^^^^^^^^^^^

.. todo: #HR/#DK: Is there anything coming?

* For security reasons, OXID eShop 7.3.0 requires ...

   More information is available at ...

Accessibility
^^^^^^^^^^^^^

Minor improvements ...

Further information can be found in the `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.3.x/CHANGELOG-7.3.md>`_.

Visual CMS & Media Library
^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #HR/#MF: Will more info be added?

See changelogs:

* Visual CMS: https://github.com/OXID-eSales/visual_cms_module/blob/b-7.3.x/CHANGELOG-7.x.md
* Media Library: https://github.com/OXID-eSales/media-library-module/blob/b-7.3.x/CHANGELOG.md
* WYSIWYG Editor: https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/b-7.3.x/CHANGELOG.md

New features for developers
^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #HR/#DK: Is there anything additioal coming?

* Leverage full compatibility with PHP 8.2 to 8.4.

  The software supports PHP versions up to and including PHP 8.4. However, note changes in floating-point rounding behavior in PHP 8.4, which may result in different calculation outcomes compared to PHP 8.3.

  More details can be found in the section `Server and System Requirements <https://docs.oxid-esales.com/eshop/de/7.3/installation/neu-installation/server-und-systemvoraussetzungen.html>`_, under `PHP <https://docs.oxid-esales.com/eshop/de/7.3/installation/neu-installation/server-und-systemvoraussetzungen.html#php>`_.

* Improve template security with the Twig Sandbox Extension.

  Use the Twig Sandbox Extension with the {% sandbox %} tag to control which tags, filters, and functions are allowed in your templates, enhancing the security of dynamic template rendering.

  .. todo: #tbd: verify link

  Learn more in the developer documentation (English) under `Using the Twig Sandbox Extension <https://docs.oxid-esales.com/developer/en/7.3/development/modules_components_themes/theme/twig_sandbox.html>`_.

* Optimize OXID controller management.

  Register OXID controllers as services in the Dependency Injection Container (DIC) for easier handling, better testability, and more flexible controller extension.

  .. todo: #tbd: verify link

  Further information is available in the developer documentation (English) under `Controller as a service <https://docs.oxid-esales.com/developer/en/7.3/development/tell_me_about/controller_as_service.html>`_.

* Simplify environment variable management.

  Use a `.env` file to define environment variables and securely integrate them into your OXID eShop application, making it easier to manage sensitive configuration values and environment-specific settings.

  .. todo: #tbd: verify link

  Further information is available in the developer documentation (English) under `Environment variables <https://docs.oxid-esales.com/developer/en/7.3/development/modules_components_themes/project/environment.html>`_.

Components
----------

Updated components
^^^^^^^^^^^^^^^^^^

.. todo: #HR: Update component version numbers

We have updated the following components and modules:

* `OXID eShop CE (from v7.1.1 to v7.2.0) <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.2.0/CHANGELOG-7.2.md>`_
* OXID eShop PE (from v7.1.0 to v7.2.0)
* OXID eShop EE (from v7.1.0 to v7.2.0)
* `Apex theme (from v1.4.0 to v2.0.0) <https://github.com/OXID-eSales/apex-theme/blob/v2.0.0/CHANGELOG-2.x.md#v200---2024-10-14>`_
* `Twig admin theme (from v2.4.0 to v2.5.0) <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.5.0/CHANGELOG-2.x.md>`_
* `Twig component CE (from v2.4.0 to v2.5.0) <https://github.com/OXID-eSales/twig-component/blob/v2.5.0/CHANGELOG-2.x.md>`_
* Twig component PE (from v2.4.0 to v2.5.0)
* Twig component EE (from v2.4.0 to v2.5.0)
* `OXID eShop demo data CE (from v8.0.1 to v8.0.2) <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.1/CHANGELOG.md>`_
* OXID eShop demo data PE (from v8.0.1 to v8.0.2)
* OXID eShop demo data EE (from v8.0.2 to v8.0.3)
* `OXID eShop Demodata Installer (from 3.2.0 to 3.3.0) <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_
* `OXID eShop doctrine migration integration (from v5.2.0 to v5.3.0) <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.3.0/CHANGELOG-5.x.md>`_
* `WYSIWYG Editor + Media Library (from v4.1.0 to v4.2.0) <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.2.0/CHANGELOG.md>`_
* `GDPR opt-in (from v4.0.0 to v4.1.0) <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.1.0/CHANGELOG.md#v410---2024-10-14>`_
* `Media Library Module (from v2.0.1 to v2.1.1) <https://github.com/OXID-eSales/media-library-module/blob/v2.1.1/CHANGELOG.md>`_
* Visual CMS (from v6.0.1 to v7.0.2)

Compilation components
^^^^^^^^^^^^^^^^^^^^^^

.. todo: #HR: Update version numbers

The compilation includes the following components:

* `OXID eShop CE 7.2.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.2.0/CHANGELOG-7.2.md>`_
* OXID eShop PE 7.2.0
* OXID eShop EE 7.2.0

* `Apex theme 2.0.0 <https://github.com/OXID-eSales/apex-theme/blob/v2.0.0/CHANGELOG-2.x.md>`_

* `Twig admin theme 2.5.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.5.0/CHANGELOG-2.x.md>`_
* `Twig component CE 2.5.0 <https://github.com/OXID-eSales/twig-component/blob/v2.5.0/CHANGELOG-2.x.md>`_
* Twig component PE 2.5.0
* Twig component EE 2.5.0

* `OXID eShop composer plugin 7.2.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.2.0/CHANGELOG-7.x.md>`_
* `OXID eShop Views Generator 2.2.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* `OXID eShop demo data installer 3.3.0 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_

* `OXID eShop demo data CE 8.0.2 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.2/CHANGELOG.md>`_
* OXID eShop demo data PE 8.0.2
* OXID eShop demo data EE 8.0.3

* `OXID eShop doctrine migration integration 5.3.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.3.0/CHANGELOG-5.x.md>`_
* `OXID eShop facts 4.2.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.2.0/CHANGELOG-4.x.md>`_
* `Unified Namespace Generator 5.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.1.0/CHANGELOG.md>`_

* `GDPR Opt-In 4.1.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.1.0/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 3.0.0 <https://github.com/OXID-eSales/usercentrics/blob/v3.0.0/CHANGELOG.md>`_
* Visual CMS 7.0.2 (PE/EE)

* `WYSIWYG Editor 4.2.0 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.2.0/CHANGELOG.md>`_
* `Media Library 2.1.1 <https://github.com/OXID-eSales/media-library-module/blob/v2.1.1/CHANGELOG.md>`_
* `Makaira 2.1.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.2/CHANGELOG.md>`_
* `Eye-Able 3.0.3 <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/blob/v3.0.3/CHANGELOG.md>`_

Installation
------------

To install or update, follow the instructions at :doc:`Installation <../../installation/index>`.
