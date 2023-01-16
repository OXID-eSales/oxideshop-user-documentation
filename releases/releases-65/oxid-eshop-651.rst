OXID eShop 6.5.1
================

Release date: 06-12-2022

With OXID eShop 6.5.1, the "Wave" theme no longer dynamically embeds Google Fonts, but locally from the theme folder.

Background: Shop owners that use dynamically embedded Google Fonts have become victims of warnings.

If you have dynamically included Google fonts other than those used in the Wave theme, make sure to include these fonts from a local folder as well. Google describes how to do this at https://fonts.google.com/knowledge/using_type/self_hosting_web_fonts.

For more information, see our `blogpost of 21-09-2022 <https://www.oxid-esales.com/blog/moegliche-abmahnungen-bei-google-fonts>`_.

We also fixed bugs. See :ref:`releases/releases-65/oxid-eshop-651:Corrections`.


Improvements and adaptations
----------------------------

Display changes in the compilation in the metapackage under `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.5.0…v6.5.1>`_.


Updated components
^^^^^^^^^^^^^^^^^^

We have updated the following components and modules:

* OXID eShop CE (Update from 6.12.0 to 6.13.0): `Changelog 6.13.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.13.0/CHANGELOG.md>`_
* Theme "Wave" (Update from 1.6.2 to 1.8.0): `Changelog 1.8.0 <https://github.com/OXID-eSales/wave-theme/blob/v1.8.0/CHANGELOG.md>`_

Compilation components
^^^^^^^^^^^^^^^^^^^^^^

The compilation contains the following components:

* OXID eShop CE 6.13.0: `Changelog 6.13.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.13.0/CHANGELOG.md>`_
* OXID eShop composer plugin 5.2.2: `Changelog 5.2.2 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.2.2/CHANGELOG.md>`_
* Theme "Flow" 3.8.1: `Changelog 3.8.1 <https://github.com/OXID-eSales/flow_theme/blob/v3.8.1/CHANGELOG.md>`_
* Theme "Wave" 1.8.0: `Changelog 1.8.0 <https://github.com/OXID-eSales/wave-theme/blob/v1.8.0/CHANGELOG.md>`_
* GDPR Opt-In 2.3.3: `Changelog 2.3.3 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* Klarna 5.5.3: `Changelog 5.5.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.3/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics 1.2.1: `Changelog 1.2.1 <https://github.com/OXID-eSales/usercentrics/blob/v1.2.1/CHANGELOG.md>`_
* PAYONE 1.7.0: `Changelog 1.7.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.7.0/Changelog.txt>`_
* PayPal 6.5.0: `Changelog 6.5.0 <https://github.com/OXID-eSales/paypal/blob/v6.5.0/CHANGELOG.md>`_
* WYSIWYG Editor + Mediathek 2.4.1: `Changelog 2.4.1 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v2.4.1/CHANGELOG.md>`_
* Makaira 1.4.2: `Changelog 1.4.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/1.4.2/CHANGELOG.md>`_
* Unzer Payment für OXID 1.0.0 (EE): `Changelog 1.0.0 <https://github.com/OXID-eSales/unzer-module/blob/v1.0.0/CHANGELOG.md>`_


Corrections
-----------

Find corrections in our bug tracking system under https://bugs.oxid-esales.com/changelog_page.php?version_id=712.


Installation
------------

To install or upgrade, follow the instructions in the *Installation* section:

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing a minor update <../../installation/update/minor-update>` |br|
:doc:`Installing a patch update <../../installation/update/patch-update>`

.. Intern: , Status:
