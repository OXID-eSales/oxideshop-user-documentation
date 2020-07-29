OXID eShop 6.0.2
================

Veröffentlichungstermin: 28.03.2018

-----------------------------------------------------------------------------------------

Allgemeines
-----------
OXID eShop 6.0.2 wird als Compilation bereitgestellt. Darin sind die Komponenten OXID eShop 6.2.0, das Theme "Flow" 3.0.0, die Module AmazonPay 3.0.2, Paymorrow 2.0.0, PayOne 1.0.5, PayPal 5.1.6, Visual CMS 3.2.0 (PE/EE) sowie der WYSIWIG Editor + Mediathek 2.1.1 enthalten. Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.0.1…v6.0.2>`_.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
OXID eShop 6.0.1 läuft unter PHP 5.6 oder 7.0. Als Datenbank wird MySQL in der Version 5.5 oder 5.7 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

Installation
^^^^^^^^^^^^
Für die Installation, folgen Sie bitte den Anleitungen im Abschnitt "Installation":

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Update-Installation <../../installation/update-installation/update-installation>`

Bitte führen Sie das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, aus. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

-----------------------------------------------------------------------------------------

Neue Funktionen
---------------

Umgang mit Kundendaten
^^^^^^^^^^^^^^^^^^^^^^
Es wurden neue Möglichkeiten geschaffen, wie Kunden des Shops mit ihren Daten umgehen können.

* Kunde erhält die Möglichkeit, sein eigenes Konto im Shop zu löschen
* Kunde kann gespeicherte Lieferadressen löschen
* Kunde kann einzelne Artikelbewertungen und Sterne-Ratings löschen
* Kunde kann Artikelempfehlungen per Formular/E-Mail an Interessenten verschicken

Einige Funktionen können im Administrationsbereich des Shops unter :menuselection:`Stammdaten --> Grundeinstellungen --> Registerkarte Einstell.` aktiviert oder abgeschaltet werden. Gehen Sie dafür zum Abschnitt :guilabel:`Artikel` bzw. :guilabel:`Kontoeinstellungen`.

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------

Templates und Sprachdateien
^^^^^^^^^^^^^^^^^^^^^^^^^^^
In der Version 6.0.2 wurden Templates des Administrationsbereiches, des Frontends, einige Sprachdateien sowie .js-Dateien und .css-Dateien geändert. Alle geänderten Dateien können in den Repositories auf GitHub eingesehen werden.

Shop: `<https://github.com/OXID-eSales/oxideshop_ce/compare/v6.1.0...v6.2.0>`_ |br|
Theme "Flow":`<https://github.com/OXID-eSales/flow_theme/compare/v2.3.3...v3.0.0>`_

Wechseln Sie jeweils zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

-----------------------------------------------------------------------------------------

Korrekturen
-----------

Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet.

Shop: `<https://bugs.oxid-esales.com/changelog_page.php?version_id=419>`_ |br|
Theme "Flow": `<https://bugs.oxid-esales.com/changelog_page.php?version_id=404>`_

-----------------------------------------------------------------------------------------

Weiterführende Informationen für Entwickler finden Sie im Changelog der Community Edition: `<https://github.com/OXID-eSales/oxideshop_ce/blob/b-6.x/CHANGELOG.md>`_.

Änderungen gegenüber den vorhergehenden Versionen finden Sie in den öffentlichen Repositories auf GitHub: |br|
`OXID eShop 6.2.0 <https://github.com/OXID-eSales/oxideshop_ce/compare/v6.1.0...v6.2.0>`_ |br|
`Theme Flow 3.0.0 <https://github.com/OXID-eSales/flow_theme/compare/v2.3.3...v3.0.0>`_ |br|
`Modul PayPal 5.1.6 <https://github.com/OXID-eSales/paypal/blob/v5.1.6/CHANGELOG.md>`_ |br|

.. Intern: oxbaij, Status: