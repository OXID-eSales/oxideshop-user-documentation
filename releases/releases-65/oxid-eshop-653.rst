OXID eShop 6.5.3
================

Veröffentlichungstermin: 01.08.2023

Mit OXID eShop 6.5.3 schließen wir eine Sicherheitslücke.

Das von einer Sicherheitslücke (NVD - CVE-2022-24775) betroffene Paket :technicalname:`guzzlehttp/psr7` Version 2.4.3 ist nicht mehr in der OXID eShop EE Compilation enthalten. Das Paket wurde als Abhängigkeit durch Version 1.0.1 des Zahlungsmoduls :productname:`Unzer Payment for OXID` Teil der EE Compilation.

Durch fehlerhaftes Parsen von Headern wäre es in Spezialfällen möglich, in einem Header nach einem Zeilenumbruch zusätzliche Werte zu übergeben.

Klassifiziert wurde die Schwachstelle durch CWE als CWE-20. Wie sich eine durchgeführte Attacke auswirken würde, ist nicht bekannt.

Weitere Verbesserungen:

* Mit PAYONE 1.9.0 stehen neue Zahlungsarten zur Auswahl.
* Mit Unzer 1.1.1 steht mit Unzer Kauf auf Rechnung (Paylater) eine neue Bezahlmethode zur Verfügung. Außerdem haben wir zahlreiche Verbesserungen am Modul vorgenommen.
* Makaira 1.4.5 enthält Verbesserungen.

Außerdem haben wir kleinere Fehler verbessert.


Verbesserungen und Anpassungen
------------------------------

Änderungen in der Compilation finden Sie im Metapackage unter `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.5.2...v6.5.3>`_.


Aktualisierte Komponenten
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Folgende Komponenten und Module haben wir aktualisiert:

* OXID eShop CE (Update von 6.14.0 zu 6.14.1): `Changelog 6.14.1 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.14.1/CHANGELOG.md>`_
* PAYONE (Update von 1.8.0 zu 1.9.0): `Changelog 1.9.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.9.0/Changelog.txt>`_
* Unzer Modul (Update von 1.0.1 zu 1.1.1): `Changelog 1.1.1 <https://github.com/OXID-eSales/unzer-module/blob/v1.1.1/CHANGELOG.md>`_
* Makaira (Update von 1.4.3 zu 1.4.5): `Changelog 1.4.5 <https://github.com/MakairaIO/oxid-connect-essential/blob/1.4.5/CHANGELOG.md>`_


Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält folgende Komponenten:

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

Zum Installieren oder Aktualisieren folgen Sie den Anleitungen im Abschnitt *Installation*:


:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Minor Update installieren <../../installation/update/minor-update>` |br|
:doc:`Patch-Update installieren <../../installation/update/patch-update>`

.. Intern: , Status:


