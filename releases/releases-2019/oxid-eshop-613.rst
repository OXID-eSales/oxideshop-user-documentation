OXID eShop 6.1.3
================

Veröffentlichungstermin: 30.04.2019

-----------------------------------------------------------------------------------------

Allgemeines
-----------
OXID eShop 6.1.3 wird als Compilation bereitgestellt. Diese enthält u.a. folgende Komponenten:

* OXID eShop CE 6.3.3
* OXID eShop PE 6.2.2
* OXID eShop EE 6.2.2
* Theme "Flow" 3.2.0
* Theme "Wave" 1.1.0
* Amazon Pay 3.2.2
* GDPR Opt-In 2.1.2
* Klarna 4.2.2
* Paymorrow 2.0.1
* PAYONE 1.0.10
* PayPal 5.2.5
* Summernote WYSIWIG-Editor und Mediathek 2.2.0
* Visual CMS 3.3.1 (PE/EE)

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.1.2...v6.1.3>`_.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
OXID eShop 6.1.1 läuft unter PHP 7.0 und 7.1. Der Support für PHP 5.6 wurde eingestellt. Als Datenbank wird MySQL in der Version 5.5 oder 5.7 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

Installation
^^^^^^^^^^^^
Für die Installation, folgen Sie bitte den Anleitungen im Abschnitt "Installation":

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Update-Installation <../../installation/update-installation/update-installation>`

Bitte führen Sie das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, aus. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------

Aktualisierte Komponenten der OXID eShop Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Folgende Komponenten wurden auf eine neue Version aktualisiert:

* OXID eShop CE (Update von 6.3.2 auf 6.3.3), `Changelog 6.3.3 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.3.3/CHANGELOG.md>`_
* OXID eShop EE (Update von 6.2.1 auf 6.2.2)
* Theme "Flow" (Update von 3.1.0 auf 3.2.0), `Changelog 3.2.0 <https://github.com/OXID-eSales/flow_theme/blob/v3.2.0/CHANGELOG.md>`_
* Theme "Wave" (Update von 1.0.1 auf 1.1.0), `Changelog 1.1.0 <https://github.com/OXID-eSales/wave-theme/blob/v1.1.0/CHANGELOG.md>`_
* Klarna (Update von 4.2.1 auf 4.2.2), `Changelog 4.2.2 <https://github.com/topconcepts/OXID-Klarna-6/blob/master/CHANGELOG.md>`_
* PayPal (Update von 5.2.3 auf 5.2.5), `Changelog 5.2.5 <https://github.com/OXID-eSales/paypal/blob/v5.2.5/CHANGELOG.md>`_
* Visual CMS (PE/EE, Update von 3.3.0 auf 3.3.1)

-----------------------------------------------------------------------------------------

Korrekturen
-----------
Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet.

https://bugs.oxid-esales.com/changelog_page.php?version_id=492

-----------------------------------------------------------------------------------------

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop CE können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.3.2...v6.3.3. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

.. Intern: oxbaip, Status: