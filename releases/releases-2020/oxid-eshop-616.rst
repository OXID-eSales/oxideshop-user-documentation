OXID eShop 6.1.6
================

Veröffentlichungstermin: 31.03.2020

-----------------------------------------------------------------------------------------

Allgemeines
-----------
Der OXID eShop 6.1.6 wird als Compilation bereitgestellt. Diese enthält u.a. folgende Komponenten:

* OXID eShop CE 6.3.7
* OXID eShop PE 6.2.3
* OXID eShop EE 6.2.4
* Theme "Flow" 3.4.1
* Theme "Wave" 1.3.1
* Amazon Pay 3.3.1
* GDPR Opt-In 2.2.0
* Klarna 5.1.3
* Paymorrow 2.0.1
* PAYONE 1.3.1
* PayPal 5.3.1
* Summernote WYSIWIG-Editor und Mediathek 2.2.0
* Visual CMS 3.3.3 (PE/EE)

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.1.5...v6.1.6>`_.

Der OXID eShop 6.1.6 enthält einen Security Fix für das Zahlungsmodul PAYONE. Wir empfehlen ein schnelles Update auf diese Shopversion.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
Der OXID eShop 6.1.6 läuft unter PHP 7.0 und 7.1. Als Datenbank wird MySQL in der Version 5.5 oder 5.7 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

Installation
^^^^^^^^^^^^
Für die Installation, folgen Sie bitte den Anleitungen im Abschnitt "Installation":

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Update-Installation <../../installation/update-installation/update-installation>`

Bitte führen Sie das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, aus. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

Der OXID eShop 6.0.* hat nun EOL (End of Life) erreicht und wird nicht mehr unterstützt. Bitte führen Sie ein Update aus, falls Sie noch einen Shop dieser Serie einsetzen.

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------
Folgende Komponenten wurden auf eine neue Version aktualisiert:

* OXID eShop CE (Update von 6.3.6 auf 6.3.7), `Changelog 6.3.7 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.3.7/CHANGELOG.md>`_
* OXID eShop PE (Update von 6.2.2 auf 6.2.3)
* OXID eShop EE (Update von 6.2.3 auf 6.2.4)
* OXID eShop facts (Update von 2.3.1 auf 2.3.2), `Changelog 2.3.2 <https://github.com/OXID-eSales/oxideshop-facts/blob/v2.3.2/CHANGELOG.md/>`_
* Theme "Flow" (Update von 3.3.0 auf 3.4.1), `Changelog 3.4.1 <https://github.com/OXID-eSales/flow_theme/blob/v3.4.1/CHANGELOG.md>`_
* Theme "Wave" (Update von 1.2.0 auf 1.3.1), `Changelog 1.3.1 <https://github.com/OXID-eSales/wave-theme/blob/v1.3.1/CHANGELOG.md/>`_
* Klarna (Update von 4.3.0 auf 5.1.3), `Changelog 5.1.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.1.3/CHANGELOG.md>`_
* PAYONE (Update von 1.0.10 auf 1.3.1), `Changelog v1.3.1 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.3.1/Changelog.txt>`_
* PayPal (Update von 5.2.5 auf 5.3.1), `Changelog 5.3.1 <https://github.com/OXID-eSales/paypal/blob/v5.3.1/CHANGELOG.md>`_
* Visual CMS (PE/EE, Update von 3.3.2 auf 3.3.3)

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop CE können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.3.6...v6.3.7. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

-----------------------------------------------------------------------------------------

Korrekturen
-----------
Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet.

https://bugs.oxid-esales.com/changelog_page.php?version_id=541


.. Intern: oxbaja, Status: