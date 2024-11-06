OXID eShop 7.0.4
================

Release-Datum: xx.xx.2024


Änderungen
----------

Um eine Sicherheitslücke im Composer zu schließen, installieren Sie OXID eShop 7.0.4.

Aus Sicherheitsgründen erfordert OXID eShop 7.0.4 die Composer-Version 2.7.7

Weitere Informationen finden Sie unter

* `Composer Version 2.7.7 <https://github.com/composer/composer/releases/tag/2.7.7>`_
* `CVE-2024-35241 <https://github.com/advisories/GHSA-47f6-5gq3-vx9c>`_
* `CVE-2024-35242 <https://github.com/advisories/GHSA-v9qv-c7wm-wgmf>`_

Korrekturen
-----------

* Darstellung von Netto-Preisen im Frontend

  Beschreibung: Es konnte dazu kommen, dass im Frontend Prozentzeischen anstelle von 0% Mehrwertsteer ausgewiesen wurde.

  .. todo:: https://oxid-esales.atlassian.net/browse/OXDEV-7907 für mehr Infos

* Performanceverbesserung: ShopId-Berechnung nur einmal pro Request

  Beschreibung: Während eines Requests wurde unter Umständen mehrfach die ShopId berechnet

  Lösung: ShopId wird im COntext Object als private Property gespeichert.

  Vorteil: Diese Optimierung führt zu einer Beschleunigung des Shops.

  Wir empfehlen allen Shop-Betreibern, dieses Update zu implementieren, um von den Performance-Verbesserungen zu profitieren.

* VisualCMS: (nur Professional und Enterprise Edition)
  Automatische Migration auf neue Layout-Klassen.

  .. todo:: Informationen von Mikkel einholen


Neuerungen und Optimierungen im Detail
--------------------------------------

Änderungen bei der Compilation im Metapackage finden Sie unter `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v7.0.3...v7.0.4>`_.

Die Korrekturen finden Sie im `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.5/CHANGELOG-7.0.md>`_.

Aktualisierte Komponenten
^^^^^^^^^^^^^^^^^^^^^^^^^

Wir haben die folgenden Komponenten und Module aktualisiert:

* `OXID eShop CE (Update von 7.0.4 auf 7.0.5) <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.5/CHANGELOG-7.0.md>`_

* `Visual CMS (Update von 4.0.2 auf 4.1.1) <https://github.com/OXID-eSales/visual_cms_module/blob/v4.1.1/CHANGELOG-4.x.md>`_


Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält die folgenden Komponenten:

* `OXID eShop CE 7.0.5 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.5/CHANGELOG-7.0.md>`_
* `OXID eShop PE 7.0.0 <https://github.com/OXID-eSales/oxideshop_pe/blob/v7.0.0/CHANGELOG.md>`_
* `OXID eShop EE 7.0.1 <https://github.com/OXID-eSales/oxideshop_ee/blob/v7.0.1/CHANGELOG-7.0.md>`_
* `Apex theme 1.2.2 <https://github.com/OXID-eSales/apex-theme/blob/v1.2.2/CHANGELOG-1.x.md>`_
* `Twig admin theme 2.3.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.3.0/CHANGELOG-2.x.md>`_
* `Twig component CE 2.3.0 <https://github.com/OXID-eSales/twig-component/blob/v2.3.0/CHANGELOG.md>`_
* `Twig component PE 2.3.0 <https://github.com/OXID-eSales/twig-component-pe/blob/v2.3.0/CHANGELOG.md>`_
* `Twig component EE 2.3.0 <https://github.com/OXID-eSales/twig-component-ee/blob/v2.3.0/CHANGELOG.md>`_

* `OXID eShop composer plugin 7.1.1 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.1.1/CHANGELOG.md>`_
* `OXID eShop Views Generator 2.1.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.1.0/CHANGELOG.md>`_
* `OXID eShop demo data installer 3.1.1 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.1.1/CHANGELOG.md>`_
* `OXID eShop demo data CE 8.0.0 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.0/CHANGELOG.md>`_
* `OXID eShop demo data PE 8.0.0 <https://github.com/OXID-eSales/oxideshop_demodata_pe/blob/v8.0.0/CHANGELOG.md>`_
* `OXID eShop demo data EE 8.0.1 <https://github.com/OXID-eSales/oxideshop_demodata_ee/blob/v8.0.1/CHANGELOG.md>`_
* `OXID eShop doctrine migration integration 5.1.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.1.0/CHANGELOG.md>`_
* `OXID eShop facts 4.1.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.1.0/CHANGELOG.md>`_
* `Unified Namespace Generator 4.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v4.1.0/CHANGELOG.md>`_

* `GDPR Opt-In 3.0.1 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v3.0.1/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 2.0.2 <https://github.com/OXID-eSales/usercentrics/blob/v2.0.2/CHANGELOG.md>`_
* `Visual CMS 4.1.1 <https://github.com/OXID-eSales/visual_cms_module/blob/v4.1.1/CHANGELOG-4.x.md>`_ (PE/EE)
* `WYSIWYG Editor + Media Library 3.0.2 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v3.0.2/CHANGELOG.md>`_
* `Makaira 2.1.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.2/CHANGELOG.md>`_

Installation
------------

Folgen Sie zum Installieren oder Aktualisieren den Anleitungen unter :ref:`installation/index:Installation`.

.. Intern: , Status:
