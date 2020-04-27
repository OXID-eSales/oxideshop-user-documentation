OXID eShop 6.2.1
================

Veröffentlichungstermin: 28.04.2020

-----------------------------------------------------------------------------------------

Allgemeines
-----------
OXID eShop 6.2.1 wird als Compilation bereitgestellt. Diese enthält u.a. folgende Komponenten:

* OXID eShop CE 6.5.4
* OXID eShop PE 6.4.0
* OXID eShop EE 6.5.2
* Theme "Flow" 3.4.1
* Theme "Wave" 1.3.1
* Amazon Pay 3.6.4
* GDPR Opt-In 2.3.0
* Klarna 5.1.4
* Paymorrow 2.0.3
* PAYONE 1.3.1
* PayPal 6.1.0
* Summernote WYSIWIG-Editor und Mediathek 2.2.0
* Visual CMS 3.3.3 (PE/EE)

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.2.0...v6.2.1>`_.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
OXID eShop 6.2.1 läuft unter PHP 7.1 bis 7.4. Als Datenbank wird MySQL in der Version 5.5 oder 5.7 und MariaDB in der Version 10.4 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

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

* OXID eShop CE (Update von 6.5.3 auf 6.5.4), `Changelog 6.5.4 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.5.4/CHANGELOG.md>`_
* OXID eShop EE (Update von 6.5.1 auf 6.5.2)
* OXID eShop Demodaten CE (Update von 6.0.3 auf 6.0.4)
* OXID eShop Demodaten PE (Update von 6.0.3 auf 6.0.4)
* OXID eShop Demodaten EE (Update von 6.0.3 auf 6.0.4)
* OXID eShop Composer Plugin (Update von 4.1.0 auf 4.1.1), `Changelog 4.1.1 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v4.1.1/CHANGELOG.md>`_
* OXID eShop Views Generator (Update von 1.2.0 auf 1.3.0)

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop CE können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.5.3...v6.5.4. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

-----------------------------------------------------------------------------------------

Korrekturen
-----------
Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet.

https://bugs.oxid-esales.com/changelog_page.php?version_id=563


.. Intern: oxbajl, Status: