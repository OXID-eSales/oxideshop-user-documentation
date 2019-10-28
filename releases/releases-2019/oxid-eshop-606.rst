OXID eShop 6.0.6
================

Veröffentlichungstermin: 29.10.2019

-----------------------------------------------------------------------------------------

Allgemeines
-----------
Der OXID eShop 6.0.6 wird als Compilation bereitgestellt. Diese enthält folgende Komponenten:

* OXID eShop CE 6.2.4
* OXID eShop PE 6.1.2
* OXID eShop EE 6.1.3
* Theme "Flow" 3.0.0
* Amazon Pay 3.1.4
* GDPR Opt-In 2.1.1
* Klarna 4.0.1
* Paymorrow 2.0.1
* PAYONE 1.0.8
* PayPal 5.2.2
* Summernote WYSIWIG-Editor und Mediathek 2.1.1
* Visual CMS 3.2.1 (PE/EE)

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.0.5…v6.0.6>`_.

Mit OXID eShop 6.0.6 wurde eine Sicherheitslücke geschlossen. Details dazu werden am 05.11.2019 im "Security Bulletin 2019-002" auf der `OXIDforge <https://oxidforge.org/de>`_ veröffentlicht. Wir empfehlen ein schnelles Update auf diese Shopversion. Eine Anleitung zum Shop-Update finden Sie unter `Update-Installation <https://docs.oxid-esales.com/eshop/de/6.0/installation/update-installation/update-installation.html>`_.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
Der OXID eShop 6.0.6 läuft unter PHP 5.6 oder 7.0. Als Datenbank wird MySQL in der Version 5.5 oder 5.7 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

Installation
^^^^^^^^^^^^
Für die Installation, folgen Sie bitte den Anleitungen im Abschnitt "Installation":

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Update-Installation <../../installation/update-installation/update-installation>`

Bitte führen Sie das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, aus. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------
Die Komponente OXID eShop CE wurde von Version 6.2.3 auf 6.2.4 aktualisiert. Siehe `Changelog 6.2.4 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.2.4/CHANGELOG.md>`_.

-----------------------------------------------------------------------------------------

Korrekturen
-----------
Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet.

https://bugs.oxid-esales.com/changelog_page.php?version_id=525

-----------------------------------------------------------------------------------------

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop CE können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.2.3...v6.2.4. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.


.. Intern: oxbaiz, Status: