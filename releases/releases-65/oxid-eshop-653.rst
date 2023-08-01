OXID eShop 6.5.3
================

Release date: 01-08.2023

With OXID eShop 6.5.3 we close a security vulnerability.

The package :technicalname:`guzzlehttp/psr7` version 2.4.3 affected by a security vulnerability (NVD - CVE-2022-24775) is no longer included in the OXID eShop EE compilation. The package became part of the EE compilation as a dependency by version 1.0.1 of the :productname:`Unzer Payment for OXID` payment module.

Due to incorrect header parsing, it would be possible to pass additional values in a header after a line break in special cases.

The vulnerability has been classified by CWE as CWE-20, and it is not known what the impact of an attack would be.

Other improvements:

* With PAYONE 1.9.0, new payment methods are available for selection.
* With Unzer 1.1.1, the new payment method Unzer Invoice (Paylater) is available. We have also made numerous improvements to the module.
* Makaira 1.4.5 contains improvements.

We have also improved minor bugs.


Improvements and adjustments
----------------------------

Display changes in the compilation in the metapackage under `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.5.2...v6.5.3>`_.

Display corrections in the bugtracker under https://bugs.oxid-esales.com/changelog_page.php?version_id=725.

Updated components
^^^^^^^^^^^^^^^^^^

We have updated the following components and modules:

* OXID eShop CE (Update from 6.14.0 to 6.14.1): `Changelog 6.14.1 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.14.1/CHANGELOG.md>`_
* PAYONE (Update from 1.8.0 to 1.9.0): `Changelog 1.9.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.9.0/Changelog.txt>`_
* Unzer Modul (Update from 1.0.1 to 1.1.1): `Changelog 1.1.1 <https://github.com/OXID-eSales/unzer-module/blob/v1.1.1/CHANGELOG.md>`_
* Makaira (Update from 1.4.3 to 1.4.5): `Changelog 1.4.5 <https://github.com/MakairaIO/oxid-connect-essential/blob/1.4.5/CHANGELOG.md>`_


Components of the compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The compilation contains the following components:

* OXID eShop CE 6.14.1: `Changelog 6.14.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.14.0/CHANGELOG.md>`_
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
* Unzer Payment für OXID 1.1.1 (EE): `Changelog 1.1.1 <https://github.com/OXID-eSales/unzer-module/blob/v1.1.1/CHANGELOG.md>`_


Installation
------------

To install or upgrade, follow the instructions in the *Installation* section:

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing a minor update <../../installation/update/minor-update>` |br|
:doc:`Installing a patch update <../../installation/update/patch-update>`

.. Intern: , Status:


