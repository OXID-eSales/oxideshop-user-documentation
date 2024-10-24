OXID eShop 7.2.0
================

Release-Datum: 09.04.2024

Die Änderungen im Überblick
---------------------------

* Sicherheit & Zuverlässigkeit

.. todo


* Barrierefreiheit



* Visual CMS & Mediathek



* Verbesserung im Shop-Administrationsbereich



* Neue Funktionen für Entwickler




Verbesserung im Shop-Administrationsbereich
-------------------------------------------

Newsletter
^^^^^^^^^^
.. todo: OXDEV-7028: Newsletter export data enhanced · OXID-eSales/oxideshop-user-documentation@a19e24b -- keine neue Funktion, nur Doku erweitert: betrieb/newsletter/newsletter.rst

As a shop owner I want to know exactly what Export users function does: https://oxid-esales.atlassian.net/browse/OXDEV-7028

Statt
Die Datensätze werden in eine CSV-Datei geschrieben, deren Dateinamen aus :file:`Export_recipients_`, einem angehängten Datum im Format JJJJ-MM-TT und der Dateiendung :file:`.csv` besteht. Die Datei enthält Anrede, Vorname, Nachname, E-Mail-Adresse, Opt-in-Status und zugeordnete Benutzergruppen für jeden Abonnenten. Opt-in-Status kann abonniert, nicht abonniert oder nicht bestätigt sein. Die Datei kann direkt im verwendeten Browser geöffnet oder lokal auf dem Rechner gespeichert werden.
Die Datensätze werden in eine CSV-Datei geschrieben, deren Dateinamen aus :file:`Export_user_recipient_status_`, einem angehängten Datum im Format JJJJ-MM-TT und der Dateiendung :file:`.csv` besteht. Die Datei enthält Anrede, Vorname, Nachname, E-Mail-Adresse, Opt-in-Status, Land und zugeordnete Benutzergruppen für jeden Abonnenten. Opt-in-Status kann abonniert, nicht abonniert oder nicht bestätigt sein. Die Datei kann direkt im verwendeten Browser geöffnet oder lokal auf dem Rechner gespeichert werden.

:ref:`betrieb/newsletter/newsletter:Newsletter`


Make mail sending optional (configuration option)
^^^^^^^^^^^^^^^^^^^^^^^^^^

New parameter oxid_esales.email.disable_order_emails to enable and disable sending order emails

.. todo: https://oxid-esales.atlassian.net/browse/OXDEV-6846
.. todo: https://github.com/OXID-eSales/developer_documentation/commit/5c970ea708e2f2b9dd67a2cfcd0129acb5df9c1a

.. todo: Ref testen: https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/parameters.html`_




Neue Funktionen für Entwickler
------------------------------

Abhängigkeiten zwischen Modulen definieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^













Sicherheit & Zuverlässigkeit
----------------------------


Barrierefreiheit
----------------



Visual CMS & Mediathek
----------------------

Visual CMS
^^^^^^^^^^


Mediathek
^^^^^^^^^

* Profitieren Sie von der erweiterten Unterstützung folgender Bewegtbild- und Vektor-Formate:

  * AVIF:

    * Beschleunigen Sie das Laden Ihrer Webseiten durch eine um 20-30 % kleinere Dateigröße im Vergleich zu WebP, bei gleicher Qualität.
    * Integrieren Sie dank des Open-Source AV1 Videocodecs animierte Bilder über Bild-Widgets in Ihre Seiten.

      Im Vergleich zu anderen Formaten für animierte Bilder wie GIF, APNG und WebP sowie zu Videoformaten wie H.264/AVC und H.265/HEVC bietet AVIF in der Regel eine verbesserte Leistung und kleinere Dateigrößen.

    * Nutzen Sie mit dem AVIF-Bildformat weitere fortgeschrittene Funktionen wie HDR sowie Ebenen, um die Qualität und Auflösung des dekodierten Bildes zu verbessern und unabhängige Ebenen für spezifische Zwecke bereitzustellen.

  * SVG:

    * Nutzen Sie Bilder, die ohne Qualitätsverlust in beliebiger Größe skaliert werden können.
    * Nutzen Sie mit SVG interaktive Elemente wie Links, Animationen und JavaScript-Interaktionen direkt innerhalb der Grafik.

      Erstellen Sie damit interaktive Diagramme, Karten, Infografiken und anderen grafische Elemente, die Benutzeraktionen ermöglichen.

    * Erstellen Sie mit SVG-Dateien barrierefreie Inhalte.

      Hintergrund: SVG-Dateien sind textbasiert. Deshalb können sie leicht von Screenreadern und anderen Hilfstechnologien interpretiert werden.

* Verwalten Sie neben Bildern die Dateiformate PDF und ZIP, um Ihren Kunden beispielsweise Datenblätter, technische Zeichnungen oder Werbematerial bereitzustellen.

  Weitere Informationen finden Sie in der Visual CMS-Dokumentation unter `Mediathek <https://docs.oxid-esales.com/modules/vcms/de/5.0/funktionsbeschreibung/mediathek.html#mediathek>`_.

* Erhalten Sie Dank des verbesserten Generierens von Bildvorschauen das ursprüngliche Dateiformat und somit auch Transparenzen von Grafiken.
* Bringen Sie mit den folgenden Funktionen Ordnung in Ihre Mediathek:

  * Ordner anlegen, um Medien-Dateien per Drag-and-drop übersichtlich zu sortieren (:ref:`oxid-eshop-710-03`, Pos. 1).
  * Dateinamen bei Bedarf ändern  (:ref:`oxid-eshop-710-03`, Pos. 2).

  .. _oxid-eshop-710-03:

  .. figure:: ../../media/screenshots/oxid-eshop-710-03.png
     :alt: Medien in der Mediathek verwalten
     :width: 650
     :class: with-shadow

     Abb.: Medien in der Mediathek verwalten

  Weitere Informationen finden Sie in der Visual CMS-Dokumentation unter `Mediathek <https://docs.oxid-esales.com/modules/vcms/de/5.0/funktionsbeschreibung/mediathek.html#mediathek>`_.

**Weitere Informationen**

Weitere Informationen zu Änderungen finden Sie in den folgenden Changelogs:

* Visual CMS: https://github.com/OXID-eSales/visual_cms_module/blob/v5.0.0/CHANGELOG.md
* WYSIWYG-Editor: https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.0.0/CHANGELOG.md
* Mediathek: https://github.com/OXID-eSales/media-library-module/blob/v1.0.0/CHANGELOG.md

Verbesserung im Shop-Administrationsbereich
-------------------------------------------



Weitere Informationen finden Sie in der Beschreibung, wie Sie :ref:`Produkte zeitgesteuert aktivieren <zeitaktivierung>` (:ref:`oxbaci02`, Pos. 1).

Neue Funktionen für Entwickler
------------------------------

Abhängigkeiten zwischen Modulen definieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


Clean Up
--------

Einladungs-Funktion
^^^^^^^^^^^^^^^^^^^

Um Ihren registrierten Kunden die Möglichkeit zu bieten, Freunde einzuladen und dafür Bonuspunkte zu erhalten, konnten Sie bis zur Version 7.0 des OXID eShops unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Einladungen` die Funktion :guilabel:`Einladungen` aktivieren.

Aufgrund des Risikos von Missbrauch durch Spam-Attacken haben wir jedoch beschlossen, diese Funktion aus der Benutzeroberfläche zu entfernen. Sie ist noch im 7.x-Code vorhanden. Ab Version 8.0 wird sie entfernt.

Veraltete (deprecated) Konsolenklassen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Folgende Konsolenklassen (console classes) aus dem internen Namensraum sind als veraltet markiert und werden im nächsten Major Release entfernt.

Prüfen Sie Ihren Code, um festzustellen, ob und wo Sie die als veraltet markierten Klassen verwenden.

Nachdem Sie gegebenenfalls Ihren Code aktualisiert haben, um die veralteten Klassen zu ersetzen, führen Sie Tests durch, um sicherzustellen, dass Ihre Anwendungen weiterhin wie erwartet funktionieren.

* :code:`Executor`
* :code:`ExecutorInterface`
* :code:`CommandsProvider`
* :code:`CommandsProviderInterface`

Komponenten
-----------

Repositories ohne Link sind private Repositories.

Geänderte und neue Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Wir haben die folgenden Komponenten und Module aktualisiert.

* Neu: `Eye-Able 3.0.1 <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/tree/v3.0.1>`_
* `OXID eShop CE (Update von 7.0.4 auf 7.1.0) <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.1.0/CHANGELOG-7.1.md>`_
* `Twig component (Update von 2.2.0 auf 2.4.0) <https://github.com/OXID-eSales/twig-component/blob/v2.4.0/CHANGELOG-2.x.md>`_
* `OXID eShop composer plugin (Update von 7.1.1 auf 7.2.0) <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.2.0/CHANGELOG-7.x.md>`_
* `OXID eShop Views Generator (Update von 2.1.0 auf 2.2.0) <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* `OXID eShop DemoData installer (Update von 3.1.1 auf 3.2.0) <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.2.0/CHANGELOG-3.x.md>`_
* `OXID eShop demodata CE (Update von 8.0.0 auf 8.0.1) <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.1/CHANGELOG.md>`_
* `OXID eShop doctrine migration integration (Update von 5.1.0 auf 5.2.0) <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.2.0/CHANGELOG-5.x.md>`_
* `OXID eShop facts (Update von 4.1.0 auf 4.2.0) <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.2.0/CHANGELOG-4.x.md>`_
* `Unified Namespace Generator (Update von 4.1.0 auf 5.0.0) <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.0.0/CHANGELOG.md>`_

* OXID eShop PE (Update von 7.0.0 auf 7.1.0)
* Twig component for Professional Edition (Update von 2.2.0 auf 2.4.0)
* OXID eShop demodata PE (Update von 8.0.0 auf 8.0.1)

* OXID eShop EE (Update von 7.0.1 auf 7.1.0)
* Twig component for Enterprise Edition (Update von 2.2.0 auf 2.4.0)
* OXID eShop demodata EE (Update von 8.0.1 to auf 8.0.2)

* `APEX Theme (Update von 1.2.1 auf 1.3.0) <https://github.com/OXID-eSales/apex-theme/blob/v1.3.0/CHANGELOG-1.x.md>`_

* `WYSIWYG Editor (Update von 3.0.2 auf 4.0.0) <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.0.0/CHANGELOG.md>`_
* Neu (extrahiert aus WYSIWYG Editor): `Mediathek (1.0.0) <https://github.com/OXID-eSales/media-library-module/blob/v1.0.0/CHANGELOG.md>`_
* Visual CMS (update from 4.0.2 to 5.0.1)

* `GDPR opt-in module (Update von 3.0.1 auf 4.0.0) <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.0.0/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics (Update von 2.0.2 auf 3.0.0) <https://github.com/OXID-eSales/usercentrics/blob/v3.0.0/CHANGELOG.md>`_

Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält die folgenden Komponenten (aktualisierte Versionen):

* `OXID eShop CE 7.1.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.1.0/CHANGELOG-7.1.md>`_
* OXID eShop PE 7.1.0
* OXID eShop EE 7.1.1

* `Apex theme 1.3.0 <https://github.com/OXID-eSales/apex-theme/blob/v1.3.0/CHANGELOG-1.x.md>`_

* `Twig admin theme 2.2.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.2.0/CHANGELOG.md>`_
* `Twig component CE 2.4.0 <https://github.com/OXID-eSales/twig-component/blob/v2.4.0/CHANGELOG-2.x.md>`_
* Twig component PE 2.4.0
* Twig component EE 2.4.0

* `OXID eShop composer plugin 7.2.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.2.0/CHANGELOG-7.x.md>`_
* `OXID eShop Views Generator 2.2.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* `OXID eShop demo data installer 3.2.0 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.2.0/CHANGELOG-3.x.md>`_

* `OXID eShop demo data CE 8.0.1 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.1/CHANGELOG.md>`_
* OXID eShop demo data PE 8.0.1
* OXID eShop demo data EE 8.0.2

* `OXID eShop doctrine migration integration 5.2.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.2.0/CHANGELOG-5.x.md>`_
* `OXID eShop facts 4.2.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.2.0/CHANGELOG-4.x.md>`_
* `Unified Namespace Generator 5.0.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.0.0/CHANGELOG.md>`_

* `GDPR Opt-In 4.0.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.0.0/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 3.0.0 <https://github.com/OXID-eSales/usercentrics/blob/v3.0.0/CHANGELOG.md>`_
* Visual CMS 5.0.1 (PE/EE)

* `WYSIWYG Editor 4.0.0 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.0.0/CHANGELOG.md>`_
* `Mediathek (1.0.0) <https://github.com/OXID-eSales/media-library-module/blob/v1.0.0/CHANGELOG.md>`_
* `Makaira 2.1.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.2/CHANGELOG.md>`_
* `Eye-Able 3.0.1 <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/tree/v3.0.1>`_


Korrekturen
-----------

Die Korrekturen finden Sie im `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.1.x/CHANGELOG-7.1.md>`_.

Installation
------------

Zum Installieren oder Aktualisieren folgen Sie den Anleitungen unter :doc:`Installation <../../installation/index>`.


.. Intern: , Status:
