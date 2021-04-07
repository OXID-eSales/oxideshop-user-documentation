OXID eShop 6.3.0
================

Veröffentlichungstermin: 20.04.2021

-----------------------------------------------------------------------------------------

Allgemeines
-----------
OXID eShop 6.3.0 wird als Compilation bereitgestellt. Diese enthält u.a. folgende Komponenten:

* OXID eShop CE ???
* OXID eShop PE ???
* OXID eShop EE ???
* Theme "Flow" 3.7.0
* Theme "Wave" 1.6.0
* Amazon Pay 3.6.8
* GDPR Opt-In 2.3.2
* Klarna 5.4.0
* OXID Cookie Management powered by usercentrics 1.1.2
* Paymorrow 2.0.3
* PAYONE 1.3.1
* PayPal 6.2.2
* WYSIWYG Editor + Mediathek 2.4.0
* Visual CMS 3.5.3 (PE/EE)

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.2.3...v6.3.0>`_.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
OXID eShop 6.3.0 läuft unter PHP 8.0, 7.4 und 7.3.

Als Datenbank wird MySQL in der Version 5.5 oder 5.7 und MariaDB in der Version 10.4 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden. Composer wird in den Versionen 1 und 2 unterstützt.

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
Die OXID eShop Compilation wurde durch das Modul OXID Cookie Management powered by usercentrics 1.1.2 erweitert. Das Modul stellt Funktionen bereit, um die im OXID eShop verwendeten Web-Tracking-Technologien mit den rechtlichen Anforderungen in Einklang zu bringen. Das wird durch die Integration der Content Management Platform (CMS) von Usercentrics umgesetzt.

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------
Folgende Komponenten wurden auf eine neue Version aktualisiert:

* ??? OXID eShop CE (Update von 6.6.0 auf 6.6.x), `Changelog 6.6.x <https://github.com/OXID-eSales/oxideshop_ce/blob/dev-b-6.2.x/CHANGELOG.md>`_
* ??? OXID eShop PE (Update von 6.4.1 auf 6.4.x)
* ??? OXID eShop EE (Update von 6.5.4 auf 6.5.x)
* Theme "Flow" (Update von 3.6.0 auf 3.7.0), `Changelog 3.7.0 <https://github.com/OXID-eSales/flow_theme/blob/v3.7.0/CHANGELOG.md>`_
* Theme "Wave" (Update von 1.5.0 auf 1.6.0), `Changelog 1.6.0 <https://github.com/OXID-eSales/wave-theme/blob/v1.6.0/CHANGELOG.md>`_
* GDPR Opt-In (Update von 2.3.1 auf 2.3.2), `Changelog 2.3.2 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.2/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics 1.1.2, `Changelog 1.1.2 <https://github.com/OXID-eSales/usercentrics/blob/v1.1.2/CHANGELOG.md>`_
* OXID eShop DemoData installer (Update von 1.1.2 auf 1.1.3)
* Amazon Pay (Update von 3.6.4 auf 3.6.8), `Changelog 3.6.8 <https://github.com/bestit/amazon-pay-oxid/blob/3.6.8/CHANGELOG.md>`_
* PayPal (Update von 6.2.1 auf 6.2.2), `Changelog 6.2.2 <https://github.com/OXID-eSales/paypal/blob/v6.2.2/CHANGELOG.md>`_
* Klarna (Update von 5.3.0 auf 5.4.0), `Changelog 5.4.0 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.4.0/CHANGELOG.md>`_

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop CE können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.6.0…v6.6.x. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

-----------------------------------------------------------------------------------------

Korrekturen
-----------
Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet. |br|
https://bugs.oxid-esales.com/changelog_page.php?version_id=???


.. Intern: oxbajs, Status: