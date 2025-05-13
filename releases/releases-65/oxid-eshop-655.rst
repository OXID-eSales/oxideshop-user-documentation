OXID eShop 6.5.5
================

Release date: 13-05-2025

To close two security vulnerabilities, install OXID eShop 6.5.5.

* Smarty-based rendering vulnerability

  If an error occurs while rendering an HTML template, the content that has already been generated is not discarded but output unfiltered. This can expose buffered data – such as a password reset link – in the frontend without authorization.

  For more information, see the `Security Bulletin 2025-001 <https://docs.oxid-esales.com/en/security/security-bulletins.html#security-bulletin-2025-001>`_.

* Composer vulnerability

  For security reasons, OXID eShop 6.5.5 requires Composer version 2.7.7.

  For more information, see

  * `Composer Version 2.7.7 <https://github.com/composer/composer/releases/tag/2.7.7>`_
  * `CVE-2024-35241 <https://github.com/advisories/GHSA-47f6-5gq3-vx9c>`_
  * `CVE-2024-35242 <https://github.com/advisories/GHSA-v9qv-c7wm-wgmf>`_

Improvements and adjustments
----------------------------

For more information about changes in the compilation, see `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.5.4...v6.5.5>`_.

Updated components
^^^^^^^^^^^^^^^^^^

We have updated the following components and modules:

* OXID eShop CE (update from 6.14.2 to 6.14.4): `Changelog 6.14.4 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.14.4/CHANGELOG.md>`_

Components of the compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The compilation contains the following components:

* OXID eShop CE 6.14.4: `Changelog 6.14.4 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.14.4/CHANGELOG.md>`_
* OXID eShop composer plugin 5.2.2: `Changelog 5.2.2 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.2.2/CHANGELOG.md>`_
* Theme "Flow" 3.8.1: `Changelog 3.8.1 <https://github.com/OXID-eSales/flow_theme/blob/v3.8.1/CHANGELOG.md>`_
* Theme "Wave" 1.8.0: `Changelog 1.8.0 <https://github.com/OXID-eSales/wave-theme/blob/v1.8.0/CHANGELOG.md>`_
* GDPR Opt-In 2.3.3: `Changelog 2.3.3 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* Klarna 5.5.3: `Changelog 5.5.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.3/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics 1.2.1: `Changelog 1.2.1 <https://github.com/OXID-eSales/usercentrics/blob/v1.2.1/CHANGELOG.md>`_
* PAYONE 1.9.0: `Changelog 1.9.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.9.0/Changelog.txt>`_
* PayPal 6.5.0: `Changelog 6.5.0 <https://github.com/OXID-eSales/paypal/blob/v6.5.0/CHANGELOG.md>`_
* WYSIWYG Editor + Mediathek 2.4.2: `Changelog 2.4.2 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v2.4.2/CHANGELOG.md>`_
* Makaira 1.4.5: `Changelog 1.4.5 <https://github.com/MakairaIO/oxid-connect-essential/blob/1.4.5/CHANGELOG.md>`_
* Unzer Payment for OXID 1.2.1 (EE): `Changelog 1.2.1 <https://github.com/OXID-eSales/unzer-module/blob/v1.2.1/CHANGELOG.md>`_

Installation
------------

To install or upgrade, follow the instructions in the *Installation* section:

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing a minor update <../../installation/update/minor-update>` |br|
:doc:`Installing a patch update <../../installation/update/patch-update>`

.. Intern: , Status:
