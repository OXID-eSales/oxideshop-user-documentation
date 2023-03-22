OXID eShop 7.0.0
================

.. todo: #VL: Datum: Tech release nä. Wo.; Taggen vermutl. 18.4.

Veröffentlichungstermin: 18.04.2023

.. todo: #VL: Was ist das Wichtige an V. 7? -- Folgendes prüfen
    * done: Präsi
    * done: https://oxidesalesag-my.sharepoint.com/:w:/g/personal/christoph_albrecht_oxid-esales_com/EfnSd3ekQv5LpEf4oywZxEIBh4ti8oT5iRoq6WXw4ef6KA?e=QVP9As

Funktionen
----------

Sicherheit
^^^^^^^^^^

* Unterstützte und getestete MySQL-Version: 8.0

  Verbessern Sie mit MySQL 8.0 vor allem die Sicherheit, aber auch die Performance:

  * schnelleres Suchen und Indizieren
  * bessere Skalierbarkeit
  * verbesserte Unterstützung von NoSQL-Operationen
  * verbesserte Unterstützung räumlicher Daten
  * verbesserte Unterstützung von Transaktionen und damit einfachere Entwicklung und Wartung


* Unterstützte und getestete PHP-Versionen: 8.0 und 8.1

* Unterstützte und getestete Composer-Version: 2.4

  Composer 2.4 unterstützt PHP 8. Composer Version 1.x unterstützen wir aus Sicherheitsgründen nicht mehr.

  Mit Composer 2.4 haben Sie außerdem bessere Unterstützung für Plugins, und es erleichtert Ihnen die Diagnose und den Umgang mit Fehlermeldungen.


* Symfony-Komponenten sind aktualisiert auf Symfony Version 6.

  Hintergrund: Es gibt keine (Sicherheits-) Updates für Symfony 3.4, und es ist nicht mit PHP 8.1 kompatibel.

  Mit dem Update ist Ihr Zugang zu den neuesten Fehlerbehebungen, Sicherheits-Patches und anderen Support-Ressourcen sichergestellt.

 * Automatisches HTML-Escaping im Frontend

  Das Interpretieren bestimmter HTML-Tags passiert nicht mehr zentral in der Klasse :code:`CoreField`, sondern im Frontend automatisch durch die Twig Templating Engine oder GraphQL.

  Twig und GraphQL umgehen diese Zeichen automatisch und geben sie sicher wider. Dadurch ist sichergestellt, dass kein schädlicher JavaScript-Code ausgeführt werden kann. Cross-Site Scripting (XSS)-Angriffe werden unterbunden.

  .. important::

     Wichtig

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

* Nutzen Sie Twig, unsere Standard-Templating Engine. Twig ist weit verbreitet, wird gut gewartet und hat eine große Entwickler-Community, in der Sie Unterstützung finden.

  Weitere Informationen finden Sie unter `Twig Template Engine <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/twig_template_engine/index.html>`_.

* Nicht nativ in Twig, aber wichtig, wenn Sie eigene Module entwickeln: Mit der Twig-Templates-Mehrfachvererbung für Module können Sie das visuelle Erscheinungsbild Ihres OXID eShops schnell ändern, ohne interne Geschäftslogik und Codebasis zu beeinträchtigen. Ändert sich ein Modul, passt sich das Layout automatisch an.

  Weitere Informationen finden Sie unter `Understanding the OXID eShop template hierarchy and override system <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/theme/theme_template_hierarchy.html>`_.


* Die Namen in den Controller-Templates sind unabhängig von der Templating Engine.

  Dies erleichtert Ihnen das Einbinden alternativer Templating Engines, beispielsweise Smarty.

  Denn die Templating Engine findet die richtige Extension automatisch.

  Beispiel: Controller::$_sThisTemplate='page/content' statt 'page/content.tpl'

Betrieb
^^^^^^^

* Um Ihnen das Installieren, Konfigurieren und Warten von OXID eshops zu erleichtern, haben wir den Aufbau der OXID eShop-Konfigurationsdatei geändert.

  Weitere Informationen finden Sie unter

  * `Modules configuration and setup <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/module_configuration/modules_configuration.html>`_
  * `Troubleshooting <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/installation_setup/troubleshooting.html>`_

* Um Ihnen auch das Installieren, Konfigurieren und Betreiben von Modulen zu erleichtern, haben wir den Module-Handler so geändert, dass alle Modul-spezifischen Informationen in YAML-Dateien gespeichert sind, nicht mehr in der Datenbank.

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
.. todo: #tbd: Ref auf Doku-Kap.

Bisher konnten Sie eine Tracking-URL :emphasis:`:emphasis:`pro Shop` definieren (unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Weitere Einstellungen`).

Diese Tracking-URL ist nun die :emphasis:`Standard`-Tracking-URL.

Sie können sie durch eine eigene Tracking-URL :emphasis:`je Versandart` ersetzen, beispielsweise für DHL, UPS, DPD und so weiter.

Sobald die Paket-ID (je nach Versanddienstleister Tracking Code, Paketscheinnummer, Paketreferenz, Sendungsnummer usw.) bei der Bestellung eingetragen ist, steht der Tracking-Link, bestehend aus der Tracking-URL und der Paket-ID der Bestellung, zur Verfügung.

.. todo: #VL: Was genau ist die neue Funktion, wo finde ich sie?

Er wird dem Kunden zur Sendungsverfolgung mit der E-Mail zugeschickt, mit der ihm der Versand der Ware mitgeteilt wird. In der Bestellhistorie des Kunden im Frontend wird der Tracking-Link ebenfalls angezeigt.

Setup per Kommandozeile
^^^^^^^^^^^^^^^^^^^^^^^

Um das Implementieren Ihres Projekts zu vereinfachen, können Sie -- als Ergänzung zum webbasierten Setup -- Ihren OXID eShop über die Kommandozeile erstellen und konfigurieren.

Sie haben auf der OXID eShop console folgende Möglichkeiten:

* Erstellen Sie mit ``oe:setup:shop`` die Datenbank und konfigurieren Sie Ihren OXID eShop.
  |br|
  Die dafür notwendigen Informationen übergeben Sie mit Parametern.

* Installieren Sie mit ``oe:setup:demodata`` Demodaten.
* Legen Sie mit ``oe:admin:create-user`` den Shop-Administrator an.
* Wenn Sie die OXID eShop Professional oder Enterprise Edition haben fügen Sie mit ``oe:license:add`` Ihren Lizenzschlüssel hinzu.

  Es ist technisch nicht möglich, vorhandene Lizenzen durch neue zu ersetzen. Wenn Sie einen bestehende Lizenz durch eine andere tauschen, löschen Sie deshalb vorher mit ``oe:license:clear`` alle Lizenzen und fügen die neue Lizenz anschließend erneut hinzu.

Weitere Informationen finden Sie unter :doc:`Setup per Kommandozeile <../../installation/neu-installation/setup-kommandozeile>`

Modul-Installation per Kommandozeile
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Installieren oder deinstallieren Sie Module mit den neuen Kommandos der OXID eShop console ``oe:module:install`` und ``oe:module:uninstall``.

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

Kreditkarte als Zahlungsart
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die im OXID eShop implementierte Zahlungsart Kreditkarte unterstützen wir aus Sicherheitsgründen nicht mehr.

Nutzen Sie das Modul eines Zahlungsanbieters, um Ihren Kunden das Zahlen mit der Kreditkarte anzubieten.

Newsletter-Versand
^^^^^^^^^^^^^^^^^^

Aus technischen Gründen haben wir das Senden von Newsletter aus dem OXID eShop entfernt.

Senden Sie Newsletter, um Ihre Kunden über aktuelle Themen zu informieren, Tipps zu geben, Aktionen anzukündigen und Artikel zu bewerben.

Nutzen Sie dafür künftig jedoch Newsletter-Dienste, cloudbasierte Newsletter-Tools oder Newsletter-Software.

Kunden können Newsletter nach wie vor abonnieren. Die Liste Ihrer Newsletter-Abonnenten exportieren Sie als csv-Datei, um sie an einen externen Anbieter zu übergeben.

Weitere Informationen finden Sie unter :doc:`Newsletter <../../betrieb/newsletter/newsletter>`.

Nachrichten entfernt
^^^^^^^^^^^^^^^^^^^^

Bereits mit "Flow", dem Standard-Theme seit OXID eShop 6.0.0, konnten Nachrichten bereits nur über einen Link im Fußbereich aufgerufen werden.

Gestalten Sie beispielsweise Landing Pages mit Visual CMS (für die Professional und Enterprise Edition), um Neuigkeiten oder Angebote zu verbreiten.


Verschlüsselten Werte in der Datenbank
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Verschlüsselung von Werten in der Datenbank wurde entfernt, weil MySQL 8.0 diese Funktion nicht mehr unterstützt.

Dies verbessert die Lesbarkeit der Konfigurations Ihres eShops und erleichtert Ihnen die Entwicklung.

Komponenten
-----------

Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält folgende Komponenten:

.. todo: #VL: wo finde ich die Komponenten? Metapackage 7.0 wann fertig? -- VL: tbd: nä Woche.
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

.. todo: #VL: Folgende Komponenten ergänzen: Payone entfällt

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

Folgen Sie zum Installieren den den Anleitungen unter :doc:`Neu-Installation <../../installation/neu-installation/neu-installation>`.

.. todo: #tbd: oder Upgrade 6.5 ->7.0, sobald vorhanden

Korrekturen
-----------

Korrekturen:

* https://bugs.oxid-esales.com/changelog_page.php?version_id=344
* https://bugs.oxid-esales.com/changelog_page.php?version_id=630
* https://bugs.oxid-esales.com/changelog_page.php?version_id=728


.. Intern: oxbajt, Status: