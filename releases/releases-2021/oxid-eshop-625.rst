OXID eShop 6.2.5
================

Veröffentlichungstermin: 03.08.2021

-----------------------------------------------------------------------------------------

Allgemeines
-----------
OXID eShop 6.2.5 wird als Compilation bereitgestellt. Diese enthält u.a. folgende Komponenten:

* OXID eShop CE 6.7.2
* OXID eShop PE 6.4.1
* OXID eShop EE 6.5.5
* Theme "Flow" 3.7.2
* Theme "Wave" 1.6.1
* Amazon Pay 3.6.8
* GDPR Opt-In 2.3.3
* Klarna 5.5.1
* OXID Cookie Management powered by usercentrics 1.1.3
* Paymorrow 2.1.0
* PAYONE 1.5.0
* PayPal 6.3.1
* WYSIWYG Editor + Mediathek 2.4.0
* Visual CMS 3.5.3 (PE/EE)

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.2.4...v6.2.5>`_.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
OXID eShop 6.2.5 läuft unter PHP 7.1 bis 7.4.

Als Datenbank wird MySQL in der Version 5.5 oder 5.7 und MariaDB in der Version 10.4 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_.

Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

Composer wird in den Versionen 1 und 2 unterstützt.

Installation
^^^^^^^^^^^^
Für die Installation, folgen Sie bitte den Anleitungen im Abschnitt "Installation":

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Update <../../installation/update/update>`

Bitte führen Sie das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, aus. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------
Folgende Komponenten wurden auf eine neue Version aktualisiert:

* OXID eShop CE (Update von 6.7.0 auf 6.7.2), `Changelog 6.7.2 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.7.2/CHANGELOG.md>`_
* Theme "Flow" (Update von 3.7.0 auf 3.7.2), `Changelog 3.7.2 <https://github.com/OXID-eSales/flow_theme/blob/v3.7.2/CHANGELOG.md>`_
* Theme "Wave" (Update von 1.6.0 auf 1.6.1), `Changelog 1.6.1 <https://github.com/OXID-eSales/wave-theme/blob/v1.6.1/CHANGELOG.md>`_
* GDPR Opt-In (Update von 2.3.2 auf 2.3.3), `Changelog 2.3.3 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics (Update von 1.1.2 auf 1.1.3), `Changelog 1.1.3 <https://github.com/OXID-eSales/usercentrics/blob/v1.1.3/CHANGELOG.md>`_
* Klarna (Update von 5.5.0 auf 5.5.1), `Changelog 5.5.1 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.1/CHANGELOG.md>`_
* Paymorrow (Update von 2.0.3 auf 2.1.0), `Changelog 2.1.0 <https://github.com/OXID-eSales/paymorrow-module/blob/v2.1.0/CHANGELOG.md>`_
* PAYONE (Update von 1.3.1 auf 1.5.0), `Changelog 1.5.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.5.0/Changelog.txt>`_
* PayPal (Update von 6.2.2 auf 6.3.1), `Changelog 6.3.1 <https://github.com/OXID-eSales/paypal/blob/v6.3.1/CHANGELOG.md>`_
* OXID eShop composer plugin (Update von 5.1.0 auf 5.2.0), `Changelog 5.2.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.2.0/CHANGELOG.md>`_
* OXID eShop DemoData installer (Update von 1.1.3 auf 1.2.0)
* OXID eShop facts (Update von 2.3.2 auf 2.4.0), `Changelog 2.4.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v2.4.0/CHANGELOG.md>`_
* Unified Namespace Generator (Update von 2.1.0 auf 2.2.0), `Changelog 2.2.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v2.2.0/CHANGELOG.md>`_

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop CE können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.7.0...v6.7.2. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

-----------------------------------------------------------------------------------------

Korrekturen
-----------
Keine Korrekturen für OXID eShop 6.2.5


.. Intern: oxbajv, Status: