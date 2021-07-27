OXID eShop 6.3.1
================

Veröffentlichungstermin: 03.08.2021

-----------------------------------------------------------------------------------------

Allgemeines
-----------
OXID eShop 6.3.1 wird als Compilation bereitgestellt. Diese enthält u.a. folgende Komponenten:

* OXID eShop CE 6.9.0
* OXID eShop PE 6.5.1
* OXID eShop EE 6.6.1
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

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.3.0...v6.3.1>`_.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
OXID eShop 6.3.1 läuft unter PHP 8.0, 7.4 und 7.3.

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

* OXID eShop CE (Update von 6.8.0 auf 6.9.0), `Changelog 6.9.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.9.0/CHANGELOG.md>`_
* OXID eShop PE (Update von 6.5.0 auf 6.5.1)
* OXID eShop EE (Update von 6.6.0 auf 6.6.1)
* Theme "Flow" (Update von 3.7.0 auf 3.7.2), `Changelog 3.7.2 <https://github.com/OXID-eSales/flow_theme/blob/v3.7.2/CHANGELOG.md>`_
* Theme "Wave" (Update von 1.6.0 auf 1.6.1), `Changelog 1.6.1 <https://github.com/OXID-eSales/wave-theme/blob/v1.6.1/CHANGELOG.md>`_
* Klarna (Update von 5.5.0 auf 5.5.1), `Changelog 5.5.1 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.1/CHANGELOG.md>`_
* Paymorrow (Update von 2.0.4 auf 2.1.0) `Changelog 2.1.0 <https://github.com/OXID-eSales/paymorrow-module/blob/v2.1.0/CHANGELOG.md>`_
* PAYONE (Update von 1.3.1 auf 1.5.0), `Changelog 1.5.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.5.0/Changelog.txt>`_
* PayPal (Update von 6.2.3 auf 6.3.1), `Changelog 6.3.1 <https://github.com/OXID-eSales/paypal/blob/v6.3.1/CHANGELOG.md>`_

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop CE können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.8.0...v6.9.0. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

-----------------------------------------------------------------------------------------

Korrekturen
-----------
Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet. |br|
https://bugs.oxid-esales.com/changelog_page.php?version_id=626


.. Intern: oxbajw, Status: