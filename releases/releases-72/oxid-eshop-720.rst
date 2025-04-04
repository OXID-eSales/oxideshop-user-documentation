OXID eShop 7.2.0
================

Release-Datum: 02-12-2024

Changes at a glance
-------------------

Core
^^^^
* Removal of obsolete demo data images from the CE component
* PHP 8.2/8.3 support
* MySQL 8.0 and MariaDB 11 support
* :ref:`Possibility to disable order emails <disable_email_notifications>`
* Improvement of the forgotten password/password change functionality

APEX
^^^^

* `Flexible zoom images (feature) <https://docs.oxid-esales.com/eshop/en/7.2/releases/releases-72/oxid-eshop-720.html#user-experience>`_
* :ref:`Script in AJAX call (feature) <loading-dynamic-content>`
* Google Analytics 4 (page views, orders)
* SEO microdata update

Administration
^^^^^^^^^^^^^^

:ref:`GDPR-compliant export of user data <GDPR-compliant-export>`

New modules for Professional and Enterprise Edition
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* :productname:`OXID Security Module`
* :productname:`OXID Module Shipping Cost Compensation Coupon`

VCMS
^^^^

The VCMS bundle has been migrated to a new layout and contains various improvements.

Corrections
-----------

* Compilation 7.2.0 contains the corrections from Compilation 7.0.4/7.1.1:

  * Display of net prices in the frontend
  * Optimized ShopId calculation

* User registration in private sales mode - e-mail confirmation for activation is mandatory.
* Display new message for items in the shopping cart: `#0007548 <https://bugs.oxid-esales.com/view.php?id=7548>`_, `PR-964 <https://github.com/OXID-eSales/oxideshop_ce/pull/964>`_
* Multilingualism creation: `#0007683 <https://bugs.oxid-esales.com/view.php?id=7683>`_
* Twig component ``ifcontent`` extension: `#0007231 <https://bugs.oxid-esales.com/view.php?id=7231>`_
* Visual CMS 7.0.1 contains the corrections from Visual CMS 4.1.1/6.0.1
* APEX: see `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.2.x/CHANGELOG-7.2.md>`_.

In detail
---------

User Experience
^^^^^^^^^^^^^^^

Improve the shopping experience for your customers in your OXID eShop with three new zoom options.

* Hover Zoom: This function offers an interactive way to view product images in detail.

  When the mouse pointer hovers over the image, it is enlarged and the magnification follows the mouse movement.

  This allows users to examine different areas of the image in detail and increases interactivity and engagement.

* Modal zoom: Clicking on the product image opens it in a larger modal window, revealing more details.

  In addition, the user can zoom into the image within the modal to see particularly fine details.

  This offers a comprehensive opportunity to take a close look at products.

* Magnifier zoom: A magnifying glass function is activated when the mouse pointer is moved over the image.

  A separate area shows a greatly enlarged view of the image section directly under the mouse pointer.

  This enables precise viewing of specific product details without enlarging the entire image.


You can set the desired zoom globally for your OXID eShop. You can also define an individual zoom type for individual items.

For more information, see :ref:`configuration/images:Choosing a zoom type`.

Safety & reliability
^^^^^^^^^^^^^^^^^^^^

* For security reasons, OXID eShop 7.2.0 requires Composer version 2.7.7.

   For more information, see

   * `Composer Version 2.7.7 <https://github.com/composer/composer/releases/tag/2.7.7>`_
   * `CVE-2024-35241 <https://github.com/advisories/GHSA-47f6-5gq3-vx9c>`_
   * `CVE-2024-35242 <https://github.com/advisories/GHSA-v9qv-c7wm-wgmf>`_

* Improvement of the password forgetting/password change functionality.

Accessibility
^^^^^^^^^^^^^

Minor improvements in the APEX theme.

For more information, see the `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.2.x/CHANGELOG-7.2.md>`_.

New modules
^^^^^^^^^^^

The following new modules are available for the Professional Edition and the Enterprise Edition:

* :productname:`OXID Security Module`: Configure password policies to enforce the security of store users' passwords.

  For more information, see `What is a password policy? <https://docs.oxid-esales.com/modules/security/en/1.0/introduction.html#what-is-a-password-policy>`_.

* :productname:`OXID Module Shipping Cost Compensation Coupon`: Generate coupons with flexible amount to compensate for shipping costs.

  For more information, see `OXID Module Shipping Cost Compensation Coupon: What for/what not? <https://docs.oxid-esales.com/modules/freeshipping-coupons/en/1.0/introduction.html>`_.

Visual CMS & Mediathek
^^^^^^^^^^^^^^^^^^^^^^

See the Changelogs:

* Visual CMS: https://github.com/OXID-eSales/visual_cms_module/blob/b-7.2.x/CHANGELOG-7.x.md
* Mediathek: https://github.com/OXID-eSales/media-library-module/blob/b-7.2.x/CHANGELOG.md
* WYSIWYG-Editor: https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/b-7.2.x/CHANGELOG.md

New functions for developers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Note the following system requirements:

  * MySQL 8.0 (MySQL 5.7 is supported, but we don't recommend it)
  * MariaDB (tested with MariaDB 11)
  * PHP versions 8.2 or 8.3

  .. _Disable_email_notifications:

* If required, deactivate the sending of e-mail notifications for orders.

  By default, an e-mail is sent to the customer and the store operator when a new order is received.

  Deactivating email notifications can be useful, for example, if your ERP system sends the messages. In this case, only a log entry is created.

  For more information, see the developer documentation (English) under `Disabling order notification e-mails <https://docs.oxid-esales.com/developer/en/7.2/development/modules_components_themes/project/parameters.html#disabling-order-notification-e-mails>`_.

  .. _loading-dynamic-content:

* When working with dynamic content loaded via Ajax, use the ``setOuterHtmlAndExecuteScripts`` method to replace elements in the DOM with new content while handling the execution of embedded JavaScript in that content.

  For more information, see the developer documentation under `Loading dynamic content via AJAX <https://docs.oxid-esales.com/developer/en/7.2/development/modules_components_themes/theme/twig/loading-dynamic-content.html>`_.


.. _GDPR-compliant-export:

GDPR-compliant export of user data
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

As an administrator, export all data associated with a specific user in accordance with GDPR regulations.

For more information, see the GDPR Opt-in documentation (German) under `Benutzerdaten GDPR-konform exportieren <https://docs.oxid-esales.com/modules/gdpr-optin/de/latest/funktionsbeschreibung.html#benutzerdaten-gdpr-konform-exportieren>`_.


Components
----------

Updated components
^^^^^^^^^^^^^^^^^^

We have updated the following components and modules:

* `OXID eShop CE (update from v7.1.1 to v7.2.0) <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.2.0/CHANGELOG-7.2.md>`_
* OXID eShop PE (update from v7.1.0 to v7.2.0)
* OXID eShop EE (update from v7.1.0 to v7.2.0)
* `Apex theme (update from v1.4.0 to v2.0.0) <https://github.com/OXID-eSales/apex-theme/blob/v2.0.0/CHANGELOG-2.x.md#v200---2024-10-14>`_
* `Twig admin theme (update from v2.4.0 to v2.5.0) <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.5.0/CHANGELOG-2.x.md>`_
* `Twig component CE (update from v2.4.0 to v2.5.0) <https://github.com/OXID-eSales/twig-component/blob/v2.5.0/CHANGELOG-2.x.md>`_
* Twig component PE (update from v2.4.0 to v2.5.0)
* Twig component EE (update from v2.4.0 to v2.5.0)
* `OXID eShop demo data CE (update from v8.0.1 to v8.0.2) <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.1/CHANGELOG.md>`_
* OXID eShop demo data PE (update from v8.0.1 to v8.0.2)
* OXID eShop demo data EE (update from v8.0.2 to v8.0.3)
* `OXID eShop Demodata Installer (update from 3.2.0 to 3.3.0) <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_
* `OXID eShop doctrine migration integration (update from v5.2.0 to v5.3.0) <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.3.0/CHANGELOG-5.x.md>`_
* `WYSIWYG Editor + Mediathek (update from v4.1.0 to v4.2.0) <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.2.0/CHANGELOG.md>`_
* `GDPR opt-in (update from v4.0.0 to v4.1.0) <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.1.0/CHANGELOG.md#v410---2024-10-14>`_
* `Media Library Module (update from v2.0.1 to v2.1.1) <https://github.com/OXID-eSales/media-library-module/blob/v2.1.1/CHANGELOG.md>`_
* Visual CMS (update from v6.0.1 to v7.0.2)

Components of the compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The compilation contains the following components:

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
* `Mediathek 2.1.1 <https://github.com/OXID-eSales/media-library-module/blob/v2.1.1/CHANGELOG.md>`_
* `Makaira 2.1.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.2/CHANGELOG.md>`_
* `Eye-Able 3.0.3 <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/blob/v3.0.3/CHANGELOG.md>`_


Installation
------------

To install or upgrade, follow the instructions under :doc:`Installation and update <../../installation/index>`.

.. Intern: , Status:
