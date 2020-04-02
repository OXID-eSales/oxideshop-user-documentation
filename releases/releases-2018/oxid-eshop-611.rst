OXID eShop 6.1.1
================

Veröffentlichungstermin: 30.10.2018

-----------------------------------------------------------------------------------------

Allgemeines
-----------
OXID eShop 6.1.1 wird als Compilation bereitgestellt. Diese enthält folgende Komponenten:

* OXID eShop CE 6.3.1
* OXID eShop PE 6.2.1
* OXID eShop EE 6.2.0
* Theme "Flow" 3.0.2
* AmazonPay 3.2.1
* GDPR Opt-In 2.1.2
* Klarna 4.2.0
* Paymorrow 2.0.1
* PAYONE 1.0.10
* PayPal 5.2.3
* Visual CMS 3.2.2 (PE/EE)
* Summernote WYSIWIG-Editor und die Mediathek 2.1.1

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.1.0...v6.1.1>`_.

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

* OXID eShop CE (Update von 6.3.0 auf 6.3.1), `Changelog 6.3.1 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.3.1/CHANGELOG.md>`_
* OXID eShop PE (Update von 6.2.0 auf 6.2.1)
* AmazonPay (Update von 3.1.4 auf 3.2.1), `Changelog 3.2.1 <https://github.com/bestit/amazon-pay-oxid/blob/3.2.1/CHANGELOG.md>`_
* GDPR Opt-In (Update von 2.1.1 auf 2.1.2), `Changelog 2.1.2 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.1.2/CHANGELOG.md>`_
* Klarna (Update von 4.0.1 auf 4.2.0), `Changelog 4.2.0 <https://github.com/topconcepts/OXID-Klarna-6/blob/master/CHANGELOG.md>`_
* PAYONE (Update von 1.0.8 auf 1.0.10), `Changelog 1.0.10 <https://github.com/PAYONE-GmbH/oxid-6/blob/1.0.10/Changelog.txt>`_
* PayPal (Update von 5.2.2 auf 5.2.3), `Changelog 5.2.3 <https://github.com/OXID-eSales/paypal/blob/v5.2.3/CHANGELOG.md>`_
* Visual CMS (PE/EE, Update von 3.2.1 auf 3.2.2)

-----------------------------------------------------------------------------------------

Korrekturen
-----------

Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet.

https://bugs.oxid-esales.com/changelog_page.php?version_id=462

-----------------------------------------------------------------------------------------

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.3.0...v6.3.1. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

.. Intern: oxbaim, Status: