OXID eShop 7.1.1
================

Release-Datum: xx.xx.2024

Die Änderungen im Überblick
---------------------------

Änderungen
----------

Um eine Sicherheitslücke im Composer zu schließen, installieren Sie OXID eShop 7.1.1.

Aus Sicherheitsgründen erfordert OXID eShop 7.1.1 die Composer-Version 2.7.7

Weitere Informationen finden Sie unter

* `Composer Version 2.7.7 <https://github.com/composer/composer/releases/tag/2.7.7>`_
* `CVE-2024-35241 <https://github.com/advisories/GHSA-47f6-5gq3-vx9c>`_
* `CVE-2024-35242 <https://github.com/advisories/GHSA-v9qv-c7wm-wgmf>`_


Wysiwig-Editor:

Verbesserung der Sicherheit: CMS content wird vorgefiltert, so dass Javascript im Content nicht mehr im
Shop-Backoffice ausgeführt wird.


Korrekturen
-----------

* Die Compilation 7.1.1 beinhaltet die Korrekturen aus Compilation 7.0.4:
  - Netto-Preise im Frontend
  - Optimierte ShopId-Berechnung

* PR #962 Rückgabewert beim Löschen von Usergruppen `<https://github.com/OXID-eSales/oxideshop_ce/pull/962>`_.

* PR #963 Laden von Übersetzungsfiles für Custom Themes  `<https://github.com/OXID-eSales/oxideshop_ce/pull/963>`_.

* APEX Theme enthält einige Korrekturen, Details im Changelog

* Mediathek enthält einige Korrekturen, Details im Changelog

* VisualCMS: (nur Professional und Enterprise Edition) Automatische Migration auf neue Layout-Klassen, Details im Changelog.


Neuerungen und Optimierungen im Detail
--------------------------------------

Änderungen bei der Compilation im Metapackage finden Sie unter `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v7.1.0...v7.1.1>`_.

Die Korrekturen finden Sie im `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.1.1/CHANGELOG-7.1.md>`_.

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


Korrekturen
-----------

Die Korrekturen finden Sie im `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.1.x/CHANGELOG-7.1.md>`_.

Installation
------------

Zum Installieren oder Aktualisieren folgen Sie den Anleitungen unter :doc:`Installation <../../installation/index>`.


.. Intern: , Status:
