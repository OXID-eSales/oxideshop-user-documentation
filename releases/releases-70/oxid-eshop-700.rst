OXID eShop 7.0.0
================

.. todo: #HR: Datum: Tech release gepl. 31.4.; Taggen vermutl. 9.5.

Veröffentlichungstermin: 31.04.2023


Funktionen
----------

Sicherheit
^^^^^^^^^^

* Unterstützte MySQL-Version: 8.0

  Verbessern Sie mit MySQL 8.0 vor allem die Sicherheit, aber auch die Performance:

  * schnelleres Suchen und Indizieren
  * bessere Skalierbarkeit
  * verbesserte Unterstützung von NoSQL-Operationen
  * verbesserte Unterstützung räumlicher Daten
  * verbesserte Unterstützung von Transaktionen und damit einfachere Entwicklung und Wartung

  .. note::
     **MySQL 5.7**

     MySQL 5.7 zu nutzen, ist möglich, aber wir empfehlen MySQL 8.0.


* Unterstützte PHP-Versionen: 8.0 und 8.1

* Unterstützte Composer-Version: 2.4

  Mit Composer 2.4 haben Sie außerdem bessere Unterstützung für Plugins, und es erleichtert Ihnen die Diagnose und den Umgang mit Fehlermeldungen.

* Symfony-Komponenten sind aktualisiert auf Symfony Version 6.

* Automatisches HTML-Escaping im Frontend

  Das Interpretieren bestimmter HTML-Tags passiert nicht mehr zentral in der Klasse :code:`Field`, sondern im Frontend automatisch durch die Twig Template Engine oder GraphQL.

  Twig und GraphQL umgehen diese Zeichen automatisch und geben sie sicher wieder. Dadurch ist sichergestellt, dass kein schädlicher JavaScript-Code ausgeführt werden kann. Cross-Site Scripting (XSS)-Angriffe werden unterbunden.

  .. important::

     Wenn Sie Smarty nutzen oder eigene Lösungen bauen, stellen Sie sicher, dass Sie das HTML-Escaping eingeschaltet haben.

     .. todo: #tbd: verify URL: (https://docs.oxid-esales.com/developer/en/7.0-rc.2/update/eshop_from_65_to_7/modules.html#check-html-escaping)

     Weitere Informationen finden Sie in der Entwickler-Dokumentation unter `Check HTML escaping <https://docs.oxid-esales.com/developer/en/latest/update/eshop_from_65_to_7/modules.html#check-html-escaping>`_.

* Metadata Version 2.0 oder höher

  Weitere Informationen über Metadaten finden Sie in der Entwickler-Dokumentation unter `metadata.php <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/skeleton/metadataphp/index.html>`_.


Performance
^^^^^^^^^^^

* Um die Browser-Geschwindigkeit zu erhöhen, unterstützen wir das Bildformat WebP.

  Optional: Sie können Ihre in anderen Formaten vorliegenden Bilder automatisch konvertieren.

  Aktivieren Sie dazu unter :menuselection:`Stammdaten --> Grundeinstellungen --> System --> Bilder` das Kontrollkästchen :guilabel:`Bilder automatisch ins WebP-Format konvertieren`.

  Siehe :ref:`konfiguration/bilder:Bildgenerierung und -qualität`.

  .. todo: EN: :menuselection:`Master Settings --> Core Settings --> System --> Pictures` -- checkbox :guilabel:`Automatically convert images to WebP format`

Entwicklung
^^^^^^^^^^^

* Nutzen Sie Twig, unsere Standard-Template Engine. Twig ist weit verbreitet, wird gut gewartet und hat eine große Entwickler-Community, in der Sie Unterstützung finden.

  Weitere Informationen finden Sie unter `Twig Template Engine <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/twig_template_engine/index.html>`_.

* Nicht nativ in Twig, aber wichtig, wenn Sie eigene Module entwickeln: Mit der Twig-Templates-Mehrfachvererbung für Module können Sie das visuelle Erscheinungsbild Ihres OXID eShops schnell ändern, ohne interne Geschäftslogik und Codebasis zu beeinträchtigen. Ändert sich ein Modul, passt sich das Layout automatisch an.

  Weitere Informationen finden Sie unter `Understanding the OXID eShop template hierarchy and override system <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/theme/theme_template_hierarchy.html>`_.


* Die Namen in den Controller-Templates sind unabhängig von der Template Engine.

  Dies erleichtert Ihnen das Einbinden alternativer Template Engines, beispielsweise Smarty.

  Denn die Template Engine findet die richtige Extension automatisch.

  Beispiel: Controller::$_sThisTemplate='page/content' statt 'page/content.tpl'

Betrieb
^^^^^^^

* Um Ihnen das Installieren, Konfigurieren und Warten Ihres OXID eShop zu erleichtern, haben wir den Aufbau der OXID eShop-Konfigurationsdatei geändert.

  Weitere Informationen finden Sie unter

  * `Modules configuration and setup <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/module_configuration/modules_configuration.html>`_
  * `Troubleshooting <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/installation_setup/troubleshooting.html>`_

* Um Ihnen auch das Installieren, Konfigurieren und Betreiben von Modulen zu erleichtern, haben wir den Module-Handler so geändert, dass alle Modul-spezifischen Informationen nicht mehr in der Datenbank, sondern in YAML-Dateien gespeichert sind.

  Weitere Informationen finden Sie unter `Check changes in the module handler <https://docs.oxid-esales.com/developer/en/latest/update/eshop_from_65_to_7/modules.html#port-to-v7-module-handler-20221123>`_.

  .. todo: #tbd: URL verif.


Änderungen bei Modulen
----------------------

Native Composer-Unterstützung für Module
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Dateien bleiben im Verzeichnis :file:`/vendor`. Sie werden nicht nach :file:`/source/modules` kopiert.

Dies erleichtert Ihnen das Entwickeln und Warten eigener Module und Projekte.

Siehe auch in der Entwickler-Dokumentation `Module skeleton: metadata, composer and structure <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/skeleton/index.html>`_


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

Modul-Installation per Kommandozeile
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Installieren oder deinstallieren Sie Module mit den neuen Kommandos der OXID eShop Console ``oe:module:install`` und ``oe:module:uninstall``.

Weitere Informationen finden Sie in der englischsprachigen Entwicklerdokumentation unter

.. todo: #tbd: URLs verifiz.
    * https://docs.oxid-esales.com/developer/en/7.0-rc.1/development/modules_components_themes/module/tutorials/module_setup.html
    * https://docs.oxid-esales.com/developer/en/7.0-rc.1/development/modules_components_themes/module/uninstall/index.html.

* https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/tutorials/module_setup.html
* https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/uninstall/index.html.

Verschlankung
-------------

Folgende technisch veralteten Funktionalitäten haben wir entfernt:

Test-Bibliothek
^^^^^^^^^^^^^^^

Nutzen Sie statt der Test-Bibliothek die native PHPUnit- und Codeception-Funktionalität.

Weitere Informationen finden Sie in der Entwickler-Dokumentation unter `Testing <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/testing/codeception/index.html>`_.

RSS-Funktionalität
^^^^^^^^^^^^^^^^^^

Die RSS-Funktionalität ist entfallen.

Anmeldung über LDAP
^^^^^^^^^^^^^^^^^^^

Wir empfehlen, wie die meisten Kunden eine eigene Login-Lösung zu implementieren.

.. todo: #HR: klärt:
    	Ich verstehe den Satz nicht. Wer empfiehlt was? Gibt es dafür eine Anleitung? Ein Modul? Was haben die anderen Kunden implementiert?
    	Funktioniert das alte Script trotzdem noch, wenn man es mit umzieht? Wir haben da draußen noch Enterprise Kunden, die LDAP verwenden.


Kreditkarte als Zahlungsart
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die im OXID eShop implementierte Zahlungsart Kreditkarte unterstützen wir aus Sicherheitsgründen nicht mehr.

Nutzen Sie das Modul eines Zahlungsanbieters, um Ihren Kunden das Zahlen mit der Kreditkarte anzubieten.

Newsletter-Versand
^^^^^^^^^^^^^^^^^^

Die rudimentäre Basis-Newsletter-Funktion zum Versenden eines Newsletters haben wir aus dem OXID eShop entfernt.

Kunden können Newsletter nach wie vor abonnieren.

Die Liste Ihrer Newsletter-Abonnenten exportieren Sie, um die Daten in einem professionellen Marketing-Tool zu verwenden.

Weitere Informationen finden Sie unter :doc:`Newsletter <../../betrieb/newsletter/newsletter>`.

Nachrichten entfernt
^^^^^^^^^^^^^^^^^^^^

Mit der Einführung des Themes Flow (OXID eShop 6.0.0), konnten Sie Nachrichten unter :menuselection:`Admin --> Kundeninformationen --> Nachrichten` bereits nur noch über einen Link im Fußbereich aufrufen.

Stattdessen empfehlen wir, zukünftig Landing Pages mit Visual CMS (für die Professional und Enterprise Edition) zu realisieren, um Neuigkeiten oder Angebote zu präsentieren.

Verschlüsselte Werte in der Datenbank
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die native Verschlüsselung der Shop-Konfiguration in der Tabelle :code:`oxconfig` haben wir entfernt, da MySQL 8.0 diese Funktion nicht mehr unterstützt.

Modul-Informationen sind in eigenen YAML-Dateien gespeichert und können, je nach Anforderung, individuell per Modul eigens verschlüsselt werden.

Komponenten
-----------

Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält folgende Komponenten:

.. attention::

   Folgendes Infos sind Platzhalter. Wir müssen die Infos noch sammeln.

.. todo: #HR: wo finde ich die Komponenten? Metapackage 7.0 wann fertig? -- VL: tbd: bis Do
.. todo: #tbd: Flow und Wave weg, dafür Twig


* OXID eShop CE 7.0.0-rc1: `Changelog 7.0.0-rc1 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.0-rc1/CHANGELOG.md>`_
* OXID eShop PE 7.0.0-rc1
* OXID eShop EE 7.0.0-rc1
* Theme "Flow" 4.0.0: `Changelog Flow 4.0.0 <https://github.com/OXID-eSales/flow_theme/blob/v4.0.0/CHANGELOG.md>`_
* Theme "Wave" 2.0.0: `Changelog 2.0.0 <https://github.com/OXID-eSales/wave-theme/blob/v2.0.0/CHANGELOG.md>`_
* OXID eShop composer plugin 6.0.0: `Changelog 6.0.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v6.0.0/CHANGELOG.md>`_
* OXID eShop Views Generator 2.0.0
* OXID eShop DemoData installer 2.0.0
* OXID eShop demodata CE/PE/EE 7.0.0
* OXID eShop doctrine migration integration 4.0.0: `Changelog 4.0.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v4.0.0/CHANGELOG.md>`_
* OXID eShop facts 3.0.0: `Changelog OXID eShop facts 3.0.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v3.0.0/CHANGELOG.md>`_
* Unified Namespace Generator 3.0.0: `Changelog 3.0.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v3.0.0/CHANGELOG.md>`_

.. todo: #HR: Folgende Komponenten ergänzen: Payone, Klarna, Unzer, PayPal entfällt

* GDPR Opt-In 2.3.3: `Changelog 2.3.3 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* Klarna 5.5.3: `Changelog 5.5.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.3/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics 1.2.1: `Changelog 1.2.1 <https://github.com/OXID-eSales/usercentrics/blob/v1.2.1/CHANGELOG.md>`_
* PAYONE 1.7.0: `Changelog 1.7.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.7.0/Changelog.txt>`_
* PayPal 6.5.0: `Changelog 6.5.0 <https://github.com/OXID-eSales/paypal/blob/v6.5.0/CHANGELOG.md>`_
* WYSIWYG Editor + Mediathek 2.4.1: `Changelog 2.4.1 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v2.4.1/CHANGELOG.md>`_
* Makaira 1.4.2: `Changelog 1.4.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/1.4.2/CHANGELOG.md>`_
* Unzer Payment für OXID 1.0.0 (EE): `Changelog 1.0.0 <https://github.com/OXID-eSales/unzer-module/blob/v1.0.0/CHANGELOG.md>`_


Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^

Die Systemvoraussetzungen finden Sie unter :ref:`installation/neu-installation/server-und-systemvoraussetzungen:Server- und Systemvoraussetzungen`.

Installation
^^^^^^^^^^^^

Folgen Sie zum Installieren den den Anleitungen unter :ref:`installation/index:Installation`.

.. todo: :doc:`Neu-Installation <../../installation/neu-installation/neu-installation>`.


Korrekturen
-----------

* https://bugs.oxid-esales.com/changelog_page.php?version_id=344
* https://bugs.oxid-esales.com/changelog_page.php?version_id=630
* https://bugs.oxid-esales.com/changelog_page.php?version_id=728


.. Intern: oxbajt, Status: