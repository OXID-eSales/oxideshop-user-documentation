OXID eShop 7.0.0
================

.. todo: #VL: Datum

Veröffentlichungstermin RC 1: 28.02.2023

.. todo: #VL: Was ist das Wichtige an V. 7?

Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält folgende Komponenten:

.. todo: #VL: wo finde ich die Komponenten? Metapackage 7.0 wann fertig?

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

.. todo: #VL: Folgende Komponenten ergänzen:

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

Es wird nicht empfohlen, ein Update des OXID eShop auf die Version 7.0.0 RC 1 vorzunehmen. Eine Update-Anleitung wird mit der Veröffentlichung der finalen Version zur Verfügung stehen.

-----------------------------------------------------------------------------------------

Neue Funktionen
---------------
Setup per Kommandozeile
^^^^^^^^^^^^^^^^^^^^^^^
Als Ergänzung zum webbasierten Setup kann OXID eShop jetzt auch über die Kommandozeile erstellt und konfiguriert werden. Das neue Kommando der OXID eShop console ``oe:setup:shop`` erstellt die Datenbank und konfiguriert den Shop. Die dafür notwendigen Informationen werden mit Parametern übergeben. In weiteren Schritten können mit ``oe:setup:demodata`` Demodaten installiert und mit ``oe:admin:create-user`` der Shop-Administrator erstellt werden. Für OXID eShop Professional und Enterprise Edition fügt das Kommando ``oe:license:add`` einen gültigen Lizenzschlüssel hinzu. Siehe: :doc:`Setup per Kommandozeile <../../installation/neu-installation/setup-kommandozeile>`

Modul-Installation per Kommandozeile
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Module können mit den neuen Kommandos der OXID eShop console ``oe:module:install`` und ``oe:module:uninstall`` installiert und deinstalliert werden. Alle Informationen dazu finden Sie in der englischsprachigen Entwicklerdokumentation: https://docs.oxid-esales.com/developer/en/7.0-rc.1/development/modules_components_themes/module/tutorials/module_setup.html und https://docs.oxid-esales.com/developer/en/7.0-rc.1/development/modules_components_themes/module/uninstall/index.html.

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------

.. todo: #HR/VL: Stimmen die Folgenden Anpassungen?

Tracking-URL je Versandart
^^^^^^^^^^^^^^^^^^^^^^^^^^
Bisher konnte eine Tracking-URL pro Shop definiert werden. Sie wird im Administrationsbereich unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Weitere Einstellungen` eingetragen. Diese Tracking-URL ist nun die Standard-Tracking-URL und kann durch eine eigene Tracking-URL je Versandart ersetzt werden.

Sobald die Paket-ID (je nach Versanddienstleister Tracking Code, Paketscheinnummer, Paketreferenz, Sendungsnummer usw.) bei der Bestellung eingetragen ist, steht der Tracking-Link, bestehend aus der Tracking-URL und der Paket-ID der Bestellung, zur Verfügung. Er wird dem Kunden zur Sendungsverfolgung mit der E-Mail zugeschickt, mit der ihm der Versand der Ware mitgeteilt wird. In der Bestellhistorie des Kunden im Frontend wird der Tracking-Link ebenfalls angezeigt.

Kreditkarte als Zahlungsart nicht mehr unterstützt
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Die im OXID eShop implementierte Zahlungsart Kreditkarte wird nicht mehr unterstützt. Shopbetreiber, welche diese Zahlungsart benötigen, sollten auf Module entsprechender Zahlungsanbieter zurückgreifen.

Newsletter-Versand entfernt
^^^^^^^^^^^^^^^^^^^^^^^^^^^
Newsletter stellen eine unkomplizierte und schnelle Möglichkeit dar, die Kunden des Onlineshops über aktuelle Themen zu informieren, Tipps zu geben, Aktionen anzukündigen und Artikel zu bewerben. Kunden können den Newsletter nach wie vor abonnieren, aber der eigentlich Versand wurde aus dem OXID eShop entfernt. Dafür sollten zukünftig ausschließlich Newsletter-Dienste, cloudbasierte Newsletter-Tools oder Newsletter-Software genutzt werden. OXID eShop bietet die Möglichkeit, eine Liste der Newsletter-Abonnenten zu exportieren, die dann an einen externen Anbieter übergeben werden kann. Siehe: :doc:`Newsletter <../../betrieb/newsletter/newsletter>`

Nachrichten entfernt
^^^^^^^^^^^^^^^^^^^^
Nachrichten konnten mit "Flow", Standard-Theme seit OXID eShop 6.0.0, bereits nur über einen Link im Fußbereich aufgerufen werden. Nun wurde diese wenig genutzte Funktion komplett aus dem Shop entfernt.

Änderungen bei Modulen
^^^^^^^^^^^^^^^^^^^^^^

* Native Composer-Unterstützung für Module: Dateien verbleiben komplett im Verzeichnis :file:`/vendor`. Sie werden nicht nach :file:`/source/modules` kopiert.
* Das Caching für Modul-Assets - statische Dateien, welche von Modulen im Frontend benötigt werden (CSS-, JavaScript- oder Bild-Dateien) - wurde optimiert.

Keine verschlüsselten Werte in der Datenbank
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Die Verschlüsselung von Werten in der Datenbank wurde entfernt, da diese Funktion nicht mehr von MySQL 8.0 unterstützt wird.

-----------------------------------------------------------------------------------------

.. todo: include as of 7.x:
    Korrekturen
    -----------
    Korrekturen 7.0.0 RC 1: https://bugs.oxid-esales.com/changelog_page.php?version_id=344


.. Intern: oxbajt, Status: