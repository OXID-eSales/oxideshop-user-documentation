OXID eShop 7.3.0
================

Release-Datum: 15.04.2025

Änderungen im Überblick
-----------------------

Core
^^^^

* Unterstützung von PHP 8.4


APEX
^^^^

.. todo: #HR: Neuerungen ergänzen

Administration
^^^^^^^^^^^^^^

.. todo: #HR: Neuerungen ergänzen

Neue und aktualisierte Module
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: OXDEV-9193 (Cache clear button)?

* Nutzen Sie das neue Admin-Tool, um ...

Nutzen Sie mit OXID eShop 7.3 die Funktionen folgenderr aktualisierter Module:

.. todo: #HR: Neuerungen im :productname:`OXID Security-Modul` ergänzen: V. 2.0 = OXDEV-8930 CAPTCHA)

* :productname:`OXID Security-Modul` 2.0

  .. todo: #tbd: Verify URLs:
  .. todo: #HR: Kommen die Module alle gleichzeitig, sodass es sinnvoll ist, auf den Release Notes zu verweisen?

  Weitere Informationen finden Sie unter `OXID Security-Modul <https://docs.oxid-esales.com/modules/security/de/2.0/releases/security-module-200.html>`_.

* :productname:`OXID eShop Enterprise B2B Edition` 7.3

  Weitere Informationen finden Sie unter `OXID eShop Enterprise B2B Edition <https://docs.oxid-esales.com/b2b/de/7.3/releases/b2b-edition-730.html>`_.

* ERP
* Usercentrics
* GDPR
* Geoblocking
* eVAT

VCMS
^^^^

.. todo: #HR/#MF: VCMS-Neuerungen erg.

Korrekturen
-----------

.. todo: #HR: Bug-IDs und changelog-refs ergänzen:
    `#0007683 <https://bugs.oxid-esales.com/view.php?id=7683>`_
    `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.3.x/CHANGELOG-7.3.md>`_.


Im Detail
---------

User Experience
^^^^^^^^^^^^^^^

.. todo: #HR: kommt da etwas?

Verbessern Sie mit ...

Weitere Informationen finden Sie unter :ref:`tbd:tbd`.

Sicherheit & Zuverlässigkeit
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #HR: kommt da etwas?

* Aus Sicherheitsgründen erfordert OXID eShop 7.3.0 ...

   Weitere Informationen finden Sie unter ..

Barrierefreiheit
^^^^^^^^^^^^^^^^

Kleinere Verbesserungen ....

Weitere Informationen finden Sie im `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.3.x/CHANGELOG-7.3.md>`_.

Visual CMS & Mediathek
^^^^^^^^^^^^^^^^^^^^^^

.. todo: #HR: kommt da noch Info?

Siehe Changelogs:

* Visual CMS: https://github.com/OXID-eSales/visual_cms_module/blob/b-7.3.x/CHANGELOG-7.x.md
* Mediathek: https://github.com/OXID-eSales/media-library-module/blob/b-7.3.x/CHANGELOG.md
* WYSIWYG-Editor: https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/b-7.3.x/CHANGELOG.md


Neue Funktionen für Entwickler
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Nutzen Sie die volle Kompatibilität mit PHP 8.2 bis 8.4.

  Die Software unterstützt PHP-Versionen bis einschließlich PHP 8.4, jedoch müssen Sie beim Runden von Gleitkommazahlen die Änderungen in PHP 8.4 beachten, da sie zu unterschiedlichen Berechnungsergebnissen im Vergleich zu PHP 8.3 führen können.

  Weitere Informationen finden Sie im Abschnitt `Server- und Systemvoraussetzungen <https://docs.oxid-esales.com/eshop/de/7.3/installation/neu-installation/server-und-systemvoraussetzungen.html>`_ unter `PHP <https://docs.oxid-esales.com/eshop/de/7.3/installation/neu-installation/server-und-systemvoraussetzungen.html#php>`_.

* Erhöhen Sie mit der Twig Sandbox Extension die Sicherheit Ihrer Templates.

  Nutzen Sie die Twig Sandbox Extension, um mit dem {% sandbox %}-Tag die erlaubten Tags, Filter und Funktionen in Ihren Templates zu kontrollieren und so die Sicherheit beim dynamischen Template-Rendering zu verbessern.

  .. todo: #tbd: verify link

  Weitere Informationen finden Sie in der Entwickler-Dokumentation (Englisch) unter `Using the Twig Sandbox Extension <https://docs.oxid-esales.com/developer/en/7.3/development/modules_components_themes/theme/twig_sandbox.html>`_.

* Optimieren Sie die Verwaltung von OXID-Controllern.

  Registrieren Sie OXID-Controller als Dienste im Dependency Injection Container (DIC), um eine einfachere Handhabung, verbesserte Testbarkeit und eine flexiblere Erweiterung Ihrer Controller zu ermöglichen.

  .. todo: #tbd: verify link

  Weitere Informationen finden Sie in der Entwickler-Dokumentation (Englisch) unter `Controller as a service <https://docs.oxid-esales.com/developer/en/7.3/development/tell_me_about/controller_as_service.html>`_.

* Vereinfachen Sie die Verwaltung von Umgebungsvariablen.

  Verwenden Sie eine `.env`-Datei, um Umgebungsvariablen zu definieren und sicher in Ihre OXID eShop-Anwendung zu integrieren und auf diese Weise sensible Konfigurationswerte und umgebungsspezifische Einstellungen einfach zu verwalten.

  .. todo: #tbd: verify link

  Weitere Informationen finden Sie in der Entwickler-Dokumentation (Englisch) unter `Environment variables <https://docs.oxid-esales.com/developer/en/7.3/development/modules_components_themes/project/environment.html>`_.



Komponenten
-----------

Aktualisierte Komponenten
^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #HR: Versionsnummern der Komponenten aktualisieren

Wir haben die folgenden Komponenten und Module aktualisiert:

* `OXID eShop CE (Update von v7.1.1 auf v7.2.0) <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.2.0/CHANGELOG-7.2.md>`_
* OXID eShop PE (Update von v7.1.0 auf v7.2.0)
* OXID eShop EE (Update von v7.1.0 auf v7.2.0)
* `Apex theme (Update von v1.4.0 auf v2.0.0) <https://github.com/OXID-eSales/apex-theme/blob/v2.0.0/CHANGELOG-2.x.md#v200---2024-10-14>`_
* `Twig admin theme (Update von v2.4.0 auf v2.5.0) <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.5.0/CHANGELOG-2.x.md>`_
* `Twig component CE (Update von v2.4.0 auf v2.5.0) <https://github.com/OXID-eSales/twig-component/blob/v2.5.0/CHANGELOG-2.x.md>`_
* Twig component PE (Update von v2.4.0 auf v2.5.0)
* Twig component EE (Update von v2.4.0 auf v2.5.0)
* `OXID eShop demo data CE (Update von v8.0.1 auf v8.0.2) <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.1/CHANGELOG.md>`_
* OXID eShop demo data PE (update von v8.0.1 auf v8.0.2)
* OXID eShop demo data EE (Update von v8.0.2 auf v8.0.3)
* `OXID eShop Demodata Installer (Update von 3.2.0 auf 3.3.0) <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_
* `OXID eShop doctrine migration integration (Update von v5.2.0 auf v5.3.0) <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.3.0/CHANGELOG-5.x.md>`_
* `WYSIWYG Editor + Mediathek (Update von v4.1.0 auf v4.2.0) <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.2.0/CHANGELOG.md>`_
* `GDPR opt-in (Update von v4.0.0 auf v4.1.0) <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.1.0/CHANGELOG.md#v410---2024-10-14>`_
* `Media Library Module (Update von v2.0.1 auf v2.1.1) <https://github.com/OXID-eSales/media-library-module/blob/v2.1.1/CHANGELOG.md>`_
* Visual CMS (Update von v6.0.1 auf v7.0.2)

Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #HR: Versionsnummern aktualisieren

Die Compilation enthält die folgenden Komponenten:

* `OXID eShop CE 7.2.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.2.0/CHANGELOG-7.2.md>`_
* OXID eShop PE 7.2.0
* OXID eShop EE 7.2.0

* `Apex theme 2.0.0 <https://github.com/OXID-eSales/apex-theme/blob/v2.0.0/CHANGELOG-2.x.md>`_

* `Twig admin theme 2.5.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.5.0/CHANGELOG-2.x.md>`_
* `Twig component CE 2.5.0 <https://github.com/OXID-eSales/twig-component/blob/v2.5.0/CHANGELOG-2.x.md>`_
* Twig component PE 2.5.0
* Twig component EE 2.5.0

* `OXID eShop composer plugin 7.2.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.2.0/CHANGELOG-7.x.md>`_
* `OXID eShop Views Generator 2.2.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* `OXID eShop demo data installer 3.3.0 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_

* `OXID eShop demo data CE 8.0.2 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.2/CHANGELOG.md>`_
* OXID eShop demo data PE 8.0.2
* OXID eShop demo data EE 8.0.3

* `OXID eShop doctrine migration integration 5.3.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.3.0/CHANGELOG-5.x.md>`_
* `OXID eShop facts 4.2.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.2.0/CHANGELOG-4.x.md>`_
* `Unified Namespace Generator 5.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.1.0/CHANGELOG.md>`_

* `GDPR Opt-In 4.1.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.1.0/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 3.0.0 <https://github.com/OXID-eSales/usercentrics/blob/v3.0.0/CHANGELOG.md>`_
* Visual CMS 7.0.2 (PE/EE)

* `WYSIWYG Editor 4.2.0 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.2.0/CHANGELOG.md>`_
* `Mediathek 2.1.1 <https://github.com/OXID-eSales/media-library-module/blob/v2.1.1/CHANGELOG.md>`_
* `Makaira 2.1.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.2/CHANGELOG.md>`_
* `Eye-Able 3.0.3 <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/blob/v3.0.3/CHANGELOG.md>`_


Installation
------------

Zum Installieren oder Aktualisieren folgen Sie den Anleitungen unter :doc:`Installation <../../installation/index>`.


.. Intern: , Status:
