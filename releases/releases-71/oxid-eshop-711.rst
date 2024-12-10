OXID eShop 7.1.1
================

Release-Datum: 02.11.2024

Sicherheits-Updates
-------------------

Composer
^^^^^^^^

Sicherheitslücke geschlossen: Installation von OXID eShop 7.1.1 erforderlich, um eine Schwachstelle im Composer zu beheben.

Voraussetzung: OXID eShop 7.1.1 benötigt Composer Version 2.7.7 zur Erhöhung der Sicherheit.

Weitere Informationen finden Sie unter

* `Composer Version 2.7.7 <https://github.com/composer/composer/releases/tag/2.7.7>`_
* `CVE-2024-35241 <https://github.com/advisories/GHSA-47f6-5gq3-vx9c>`_
* `CVE-2024-35242 <https://github.com/advisories/GHSA-v9qv-c7wm-wgmf>`_


WYSIWYG-Editor
^^^^^^^^^^^^^^

Verbesserung der Sicherheit: JavaScript im CMS-Content wird im Shop-Backoffice nicht mehr ausgeführt, da eine Vorfilterung implementiert wurde.

Korrekturen
-----------

* Die Compilation 7.1.1 enthält die Korrekturen aus Compilation 7.0.4:

  * Frontend: Korrekte Darstellung von Netto-Preisen
  * Backend: Optimierung der Performance durch Verbesserung der `ShopId`-Berechnung

  Weitere Informationen finden Sie in den `Release Notes für OXID eShop 7.0.4 <https://docs.oxid-esales.com/eshop/de/7.0/releases/releases-70/oxid-eshop-704.html#korrekturen>`_.

* Benutzergruppen: PR #962 korrigiert den Rückgabewert beim Löschen von Benutzergruppen. Details finden Sie unter `GitHub-PR #962 <https://github.com/OXID-eSales/oxideshop_ce/pull/962>`_.
* Übersetzungsdateien: PR #963 ermöglicht das Laden von Übersetzungsdateien für benutzerdefinierte Themes. Details finden Sie unter `GitHub-PR #963 <https://github.com/OXID-eSales/oxideshop_ce/pull/963>`_.
* APEX Theme: Verschiedene Korrekturen (Details siehe Changelog).
* Mediathek: Verschiedene Korrekturen (Details siehe Changelog).
* VisualCMS (nur PE/EE): Automatische Migration auf neue Layout-Klassen (Details siehe Changelog).

Das Changelog finden Sie unter `Changelog 7.1.x <https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.1.x/CHANGELOG-7.1.md>`_.

Komponenten
-----------

Änderungen in der Compilation sind im Metapackage einsehbar. Details finden Sie auf Github im Vergleich der Versionen `v7.1.0...v7.1.1 <https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v7.1.0...v7.1.1>`_.

Aktualisierte Komponenten
^^^^^^^^^^^^^^^^^^^^^^^^^

Wir haben die folgenden Komponenten und Module aktualisiert:

* `OXID eShop CE (Update von 7.1.0 auf 7.1.1) <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.1.1/CHANGELOG-7.1.md>`_
* `WYSIWYG Editor Module (Update von 4.0.0 auf 4.1.0) <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.1.0/CHANGELOG.md>`_
* `Visual CMS (Update von 5.0.1 auf 6.0.1) <https://github.com/OXID-eSales/visual_cms_module/blob/v6.0.1/CHANGELOG-6.x.md>`_
* `Eye Able Assist (Update von 3.0.1 auf 3.0.3) <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/blob/v3.0.3/CHANGELOG.md>`_
* `APEX Theme (Update von 1.3.0 auf 1.4.0) <https://github.com/OXID-eSales/apex-theme/blob/v1.4.0/CHANGELOG.md>`_
* `Mediathek (Update von 1.0.0 auf 2.0.1) <https://github.com/OXID-eSales/media-library-module/blob/v2.0.1/CHANGELOG.md>`_
* `Unified Namespace Generator (Update von 5.0.0 auf 5.1.0) <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.1.0/CHANGELOG.md>`_


Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält die folgenden Komponenten (aktualisierte Versionen):

* `OXID eShop CE 7.1.1 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.1.1/CHANGELOG-7.1.md>`_
* OXID eShop PE 7.1.0
* OXID eShop EE 7.1.0

* `Apex theme 1.4.0 <https://github.com/OXID-eSales/apex-theme/blob/v1.4.0/CHANGELOG.md>`_

* `Twig admin theme 2.4.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.4.0/CHANGELOG-2.x.md>`_
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
* `Unified Namespace Generator 5.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.1.0/CHANGELOG.md>`_

* `GDPR Opt-In 4.0.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.0.0/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 3.0.0 <https://github.com/OXID-eSales/usercentrics/blob/v3.0.0/CHANGELOG.md>`_
* Visual CMS 6.0.1 (PE/EE)

* `WYSIWYG Editor 4.1.0 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.1.0/CHANGELOG.md>`_
* `Mediathek 2.0.1 <https://github.com/OXID-eSales/media-library-module/blob/v2.0.1/CHANGELOG.md>`_
* `Makaira 2.1.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.2/CHANGELOG.md>`_
* `Eye-Able 3.0.3 <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/tree/v3.0.3>`_

Installation
------------

Zum Installieren oder Aktualisieren folgen Sie den Anleitungen unter :doc:`Installation <../../installation/index>`.


.. Intern: , Status:
