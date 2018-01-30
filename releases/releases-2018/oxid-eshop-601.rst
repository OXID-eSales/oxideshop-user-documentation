OXID eShop 6.0.1
================

Veröffentlichungstermin: 30.01.2018

-----------------------------------------------------------------------------------------

Allgemeines
-----------
Der OXID eShop 6.0.1 wird als Compilation bereitgestellt. Darin sind OXID eShop 6.1.0, die Module AmazonPay 3.0.2, Paymorrow 2.0.0, PayOne 1.0.5, PayPal 5.1.5, VisualCMS 3.1.0 (PE/EE) sowie der WYSIWIG-Editor und die Mediathek Summernote 2.1.0 als Komponenten enthalten. Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.0.0...v6.0.1 <https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.0.0...v6.0.1>`_.

Mit OXID eShop 6.0.1 wird eine Sicherheitslücke geschlossen, die mit CVSS = 4.9 eingestuft wurde und nur in der Enterprise Edition mit Hochlastoption und aktivem Varnish auftritt. Bitte aktualisieren Sie die betroffene Shopsoftware so schnell als möglich. Details zur Sicherheitslücke werden in den kommenden Tagen mit dem OXID Security Bulletin 2018-01 veröffentlicht.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
Der OXID eShop 6.0.0 läuft unter PHP 5.6 oder 7.0. Als Datenbank wird MySQL in der Version 5.5 oder 5.7 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte en Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

Installation
^^^^^^^^^^^^
Für die Installation, folgen Sie bitte den Anleitungen im Abschnitt "Installation":

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Update-Installation <../../installation/update-installation/update-installation>`

Bitte führen Sie das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, aus. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------

Webbasiertes Setup
^^^^^^^^^^^^^^^^^^
Das Setup des OXID eShop, welches im Browser aufgerufen wird, wurde überarbeitet. Es präsentiert sich jetzt im neuen Design. Im zweiten Installationsschritt kann nicht mehr ausgewählt werden, für welche Wirtschaftsregion das Angebot des Shops bestimmt ist (Deutschland, Österreich, Schweiz). Die Auswahl war ohne Funktion, nachdem bereits im OXID eShop 6.0.0 die sogenannten DynPages mit e-Commerce-Inhalten aus dem Menü des Administrationsbereiches entfernt wurden.

Templates und Sprachdateien
^^^^^^^^^^^^^^^^^^^^^^^^^^^
In der Version 6.0.1 wurden Änderungen im Template :file:`article_main.tpl` des Administrationsbereiches vorgenommen. Darüber hinaus gab es keine weiteren Änderungen in Templates für den Administrationsbereich und keine in den Templates für das Frontend sowie in den Sprachdateien.

-----------------------------------------------------------------------------------------

Korrekturen
-----------

Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet: |br|
`https://bugs.oxid-esales.com/changelog_page.php?version_id=392 <https://bugs.oxid-esales.com/changelog_page.php?version_id=392>`_

-----------------------------------------------------------------------------------------

Weiterführende Informationen für Entwickler finden Sie im Changelog der Community Edition: `https://github.com/OXID-eSales/oxideshop_ce/blob/b-6.x/CHANGELOG.md <https://github.com/OXID-eSales/oxideshop_ce/blob/b-6.x/CHANGELOG.md>`_.

Änderungen gegenüber der vorhergehenden Version können im im Repository der Community Edition auf GitHub eingesehen werden: `https://github.com/OXID-eSales/oxideshop_ce/compare/v6.0.0...v6.1.0 <https://github.com/OXID-eSales/oxideshop_ce/compare/v6.0.0...v6.1.0>`_

.. Intern: oxbaib, Status: