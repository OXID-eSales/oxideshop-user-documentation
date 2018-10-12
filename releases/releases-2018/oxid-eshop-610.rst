OXID eShop 6.1.0
================

Veröffentlichungstermin: 31.07.2018

-----------------------------------------------------------------------------------------

Allgemeines
-----------
Der OXID eShop 6.1.0 wird als Compilation bereitgestellt. Diese enthält folgende Komponenten:

* OXID eShop 6.3.0
* Theme "Flow" 3.0.2
* AmazonPay 3.1.4
* GDPR Opt-In 2.1.1
* Klarna 4.0.1
* Paymorrow 2.0.1
* PAYONE 1.0.8
* PayPal 5.2.2
* Visual CMS 3.2.1
* WYSIWIG-Editor und die Mediathek Summernote 2.1.1

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.0.3...v6.1.0>`_.

Mit OXID eShop 6.1.0 wurden zwei Sicherheitslücken geschlossen. Eine der beiden Sicherheitslücken ist nur dann relevant, wenn im Shop die Zahlungsart Paymorrow aktiv genutzt wird. Details zu beiden Sicherheitslücken finden Sie auf folgenden Seiten der OXIDforge: `Security Bulletin 2018-002 <https://oxidforge.org/en/security-bulletin-2018-002.html>`_ und `Security Bulletin 2018-003 <https://oxidforge.org/en/security-bulletin-2018-002.html>`_. Wir empfehlen ein schnelles Update auf diese Shopversion (6.1.0) und auf das ausgelieferte Modul Paymorrow 2.0.1. Eine Anleitung zum Shop-Update finden Sie unter :doc:`Update-Installation <../../installation/update-installation/index>`.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
Der OXID eShop 6.1.0 läuft unter PHP 7.0 und 7.1. Der Support für PHP 5.6 wurde eingestellt. Als Datenbank wird MySQL in der Version 5.5 oder 5.7 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

Installation
^^^^^^^^^^^^
Für die Installation, folgen Sie bitte den Anleitungen im Abschnitt "Installation":

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Update-Installation <../../installation/update-installation/update-installation>`

Bitte führen Sie das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, aus. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

-----------------------------------------------------------------------------------------

Neue Funktionen
---------------

Neue Komponenten der OXID eShop Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Die OXID eShop Compilation wurde durch die Module GDPR Opt-in 2.1.1 und Klarna 4.0.1 erweitert. Das Modul GDPR Opt-in stellt Opt-in-Funktionen bereit, welche der OXID eShop für die Umsetzung der Datenschutz-Grundverordnung (DSGVO) benötigt. Mit dem Modul Klarna wird ein weiteres Zahlungsmodul ausgeliefert, mit dem Shopbetreiber beispielsweise Zahlungen auf Rechnung, per Ratenkauf oder per Sofortüberweisung über den Finanzdienstleister Klarna abwickeln können.

PSR-3 Logger
^^^^^^^^^^^^
Ein Logger nach Spezifikation von PSR-3 wurde in den OXID eShop integriert. Die standardisierte Schnittstelle zum automatischen Erstellen und Abspeichern von Logs ersetzt den bisherigen Logging-Mechanismus des Shops.

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------

Aktualisierte Komponenten der OXID eShop Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Folgende Komponenten wurden auf eine neue Version aktualisiert:

* OXID eShop (Update von 6.2.0 auf 6.3.0), `Changelog 6.3.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.3.0/CHANGELOG.md>`_
* Theme "Flow" (Update von 3.0.0 auf 3.0.2), `Changelog 3.0.2 <https://github.com/OXID-eSales/flow_theme/blob/v3.0.2/CHANGELOG.md>`_
* AmazonPay (Update von 3.0.2 auf 3.1.4)
* Paymorrow (Update von 2.0.0 auf 2.0.1), `Changelog 2.0.1 <https://github.com/OXID-eSales/paymorrow-module/blob/v2.0.1/CHANGELOG.md>`_
* PAYONE (Update von 1.0.5 auf 1.0.8), `Changelog 1.0.8 <https://github.com/PAYONE-GmbH/oxid-6/blob/1.0.8/Changelog.txt>`_
* PayPal (Update von 5.1.6 auf 5.2.2), `Changelog 5.2.2 <https://github.com/OXID-eSales/paypal/blob/v5.2.2/CHANGELOG.md>`_
* Visual CMS (PE/EE, Update von 3.2.0 auf 3.2.1) `Changelog 3.2.1 <https://github.com/OXID-eSales/visual_cms_module/blob/v3.2.1/CHANGELOG.md>`_

Konfigurierbares Kontaktformular
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Im Administrationsbereich kann unter :menuselection:`Grundeinstellungen --> Stammdaten`, Registerkarte :guilabel:`Einstell.` in der Sektion :guilabel:`Weitere Einstellungen` eingestellt werden, welche Eingabefelder des Kontaktformulars Pflichtfelder sein sollen. Nur die aktivierten Felder werden beim Abschicken des Kontaktformulars validiert.

Diese Einstellungen für das Kontaktformular wurden im Zusammenhang mit der Datenschutz-Grundverordnung implementiert, um Shopbetreibern die Möglichkeit zu geben, nur die für die Bearbeitung einer Anfrage notwendigen Daten zu erheben.

Module können Smarty-Plugins überschreiben
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Module sind jetzt in der Lage, Smarty-Plugins zu überschreiben. Dafür wurde die Version 2.1 der Metadata eingeführt.

Nicht mehr unterstützte Features und Funktionen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Das für den OXID eShop 4&5 verwendete Prüfscript, welches die Integrität der .php-Dateien und Templates prüfte, wird nicht mehr unterstützt. Der Aufruf aus dem Administrationsbereich heraus durch Aktivieren des Kontrollkästchens :guilabel:`Versionsprüfung ausführen und abfragen` unter :menuselection:`Service --> Diagnosewerkzeug` wurde entfernt.

-----------------------------------------------------------------------------------------

Korrekturen
-----------
Es wurden die oben genannten Sicherheitslücken geschlossen. Die mit diesem Release behobenen Bugs sind identisch wie die der Version 6.0.3. Da Bugs im Bugtrack-System nicht für alle Versionen als behoben markiert werden können, gilt die Liste für OXID eShop 6.0.3.

https://bugs.oxid-esales.com/changelog_page.php?version_id=433

-----------------------------------------------------------------------------------------

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.2.0...v6.3.0.

.. Intern: oxbaia, Status: