OXID eShop 6.0.4
================

Veröffentlichungstermin: 05.03.2019

-----------------------------------------------------------------------------------------

Allgemeines
-----------
Der OXID eShop 6.0.4 wird als Compilation bereitgestellt. Diese enthält folgende Komponenten:

* OXID eShop CE from version v6.2.1 to version v6.2.2
* OXID eShop PE from version v6.1.1 to version v6.1.2
* OXID eShop EE from version v6.1.2 to version v6.1.3
* Theme "Flow" 3.0.0
* Amazon Pay 3.1.4
* GDPR Opt-In 2.1.1
* Klarna 4.0.1
* Paymorrow 2.0.1
* PAYONE 1.0.8
* PayPal 5.2.2
* Summernote WYSIWIG-Editor und Mediathek 2.1.1
* Visual CMS 3.2.1 (PE/EE)

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.0.3…v6.0.4>`_.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
Der OXID eShop 6.0.3 läuft unter PHP 5.6 oder 7.0. Als Datenbank wird MySQL in der Version 5.5 oder 5.7 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

Installation
^^^^^^^^^^^^
Für die Installation, folgen Sie bitte den Anleitungen im Abschnitt "Installation":

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Update-Installation <../../installation/update-installation/update-installation>`

Bitte führen Sie das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, aus. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

-----------------------------------------------------------------------------------------

Korrekturen
-----------
Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet.

`<https://bugs.oxid-esales.com/changelog_page.php?version_id=458>`_

-----------------------------------------------------------------------------------------

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop CE können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.2.1...v6.2.2. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

.. Intern: oxbaio, Status: