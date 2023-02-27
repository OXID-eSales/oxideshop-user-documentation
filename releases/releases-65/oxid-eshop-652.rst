OXID eShop 6.5.2
================

Veröffentlichungstermin: 28.02.2023

Mit OXID eShop 6.5.2 schließen wir ein potentielle Sicherheitslücke.

.. todo: #VL: Drücken wir es so aus?

Wenn in einem Request eine Sitzungs-ID gesendet worden wäre, hätte ein Angreifer auf das Konto eines anderen Kunden zugreifen können.

.. todo: #tbd: Link auf Sicherheits-Bulletin unter

Weitere Informationen finden Sie in unserem Sicherheits-Bulletin unter

Mit PAYONE 1.8.0 stehen neue Zahlungsarten zur Auswahl.

Ausßerdem haben wir kleinere Fehler verbessert.


.. todo: #VL: gibt es eine tracking-ID für Bug fixes?

Außerdem haben wir Bugs behoben. Siehe :ref:`releases/releases-65/oxid-eshop-652:Korrekturen`.

Verbesserungen und Anpassungen
------------------------------

Sehen Sie Änderungen in der Compilation in den Metapackages ein:

.. todo: #VL: Warum gehören PE und EE bisher nicht zu unserer Liste der Module in der Compilation unten?

* CE: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.5.1...v6.5.2>`_
* PE: `<https://github.com/OXID-eSales/oxideshop_metapackage_pe/compare/v6.5.1...v6.5.2>`_
* EE: `<https://github.com/OXID-eSales/oxideshop_metapackage_ee/compare/v6.5.1...v6.5.2>`_

Aktualisierte Komponenten
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Folgende Komponenten und Module haben wir aktualisiert:

.. todo: #VL: Folgendes ist aktualisiert gemäß https://core-ci-resources.oxid-esales.com/static-files/BgnUABZOLVTZGuwmvhxWaaKJWeIg_4SQuDwma1g70xIxNjc3NDg2ODEyMDMyOjg6bmFidXNzYW46dXNlckNvbnRlbnQ=/wiki_t1/shop/changelog/changelog_v6.5.2.html

* OXID eShop CE (Update von 6.13.0 zu 6.14.0): `Changelog 6.14.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.14.0/CHANGELOG.md>`_
* OXID eShop PE (Update von 6.5.2 zu 6.5.3: `Changelog 6.5.3 <https://github.com/OXID-eSales/oxideshop_pe/blob/v6.5.3/CHANGELOG.md>`_
* OXID eShop PE (Update von 6.8.0 zu 6.8.1: `Changelog 6.8.1 <https://github.com/OXID-eSales/oxideshop_ee/blob/v6.8.1/CHANGELOG.md>`_
* WYSIWYG Editor + Mediathek (Update von 2.4.1 zu 2.4.2): `Changelog 2.4.2 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v2.4.2/CHANGELOG.md>`_
* PAYONE (Update von 1.7.0 zu 1.8.0): `Changelog 1.80 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.8.0/Changelog.txt>`_

Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält folgende Komponenten:

.. todo: #VL: gehören PE und EE nicht dazu (s. oben)?

* OXID eShop CE 6.14.0: `Changelog 6.14.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.14.0/CHANGELOG.md>`_
* OXID eShop composer plugin 5.2.2: `Changelog 5.2.2 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.2.2/CHANGELOG.md>`_
* Theme "Flow" 3.8.1: `Changelog 3.8.1 <https://github.com/OXID-eSales/flow_theme/blob/v3.8.1/CHANGELOG.md>`_
* Theme "Wave" 1.8.0: `Changelog 1.8.0 <https://github.com/OXID-eSales/wave-theme/blob/v1.8.0/CHANGELOG.md>`_
* GDPR Opt-In 2.3.3: `Changelog 2.3.3 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* Klarna 5.5.3: `Changelog 5.5.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.3/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics 1.2.1: `Changelog 1.2.1 <https://github.com/OXID-eSales/usercentrics/blob/v1.2.1/CHANGELOG.md>`_
* PAYONE 1.8.0: `Changelog 1.8.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.8.0/Changelog.txt>`_
* PayPal 6.5.0: `Changelog 6.5.0 <https://github.com/OXID-eSales/paypal/blob/v6.5.0/CHANGELOG.md>`_
* WYSIWYG Editor + Mediathek 2.4.2: `Changelog 2.4.2 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v2.4.2/CHANGELOG.md>`_
* Makaira 1.4.2: `Changelog 1.4.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/1.4.2/CHANGELOG.md>`_
* Unzer Payment für OXID 1.0.0 (EE): `Changelog 1.0.0 <https://github.com/OXID-eSales/unzer-module/blob/v1.0.0/CHANGELOG.md>`_


Korrekturen
-----------

.. todo: #VL: gibt es weitere Korrekturen?- Haben wir eine Tracking-ID?

Korrekturen finden Sie in unserem Bugtracking-System unter https://bugs.oxid-esales.com/changelog_page.php?version_id=712.


Installation
------------

Zum Installieren oder Aktualisieren folgen Sie den Anleitungen im Abschnitt *Installation*:


:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Minor Update installieren <../../installation/update/minor-update>` |br|
:doc:`Patch-Update installieren <../../installation/update/patch-update>`

.. Intern: , Status:
