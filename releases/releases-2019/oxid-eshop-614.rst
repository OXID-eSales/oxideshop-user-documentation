OXID eShop 6.1.4
================

Veröffentlichungstermin: 30.07.2019

-----------------------------------------------------------------------------------------

Allgemeines
-----------
Der OXID eShop 6.1.4 wird als Compilation bereitgestellt. Diese enthält u.a. folgende Komponenten:

* OXID eShop CE 6.3.5
* OXID eShop PE 6.2.2
* OXID eShop EE 6.2.3
* Theme "Flow" 3.3.0
* Theme "Wave" 1.2.0
* Amazon Pay 3.3.1
* GDPR Opt-In 2.2.0
* Klarna 4.3.0
* Paymorrow 2.0.1
* PAYONE 1.0.10
* PayPal 5.2.5
* Summernote WYSIWIG-Editor und Mediathek 2.2.0
* Visual CMS 3.3.2 (PE/EE)

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.1.3...v6.1.4>`_.

Mit OXID eShop 6.1.4 wurde eine Sicherheitslücke geschlossen: über eine speziell gestaltete URL kann ein Angreifer vollen Zugriff auf den Administrationsbereich erhalten. Details zur Sicherheitslücke finden Sie auf folgender Seite der OXIDforge: `Security Bulletin 2019-001 <https://oxidforge.org/de/security-bulletin-2019-001.html>`_. Wir empfehlen ein schnelles Update auf diese Shopversion. Eine Anleitung zum Shop-Update finden Sie unter `Update-Installation <https://docs.oxid-esales.com/eshop/de/6.1/installation/update-installation/update-installation.html>`_.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
OXID eShop 6.1.4 läuft unter PHP 7.0 und 7.1. Als Datenbank wird MySQL in der Version 5.5 oder 5.7 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

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

* OXID eShop CE (Update von 6.3.3 auf 6.3.5), `Changelog 6.3.5 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.3.5/CHANGELOG.md>`_
* OXID eShop EE (Update von 6.2.2 auf 6.2.3)
* Theme "Flow" (Update von 3.2.0 auf 3.3.0), `Changelog 3.3.0 <https://github.com/OXID-eSales/flow_theme/blob/v3.3.0/CHANGELOG.md>`_
* Theme "Wave" (Update von 1.1.0 auf 1.2.0), `Changelog 1.2.0 <https://github.com/OXID-eSales/wave-theme/blob/v1.2.0/CHANGELOG.md>`_
* Klarna (Update von 4.2.2 auf 4.3.0), `Changelog 4.3.0 <https://github.com/topconcepts/OXID-Klarna-6/blob/v4.3.0/CHANGELOG.md>`_
* Amazon Pay (Update von 3.2.2 auf 3.3.1), `Changelog 3.3.1 <https://github.com/bestit/amazon-pay-oxid/blob/3.3.1/CHANGELOG.md>`_
* GDPR Opt-In (Update von 2.1.2 auf 2.2.0), `Changelog 2.2.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.2.0/CHANGELOG.md>`_
* Visual CMS (PE/EE, Update von 3.3.0 auf 3.3.1)

-----------------------------------------------------------------------------------------

Korrekturen
-----------
Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet.

https://bugs.oxid-esales.com/changelog_page.php?version_id=504

-----------------------------------------------------------------------------------------

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop CE können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.3.3...v6.3.5. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

.. Intern: oxbair, Status: