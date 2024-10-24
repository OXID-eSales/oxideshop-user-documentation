OXID eShop 7.0.0
================

Veröffentlichungstermin: 30.05.2023

Die wichtigsten Änderungen im Überblick
---------------------------------------

* OXID eShop 7.0 unterstützt nativ die Template Engine Twig.

  .. important::
     Um Ihnen den Umstieg zu erleichtern, stellen wir die bisher verwendete Template-Engine Smarty für :productname:`OXID eShop` 7.0 noch als alternatives Paket zur Verfügung.

     Bereits :productname:`OXID eShop` 7.1 wird jedoch die Smarty-Engine nicht mehr unterstützen.

     Steigen Sie deshalb so bald wie möglich auf den neuen Standard Twig um.

* MySQL 8, Composer 2.7 und das Bildformat WebP werden unterstützt.
* Das Module-Handling wurde optimiert und angepasst.

Technologien
------------

* Unterstützung für MySQL-Version 8.0

* Unterstützung für Composer-Version 2.7

* Umstellung der Standard Template Engine von Smarty auf Twig

  Weitere Informationen finden Sie unter `Twig Template Engine <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/twig_template_engine/index.html>`_.

  Optional können Sie weiterhin Smarty verwenden.
  |br|
  Weitere Informationen finden Sie unter `Switching to the legacy Smarty template engine <https://docs.oxid-esales.com/developer/en/latest/update/eshop_from_65_to_7/install_smarty_engine.html>`_.

* Automatisches HTML-Escaping im Frontend

  Weitere Informationen finden Sie in der Entwickler-Dokumentation unter `Check HTML escaping <https://docs.oxid-esales.com/developer/en/latest/update/eshop_from_65_to_7/modules.html#check-html-escaping>`_.

* Unterstützung des Bildformats WebP

  Weitere Informationen finden Sie unter :ref:`konfiguration/bilder:Bildgenerierung und -qualität`.

* Aktualisierung der Symfony-Komponenten auf Version 6

Verbesserung des Modulsystems
-----------------------------

Composer
^^^^^^^^

Entsprechend der Philosophie von Composer werden Moduldateien ausschließlich aus dem Verzeichnis :file:`vendor/` gelesen.

Beim Installieren von Modulen werden die Dateien nicht mehr in das Verzeichnis :file:`source/modules/` kopiert.

Weitere Informationen finden Sie in unserer Entwickler-Dokumentation unter `Module skeleton: metadata, composer and structure <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/skeleton/index.html>`_

YAML-Files
^^^^^^^^^^

Wir haben die Struktur der Konfigurationsdateien angepasst.

Weitere Informationen finden Sie unter

* `Modules configuration and setup <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/module_configuration/modules_configuration.html>`_
* `Troubleshooting <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/installation_setup/troubleshooting.html>`_

Bei einem Update auf die Version 7 ist es daher notwendig, dass Sie eigene Module in die neue Struktur überführen.

Weitere Informationen finden Sie unter `Check changes in the module handler <https://docs.oxid-esales.com/developer/en/latest/update/eshop_from_65_to_7/modules.html#port-to-v7-module-handler-20221123>`_.

Console
^^^^^^^

Die Befehle für das Handling von Modulen sind geändert.

Weitere Informationen finden Sie unter

* `Best practice module setup for development with composer <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/tutorials/module_setup.html>`_
* `Uninstall modules <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/uninstall/index.html>`_


Neue Funktionen
---------------

Tracking-URL je Versandart
^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #tbd: Doku im entspr. Kap. erg: :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Weitere Einstellungen`
        :menuselection:`Master Settings --> Core Settings --> Settings --> Other Settings`, :guilabel:`Standard shipping provider tracking URL`

Hinterlegen Sie pro Versandart eine Tracking-URL.

Sobald die Paket-ID (je nach Versanddienstleister Tracking Code, Paketscheinnummer, Paketreferenz, Sendungsnummer usw.) bei der Bestellung eingetragen wurde, steht der Tracking-Link, bestehend aus der Tracking-URL und der Paket-ID der Bestellung, zur Verfügung.

Weitere Informationen finden Sie unter :ref:`Tracking-URL <tracking-url-shipping-method>`.

Setup per Kommandozeile
^^^^^^^^^^^^^^^^^^^^^^^

Um das Implementieren Ihres Projekts zu vereinfachen, können Sie, alternativ zum webbasierten Setup, Ihren OXID eShop über die Kommandozeile erstellen und konfigurieren.

Sie haben auf der OXID eShop-Console folgende Möglichkeiten:

* Erstellen Sie mit ``oe:setup:shop`` die Datenbank und konfigurieren Sie Ihren OXID eShop.
  |br|
  Die dafür notwendigen Informationen übergeben Sie mit Parametern.

* Installieren Sie mit ``oe:setup:demodata`` Demodaten.
* Legen Sie mit ``oe:admin:create-user`` den Shop-Administrator an.
* Wenn Sie die OXID eShop Professional oder Enterprise Edition haben, fügen Sie mit ``oe:license:add`` Lizenzschlüssel hinzu.

  Es ist technisch nicht möglich, vorhandene Lizenzschlüssel durch neue zu ersetzen. Wenn Sie einen bestehenden Lizenzschlüssel durch eine anderen tauschen, löschen Sie deshalb vorher mit ``oe:license:clear`` alle Lizenzschlüssel und fügen die Lizenzschlüssel anschließend erneut hinzu.

Weitere Informationen finden Sie unter :doc:`Setup per Kommandozeile <../../installation/neu-installation/setup-kommandozeile>`.

Clean Up
--------

Folgende veraltete (deprecated) Funktionen haben wir entfernt.

Test-Bibliothek
^^^^^^^^^^^^^^^

Nutzen Sie statt der Test-Bibliothek die native PHPUnit- und Codeception-Funktionalität.

Weitere Informationen finden Sie in der Entwickler-Dokumentation unter `Testing <https://docs.oxid-esales.com/developer/en/latest/development/testing/index.html>`_.

RSS-Funktionalität
^^^^^^^^^^^^^^^^^^

Die RSS-Funktionalität ist entfallen.

Anmeldung über LDAP
^^^^^^^^^^^^^^^^^^^

Wenn Sie eine LDAP-Umgebung haben, müssen Sie eine eigene Login-Lösung implementieren.

Kreditkarte als Zahlungsart
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die im OXID eShop implementierte Zahlungsart Kreditkarte unterstützen wir aus Sicherheitsgründen nicht mehr.

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


Korrekturen
-----------

* https://bugs.oxid-esales.com/changelog_page.php?version_id=344
* https://bugs.oxid-esales.com/changelog_page.php?version_id=630
* https://bugs.oxid-esales.com/changelog_page.php?version_id=728

Installation
------------

Folgen Sie zum Installieren den Anleitungen unter :ref:`installation/index:Installation`.

Dank
----

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