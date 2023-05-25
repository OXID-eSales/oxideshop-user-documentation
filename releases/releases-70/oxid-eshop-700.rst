OXID eShop 7.0.0
================

.. todo: #HR: Datum: verif. 24.05

Veröffentlichungstermin: 30.05.2023

Die wichtigsten Änderungen im Überblick
----------

* OXID eShop 7.0 unterstützt nativ die Template Engine Twig. Die bisher verwendete Template Engine Smarty steht als alternatives Paket zur Verfügung. Wir empfehlen jedoch einen baldigen Umstieg auf den neuen Standard Twig.
* MySQL 8, Composer 2.4 und das Bildformat WebP unterstützt.
* Das Module-Handling wurde optimiert und angepasst.

Technologien
----------

* Unterstützung für MySQL-Version 8.0.

* Unterstützung für Composer-Version 2.4.

* Umstellung der Standard Template Engine von Smarty auf Twig.

  * Weitere Informationen finden Sie unter `Twig Template Engine <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/twig_template_engine/index.html>`_.

  * Smarty kann optional weiterhin verwendet werden. Siehe <Link zu https://github.com/OXID-eSales/developer_documentation/commit/e9bdc830de0de7c828d0e3b293dd5c9edbc5a24b>

* Automatisches HTML-Escaping im Frontend.

  * Weitere Informationen finden Sie in der Entwickler-Dokumentation `Check HTML escaping <https://docs.oxid-esales.com/developer/en/latest/update/eshop_from_65_to_7/modules.html#check-html-escaping>`_.

* Unterstützung des WebP Bildformats.

  * Siehe :ref:`konfiguration/bilder:Bildgenerierung und -qualität`.

* Symfony-Komponenten wurden auf Version 6 aktualisiert.



Verbesserung des Modulsystems
-------

Composer
^^^^^^^^
Entsprechend der Composer Philosophie werden Moduldateien ausschließlich aus dem Verzeichnis :file:`vendor/` gelesen. Beim Installieren von Modulen werden die Dateien nicht mehr automatisch in das Verzeichnis :file:`source/modules/` kopiert.

Weitere Informationen finden Sie in unserer Entwickler-Dokumentation `Module skeleton: metadata, composer and structure <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/skeleton/index.html>`_

YAML-Files
^^^^^^^^
Weiterhin wurde die Struktur der Konfigurationsdateien angepasst. Weitere Informationen finden Sie unter

* `Modules configuration and setup <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/module_configuration/modules_configuration.html>`_
* `Troubleshooting <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/installation_setup/troubleshooting.html>`_

Bei einem Update auf die Version 7 ist es daher notwendig eigene Module in die neue Struktur zu überführen: `Check changes in the module handler <https://docs.oxid-esales.com/developer/en/latest/update/eshop_from_65_to_7/modules.html#port-to-v7-module-handler-20221123>`_.

  .. todo: #tbd: URL verif.


Console
^^^^^^^^

Geänderte Commands für das Handling von Modulen:

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

Sie haben auf der OXID eShop Console folgende Möglichkeiten:

* Erstellen Sie mit ``oe:setup:shop`` die Datenbank und konfigurieren Sie Ihren OXID eShop.
  |br|
  Die dafür notwendigen Informationen übergeben Sie mit Parametern.

* Installieren Sie mit ``oe:setup:demodata`` Demodaten.
* Legen Sie mit ``oe:admin:create-user`` den Shop-Administrator an.
* Wenn Sie die OXID eShop Professional oder Enterprise Edition haben, fügen Sie mit ``oe:license:add`` Lizenzschlüssel hinzu.

  Es ist technisch nicht möglich, vorhandene Lizenzschlüssel durch neue zu ersetzen. Wenn Sie einen bestehenden Lizenzschlüssel durch eine anderen tauschen, löschen Sie deshalb vorher mit ``oe:license:clear`` alle Lizenzschlüssel und fügen die Lizenzschlüssel anschließend erneut hinzu.

Weitere Informationen finden Sie unter :doc:`Setup per Kommandozeile <../../installation/neu-installation/setup-kommandozeile>`

Clean Up
-------------
Entfernung von veralteten (deprecated) Funktionen.

Test-Bibliothek
^^^^^^^^^^^^^^^

Nutzen Sie statt der Test-Bibliothek die native PHPUnit- und Codeception-Funktionalität.

Weitere Informationen finden Sie in der Entwickler-Dokumentation unter `Testing <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/testing/codeception/index.html>`_.

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

Die Liste Ihrer Newsletter-Abonnenten können Sie im Administrationsbereich exportieren, um die Daten in einem professionellen Marketing-Tool zu verwenden.

Weitere Informationen finden Sie unter :doc:`Newsletter <../../betrieb/newsletter/newsletter>`.

Nachrichten (News) wurde entfernt
^^^^^^^^^^^^^^^^^^^^

Mit der Einführung des Themes Flow (OXID eShop 6.0.0), konnten Sie Nachrichten unter :menuselection:`Admin --> Kundeninformationen --> Nachrichten` bereits nur noch über einen Link im Fußbereich aufrufen.

Stattdessen empfehlen wir, zukünftig Landing Pages mit Visual CMS (für die Professional und Enterprise Edition) zu realisieren, um Neuigkeiten oder Angebote zu präsentieren.

Verschlüsselte Werte in der Datenbank
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die native Verschlüsselung der Shop-Konfiguration in der Tabelle :code:`oxconfig` haben wir entfernt, da MySQL 8.0 diese Funktion nicht mehr unterstützt.

Komponenten
-----------

Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält folgende Komponenten:

.. todo: Metapackes: https://github.com/OXID-eSales/oxideshop_metapackage_ce/blob/b-7.0/composer.json, dito: PE, EE
.. todo: #done: Flow und Wave weg, dafür Twig
.. todo: #Support: Sind Twig admin-theme und Twig component durch Twig theme abgedeckt?
.. todo: #done: Payone, Klarna, Unzer, PayPal entfallen

* `OXID eShop CE 7.0.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.0/CHANGELOG.md>`_
* `OXID eShop PE 7.0.0 <https://github.com/OXID-eSales/oxideshop_pe/blob/v7.0.0/CHANGELOG.md>`_
* `OXID eShop EE 7.0.0 <https://github.com/OXID-eSales/oxideshop_ee/blob/v7.0.0/CHANGELOG.md>`_
* `Apex theme 1.0.0 <https://github.com/OXID-eSales/apex-theme/blob/v1.0.0/CHANGELOG.md>`_
* `Twig theme 2.1.0 <https://github.com/OXID-eSales/twig-theme/blob/v2.1.0/CHANGELOG.md>`_
* `Twig admin theme 2.1.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.1.0/CHANGELOG.md>`_
* `Twig component 2.1.0 <https://github.com/OXID-eSales/twig-component/blob/v2.1.0/CHANGELOG.md>`_

* `OXID eShop composer plugin 7.1.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.1.0/CHANGELOG.md>`_
* `OXID eShop Views Generator 2.1.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.1.0/CHANGELOG.md>`_
* `OXID eShop DemoData installer 3.1.0 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.1.0/CHANGELOG.md>`_
* `OXID eShop demodata CE/PE/EE 8.0.0 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.0/CHANGELOG.md>`_
* `OXID eShop doctrine migration integration 5.1.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.1.0/CHANGELOG.md>`_
* `OXID eShop facts 4.1.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.1.0/CHANGELOG.md>`_
* `Unified Namespace Generator 4.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v4.1.0/CHANGELOG.md>`_

* `GDPR Opt-In 3.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 2.0.2 <https://github.com/OXID-eSales/usercentrics/blob/v2.0.2/CHANGELOG.md>`_
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


.. Intern: oxbajt, Status: