OXID eShop 6.2.3
================

Veröffentlichungstermin: 24.11.2020

-----------------------------------------------------------------------------------------

Allgemeines
-----------
OXID eShop 6.2.3 wird als Compilation bereitgestellt. Diese enthält u.a. folgende Komponenten:

* OXID eShop CE 6.6.0
* OXID eShop PE 6.4.1
* OXID eShop EE 6.5.4
* Theme "Flow" 3.6.0
* Theme "Wave" 1.5.0
* Amazon Pay 3.6.4
* GDPR Opt-In 2.3.1
* Klarna 5.3.0
* Paymorrow 2.0.3
* PAYONE 1.3.1
* PayPal 6.2.1
* WYSIWYG Editor + Mediathek 2.4.0
* Visual CMS 3.5.3 (PE/EE)

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.2.2...v6.2.3>`_.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
OXID eShop 6.2.3 läuft unter PHP 7.1 bis 7.4. Als Datenbank wird MySQL in der Version 5.5 oder 5.7 und MariaDB in der Version 10.4 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

Mit OXID eShop 6.2.3 werden die Versionen 1 und 2 von Composer unterstützt.

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

* OXID eShop CE (Update von 6.5.6 auf 6.6.0), `Changelog 6.6.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.6.0/CHANGELOG.md>`_
* OXID eShop EE (Update von 6.5.3 auf 6.5.4)
* Theme "Flow" (Update von 3.5.0 auf 3.6.0), `Changelog 3.6.0 <https://github.com/OXID-eSales/flow_theme/blob/v3.6.0/CHANGELOG.md>`_
* Theme "Wave" (Update von 1.4.0 auf 1.5.0), `Changelog 1.5.0 <https://github.com/OXID-eSales/wave-theme/blob/v1.5.0/CHANGELOG.md>`_
* Klarna (Update von 5.1.4 auf 5.3.0), `Changelog 5.3.0 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.3.0/CHANGELOG.md>`_
* PayPal (Update von 6.2.0 auf 6.2.1), `Changelog 6.2.1 <https://github.com/OXID-eSales/paypal/blob/v6.2.1/CHANGELOG.md>`_
* WYSIWYG Editor + Mediathek (Update von 2.3.0 auf 2.4.0), `Changelog 2.4.0 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v2.4.0/CHANGELOG.md>`_
* Visual CMS, PE/EE (Update von 3.4.0 auf 3.5.3)
* OXID eShop composer plugin (Update von 5.0.1 auf 5.1.0), `Changelog 5.1.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.1.0/CHANGELOG.md>`_
* OXID eShop doctrine migration integration (Update von 2.1.3 auf 3.1.1), `Changelog 3.1.1 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v3.1.1/CHANGELOG.md>`_
* Unified Namespace Generator (Update von 2.0.1 auf 2.1.0), `Changelog 2.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v2.1.0/CHANGELOG.md>`_

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop CE können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.5.6...v6.6.0. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

-----------------------------------------------------------------------------------------

Korrekturen
-----------
Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet. |br|
https://bugs.oxid-esales.com/changelog_page.php?version_id=578


.. Intern: oxbajq, Status: