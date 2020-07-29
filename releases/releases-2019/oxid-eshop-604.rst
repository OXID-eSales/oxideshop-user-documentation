OXID eShop 6.0.4
================

Veröffentlichungstermin: 05.03.2019

-----------------------------------------------------------------------------------------

Allgemeines
-----------
OXID eShop 6.0.4 wird als Compilation bereitgestellt. Diese enthält folgende Komponenten:

* OXID eShop CE 6.2.2
* OXID eShop PE 6.1.2
* OXID eShop EE 6.1.3
* Theme "Flow" 3.0.0
* Amazon Pay 3.1.4
* GDPR Opt-In 2.1.1
* Klarna 4.0.1
* Paymorrow 2.0.1
* PAYONE 1.0.8
* PayPal 5.2.2
* WYSIWIG Editor + Mediathek 2.1.1
* Visual CMS 3.2.1 (PE/EE)

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.0.3…v6.0.4>`_.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
OXID eShop 6.0.3 läuft unter PHP 5.6 oder 7.0. Als Datenbank wird MySQL in der Version 5.5 oder 5.7 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

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

* OXID eShop CE (Update von 6.2.1 auf 6.2.2), `Changelog 6.2.2 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.2.2/CHANGELOG.md>`_
* OXID eShop PE (Update von 6.1.1 auf 6.1.2)
* OXID eShop EE (Update von 6.1.2 auf 6.1.3)

Es wurde ein Fehler in einer Funktion der Enterprise Edition behoben. Die Korrektur erforderte auch Änderungen in der Community und Professional Edition.

Diverse Anpassungen
^^^^^^^^^^^^^^^^^^^
* In den Komponenten OXID eShop facts und Doctrine Migration Integration werden die Tests nicht mehr per Composer ausgeliefert. Falls diese benötigt werden, können sie mit der Composer-Option ``--prefer-source`` oder per ``git clone`` des jeweiligen Repositories bezogen werden.
* In Doctrine Migration Wrapper sind mit PR-4 verschiedene Typen von Output-Handlern, wie beispielsweise BufferdOutput, möglich. Bislang konnte im Shop nur ConsoleOutput verarbeitet werden. Mehr Informationen dazu in der Dokumentation der `Symfony API <https://api.symfony.com>`_.
* Aufgrund eines Sicherheitsproblems in PHPMailer wurde diese Komponente auf die Version 5.2.27 aktualisiert.

-----------------------------------------------------------------------------------------

Korrekturen
-----------
Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet.

`<https://bugs.oxid-esales.com/changelog_page.php?version_id=458>`_

-----------------------------------------------------------------------------------------

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop CE können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.2.1...v6.2.2. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

.. Intern: oxbaio, Status: