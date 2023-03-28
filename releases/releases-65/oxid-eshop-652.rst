OXID eShop 6.5.2
================

Release date: 21-02-2023

With OXID eShop 6.5.2, we close a potential security vulnerability: Passing a URL that contains the :code:`force_sid` parameter could have resulted in the session being hijacked. In case of a takeover, the attacker would have had access to the user account.

For more information, see our security bulletin at https://docs.oxid-esales.com/en/security/security-bulletins.html#security-bulletin-2023-001-cve-2023-26260.

With PAYONE 1.8.0, new payment methods are available.

In addition, we have fixed minor bugs.


Improvements and adaptations
----------------------------

Display changes in the compilation in the metapackage under `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.5.1…v6.5.2>`_.


Updated components
^^^^^^^^^^^^^^^^^^

We have updated the following components and modules:

* OXID eShop CE (Update from 6.13.0 to 6.14.0): `Changelog 6.14.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.14.0/CHANGELOG.md>`_
* OXID eShop PE (Update from 6.5.2 to 6.5.3)
* OXID eShop EE (Update from 6.8.0 to 6.8.1)
* WYSIWYG Editor + Media Library (Update from 2.4.1 to 2.4.2): `Changelog 2.4.2 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v2.4.2/CHANGELOG.md>`_
* PAYONE (update from 1.7.0 to 1.8.0): `Changelog 1.80 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.8.0/Changelog.txt>`_

Compilation components
^^^^^^^^^^^^^^^^^^^^^^

The compilation contains the following components:

* OXID eShop CE 6.14.0: `Changelog 6.14.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.14.0/CHANGELOG.md>`_
* OXID eShop composer plugin 5.2.2: `Changelog 5.2.2 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.2.2/CHANGELOG.md>`_
* Theme "Flow" 3.8.1: `Changelog 3.8.1 <https://github.com/OXID-eSales/flow_theme/blob/v3.8.1/CHANGELOG.md>`_
* Theme "Wave" 1.8.0: `Changelog 1.8.0 <https://github.com/OXID-eSales/wave-theme/blob/v1.8.0/CHANGELOG.md>`_
* GDPR Opt-In 2.3.3: `Changelog 2.3.3 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* Klarna 5.5.3: `Changelog 5.5.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.3/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics 1.2.1: `Changelog 1.2.1 <https://github.com/OXID-eSales/usercentrics/blob/v1.2.1/CHANGELOG.md>`_
* PAYONE 1.8.0: `Changelog PAYONE 1.8.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.8.0/Changelog.txt>`_
* PayPal 6.5.0: `Changelog 6.5.0 <https://github.com/OXID-eSales/paypal/blob/v6.5.0/CHANGELOG.md>`_
* WYSIWYG Editor + Mediathek 2.4.2: `Changelog 2.4.2 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v2.4.2/CHANGELOG.md>`_
* Makaira 1.4.2: `Changelog 1.4.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/1.4.2/CHANGELOG.md>`_
* Unzer Payment für OXID 1.0.0 (EE): `Changelog 1.0.0 <https://github.com/OXID-eSales/unzer-module/blob/v1.0.0/CHANGELOG.md>`_


Installation
------------

To install or upgrade, follow the instructions in the *Installation* section:

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing a minor update <../../installation/update/minor-update>` |br|
:doc:`Installing a patch update <../../installation/update/patch-update>`