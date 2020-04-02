OXID eShop 6.1.2
================

Veröffentlichungstermin: 29.01.2019

-----------------------------------------------------------------------------------------

Allgemeines
-----------
OXID eShop 6.1.2 wird als Compilation bereitgestellt. Diese enthält folgende Komponenten:

* OXID eShop CE 6.3.2
* OXID eShop PE 6.2.2
* OXID eShop EE 6.2.1
* Theme "Flow" 3.1.0
* Theme "Wave" 1.0.1
* Amazon Pay 3.2.2
* GDPR Opt-In 2.1.2
* Klarna 4.2.1
* Paymorrow 2.0.1
* PAYONE 1.0.10
* PayPal 5.2.3
* Summernote WYSIWIG-Editor und Mediathek 2.2.0
* Visual CMS 3.3.0 (PE/EE)

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.1.1...v6.1.2>`_.

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

Neue Funktionen
---------------

Neue Komponente der OXID eShop Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Das Theme "Wave" - responsiv und auf Bootstrap 4 basierend - ist jetzt neue Komponente der OXID eShop Compilation. Mehr Informationen zum Theme stellt der englischsprachige Blogbeitrag `Introducing Wave theme <https://oxidforge.org/en/introducing-wave-theme.html>`_ auf der OXIDforge bereit.

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------

Aktualisierte Komponenten der OXID eShop Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Folgende Komponenten wurden auf eine neue Version aktualisiert:

* OXID eShop CE (Update von 6.3.1 auf 6.3.2), `Changelog 6.3.2 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.3.2/CHANGELOG.md>`_
* OXID eShop PE (Update von 6.2.1 auf 6.2.2)
* OXID eShop EE (Update von 6.2.0 auf 6.2.1)
* Theme "Flow" (Update von 3.0.2 auf 3.1.0) `Changelog 3.1.0 <https://github.com/OXID-eSales/flow_theme/blob/v3.1.0/CHANGELOG.md>`_
* AmazonPay (Update von 3.2.1 auf 3.2.2), `Changelog 3.2.2 <https://github.com/bestit/amazon-pay-oxid/blob/3.2.2/CHANGELOG.md>`_
* Klarna (Update von 4.2.0 auf 4.2.1), `Changelog 4.2.1 <https://github.com/topconcepts/OXID-Klarna-6/blob/master/CHANGELOG.md>`_
* Visual CMS (PE/EE, Update von 3.2.2 auf 3.3.0)

-----------------------------------------------------------------------------------------

Korrekturen
-----------

Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet.

https://bugs.oxid-esales.com/changelog_page.php?version_id=470 und |br|
https://bugs.oxid-esales.com/changelog_page.php?version_id=458

-----------------------------------------------------------------------------------------

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop CE können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.3.1...v6.3.2. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

.. Intern: oxbain, Status: