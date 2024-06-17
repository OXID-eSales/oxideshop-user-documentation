
Nutzen Sie das Modul eines Zahlungsanbieters, um Ihren Kunden das Zahlen mit der Kreditkarte anzubieten.

Newsletter-Versand
^^^^^^^^^^^^^^^^^^

Die rudimentäre Basis-Newsletter-Funktion zum Versenden eines Newsletters haben wir aus dem OXID eShop entfernt.

Kunden können Newsletter nach wie vor abonnieren.

Um die Daten in einem professionellen Marketing-Tool zu verwenden, exportieren Sie die Liste Ihrer Newsletter-Abonnenten im Administrationsbereich.

Weitere Informationen finden Sie unter :doc:`Newsletter <../../betrieb/newsletter/newsletter>`.

Nachrichten (News)
^^^^^^^^^^^^^^^^^^

Mit der Einführung des Themes Flow (OXID eShop 6.0.0), konnten Sie Nachrichten unter :menuselection:`Admin --> Kundeninformationen --> Nachrichten` bereits nur noch über einen Link im Fußbereich aufrufen.

Um Neuigkeiten oder Angebote zu präsentieren, empfehlen wir, zukünftig Landing Pages mit Visual CMS (für die Professional und Enterprise Edition) zu realisieren.

Verschlüsselte Werte in der Datenbank
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die native Verschlüsselung der Shop-Konfiguration in der Tabelle :code:`oxconfig` haben wir entfernt, weil MySQL 8.0 diese Funktion nicht mehr unterstützt.

Komponenten
-----------

Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält folgende Komponenten:

* `OXID eShop CE 7.0.1 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.1/CHANGELOG.md>`_
* `OXID eShop PE 7.0.0 <https://github.com/OXID-eSales/oxideshop_pe/blob/v7.0.0/CHANGELOG.md>`_
* `OXID eShop EE 7.0.0 <https://github.com/OXID-eSales/oxideshop_ee/blob/v7.0.0/CHANGELOG.md>`_
* `Apex theme 1.0.0 <https://github.com/OXID-eSales/apex-theme/blob/v1.0.0/CHANGELOG.md>`_
* `Twig admin theme 2.1.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.1.0/CHANGELOG.md>`_
* `Twig component CE 2.1.0 <https://github.com/OXID-eSales/twig-component/blob/v2.1.0/CHANGELOG.md>`_
* `Twig component PE 2.1.0 <https://github.com/OXID-eSales/twig-component-pe/blob/v2.1.0/CHANGELOG.md>`_
* `Twig component EE 2.1.0 <https://github.com/OXID-eSales/twig-component-ee/blob/v2.1.0/CHANGELOG.md>`_

* `OXID eShop composer plugin 7.1.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.1.0/CHANGELOG.md>`_
* `OXID eShop Views Generator 2.1.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.1.0/CHANGELOG.md>`_
* `OXID eShop demo data installer 3.1.0 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.1.0/CHANGELOG.md>`_
* `OXID eShop demo data CE/PE/EE 8.0.0 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.0/CHANGELOG.md>`_
* `OXID eShop doctrine migration integration 5.1.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.1.0/CHANGELOG.md>`_
* `OXID eShop facts 4.1.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.1.0/CHANGELOG.md>`_
* `Unified Namespace Generator 4.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v4.1.0/CHANGELOG.md>`_

* `GDPR Opt-In 3.0.1 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v3.0.1/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 2.0.2 <https://github.com/OXID-eSales/usercentrics/blob/v2.0.2/CHANGELOG.md>`_
* `Visual CMS 4.0.1 <https://github.com/OXID-eSales/visual_cms_module/blob/v4.0.1/CHANGELOG.md>`_ (PE/EE)
* `WYSIWYG Editor + Mediathek 3.0.1 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v3.0.1/CHANGELOG.md>`_
* `Makaira 2.1.0 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.0/CHANGELOG.md>`_


Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^

Die Systemvoraussetzungen finden Sie unter :ref:`installation/neu-installation/server-und-systemvoraussetzungen:Server- und Systemvoraussetzungen`.

Installation
^^^^^^^^^^^^

Folgen Sie zum Installieren den Anleitungen unter :ref:`installation/index:Installation`.

Korrekturen
-----------

* https://bugs.oxid-esales.com/changelog_page.php?version_id=344
* https://bugs.oxid-esales.com/changelog_page.php?version_id=630
* https://bugs.oxid-esales.com/changelog_page.php?version_id=728


Dank
^^^^

Vielen Dank für die Merge Requests, die mit dieser Version veröffentlicht wurden!

.. todo: #tbd: #VL: Haben wir eine Liste zu Beiträger? -- siehe Changelog: dort keine Namen -- VL prüft: i.a.
        flow-control |br|
        PR-758 Refaktorierung von Aufrufen der veralteten getStr-Methode |br|
        PR-721 Fehlende veraltete getConfig- und getSession-Methodenaufrufe behoben |br|
        PR-728 PHP-Fehlerberichtsstufe nicht zurücksetzen |br|
        vanilla-thunder |br|
        PR-764 Anzeige von mehr Details in der Berechtigungsprüfung im Setup-Prozess
        BernhardScheffold |br|
        PR-466 oxseo::OXOBJECTID-Index verbessern
        alfredbez |br|
        PR-772 BC-Klassen durch namenstragende Klassen ersetzt |br|
        PR-493 Zeitstempel wird nun für css und js Dateien hinzugefügt, die von Modulen eingebunden werden |br|
        PR-733 Protokollierung im Shop-Konstruktor, wenn der Shop nicht gültig ist |br|
        PR-766 Einführung von Psalm für statische Code-Analyse |br|
        PR-449 Unterstützung für eine einzige Language-Map-Datei |br|
        PR-744 Argumente zur oxNew-Methodensignatur hinzugefügt, um die Möglichkeiten der statischen Analyse zu verbessern |br|
        PR-802 Exception in der getLanguageAbbr Methode, wenn keine Abkürzung für eine bestimmte ID verfügbar ist |br|
        8i11y |br|
        PR-789 Sicherstellen, dass das Verzeichnis source/out/pictures/generated existiert
        ivoba |br|
        PR-808 und PR-827 Verbessert gitignore
        dx-bhesse |br|
        PR-793 Behebung des Problems mit der Escape-Funktion für Sonderzeichen in simplexml::addChild
        keywan-ghadami-oxid |br|
        PR-754 Preflight-Prüfung für die Erzeugung von Views |br|
        PR-794 Autovervollständigung für SMTP-Felder im Admin-Template abschalten
        AlfonsMartin |br|
        PR-771 Leistungsverbesserung der Klasse Field
        kermie |br|
        PR-826 Beispiel-Dist-Dateien für Übersetzungen im Ordner Application/translations |br|
        PR-729 Mehrzeilen in Übersetzungsdateien entfernt, um sie für Lokalisierungsplattformen geeignet zu machen |br|
        PR-852 Korrektur des Url-Protokolls für die neue Versionsprüfung
        SvenBrunk |br|
        PR-730 Blocknamen in source/Application/views/admin/tpl/shop_main.tpl ändern
        tterhaarlaudert |br|
        PR-750 Überspringen der Währungsurl-Generierung, wenn die Option "Währungen anzeigen" deaktiviert ist
        JaroslavHerber |br|
        PR-787 Verbessertes Laden der Konfigurationsoptionen
        szdirk |br|
        PR-853 Aktualisierte aRobots in source/config.inc.php.dist
        olivereanderson |br|
        PR-813 Copyright-String korrigiert |br|
        |br|
        Behebung von Code-Stil und Typ-Problemen von alfredbez, flow-control, mprokopov, ivoba, SvenBrunk, SimonNitzsche

.. Intern: oxbajt, Status: