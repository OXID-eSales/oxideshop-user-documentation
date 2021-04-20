OXID eShop 6.3.0
================

Veröffentlichungstermin: 20.04.2021

-----------------------------------------------------------------------------------------

Allgemeines
-----------
OXID eShop 6.3.0 wird als Compilation bereitgestellt. Diese enthält u.a. folgende Komponenten:

* OXID eShop CE 6.8.0
* OXID eShop PE 6.5.0
* OXID eShop EE 6.6.0
* Theme "Flow" 3.7.0
* Theme "Wave" 1.6.0
* Amazon Pay 3.6.8
* GDPR Opt-In 2.3.3
* Klarna 5.5.0
* OXID Cookie Management powered by usercentrics 1.1.3
* Paymorrow 2.0.4
* PAYONE 1.3.1
* PayPal 6.2.3
* WYSIWYG Editor + Mediathek 2.4.0
* Visual CMS 3.5.3 (PE/EE)

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.2.3...v6.3.0>`_.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
OXID eShop 6.3.0 läuft unter PHP 8.0, 7.4 und 7.3.

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

Neue Funktionen
---------------
Unterstützung von PHP 8.0
^^^^^^^^^^^^^^^^^^^^^^^^^
OXID eShop 6.3.0 läuft jetzt auch unter PHP 8.0. Die Unterstützung für PHP 7.1 und 7.2 wurde eingestellt.

Neue Komponente der OXID eShop Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Die OXID eShop Compilation wurde durch das Modul OXID Cookie Management powered by usercentrics 1.1.3 erweitert. Das Modul stellt Funktionen bereit, um die im OXID eShop verwendeten Web-Tracking-Technologien mit den rechtlichen Anforderungen in Einklang zu bringen. Das wird durch die Integration der Content Management Platform (CMS) von Usercentrics umgesetzt.

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------
Folgende Komponenten wurden auf eine neue Version aktualisiert:

* OXID eShop CE (Update von 6.6.0 auf 6.8.0), `Changelog 6.8.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.8.0/CHANGELOG.md>`_
* OXID eShop PE (Update von 6.4.1 auf 6.5.0)
* OXID eShop EE (Update von 6.5.4 auf 6.6.0)
* Theme "Flow" (Update von 3.6.0 auf 3.7.0), `Changelog 3.7.0 <https://github.com/OXID-eSales/flow_theme/blob/v3.7.0/CHANGELOG.md>`_
* Theme "Wave" (Update von 1.5.0 auf 1.6.0), `Changelog 1.6.0 <https://github.com/OXID-eSales/wave-theme/blob/v1.6.0/CHANGELOG.md>`_
* GDPR Opt-In (Update von 2.3.1 auf 2.3.3), `Changelog 2.3.3 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics 1.1.3, `Changelog 1.1.3 <https://github.com/OXID-eSales/usercentrics/blob/v1.1.3/CHANGELOG.md>`_
* OXID eShop DemoData installer (Update von 1.1.2 auf 1.1.3)
* Amazon Pay (Update von 3.6.4 auf 3.6.8), `Changelog 3.6.8 <https://github.com/bestit/amazon-pay-oxid/blob/3.6.8/CHANGELOG.md>`_
* Klarna (Update von 5.3.0 auf 5.5.0), `Changelog 5.5.0 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.0/CHANGELOG.md>`_
* Paymorrow (Update von 2.0.3 auf 2.0.4) `Changelog 2.0.4 <https://github.com/OXID-eSales/paymorrow-module/blob/v2.0.4/CHANGELOG.md>`_
* PayPal (Update von 6.2.1 auf 6.2.3), `Changelog 6.2.3 <https://github.com/OXID-eSales/paypal/blob/v6.2.3/CHANGELOG.md>`_
* OXID eShop composer plugin (Update von 5.1.0 auf 5.2.0) `Changelog 5.2.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.2.0/CHANGELOG.md>`_
* OXID eShop DemoData installer (Update von 1.1.2 auf 1.2.0)
* OXID eShop doctrine migration integration (Update von 3.1.1 auf 3.2.0) `Changelog 3.2.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v3.2.0/CHANGELOG.md>`_
* Unified Namespace Generator (Update von 2.1.0 auf 2.2.0) `Changelog 2.2.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v2.2.0/CHANGELOG.md>`_

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop CE können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.6.0...v6.8.0. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

-----------------------------------------------------------------------------------------

Korrekturen
-----------
Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet. |br|
https://bugs.oxid-esales.com/changelog_page.php?version_id=528


.. Intern: oxbajs, Status: