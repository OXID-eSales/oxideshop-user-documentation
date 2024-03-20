OXID eShop 7.0.3
================

Release-Datum: 26.03.2024

Korrekturen
-----------

* Dedizierter Template-Cache für Subshops in der :productname:`OXID eShop Enterprise Edition`

  Beschreibung: In der :productname:`OXID eShop Enterprise Edition` konnte es dazu kommen, dass der Template-Cache von den Subshops überschrieben wurde.

  Dieses Verhalten trat auf, wenn die Modulinstallationen zwischen Haupt- und Subshops unterschiedlich waren und die Module eigene Templates mitbrachten. In einem Szenario, in dem ein Subshop ein Modul aktiviert hatte und seinen Template-Cache aufbaute, konnte der Hauptshop, beim Zugriff auf denselben Cache, feststellen, dass das entsprechende Modul bei ihm nicht aktiv war. Dies führte dazu, dass der eShop in den Wartungsmodus versetzt wurde.

  Lösung: Mit diesem Update stellen wir sicher, dass Subshops einen getrennten Template-Cache verwenden. Diese Änderung verhindert das beschriebene Verhalten, indem sie sicherstellt, dass Unterschiede in den Modulinstallationen und den verwendeten Templates zwischen Haupt- und Subshops keine Konflikte im Template-Cache verursachen. Dies gewährleistet eine stabilere und zuverlässigere Betriebsumgebung für Shops mit mehreren Subshops.

  Wir empfehlen allen Betreibern der :productname:`OXID eShop Enterprise Edition`, dieses Update zu implementieren, um die Integrität und Leistung ihrer Online-Shops zu optimieren.

* Performanceverbesserung: Modul-Erweiterungsketten aus dem Cache laden

  Beschreibung: Wenn Module im OXID eShop installiert sind, wurde die Class Chain für diese Module aus YAML-Dateien konstruiert. Dieser Prozess führte zu Performance-Einbußen, da das Lesen von YAML-Dateien im Vergleich zum Zugriff auf bereits im Cache gespeicherte Daten langsamer ist.

  Lösung: Wir optimieren das Laden von Modul-Erweiterungsketten, indem wir diese nun direkt aus dem Cache beziehen, anstatt auf YAML-Dateien zurückzugreifen. Dies verbessert die Shop-Performance, da der Zugriff auf den Cache schneller und effizienter ist. Die Class Chains für Module werden jetzt beim ersten Aufbau im Cache gespeichert und bei Bedarf von dort geladen. Dies reduziert die Lastzeiten und verbessert das allgemeine Nutzererlebnis im Shop.

  Vorteil: Diese Optimierung führt zu einer Beschleunigung des Shops.

  Wir empfehlen allen Shop-Betreibern, dieses Update zu implementieren, um von den Performance-Verbesserungen zu profitieren.

Bereinigung veralteter Services und Methoden
--------------------------------------------

Bestimmte Services und Methoden sind veraltet. Wir haben sie durch leistungsfähigere und modernere Alternativen ersetzt.

Im Zuge unserer laufenden Optimierungen haben wir daher folgende Komponenten entfernt:

* :code:`TemplateCacheServiceInterface`: Dieser Service ist nun obsolet, wir haben ihn durch neuere Caching-Mechanismen ersetzt.
* :code:`BasicContextInterface::getTemplateCacheDirectory()`: Diese Methode wird nicht mehr benötigt, da der Template-Cache jetzt über verbesserte Methoden verwaltet wird.

Diese Bereinigungsaktion hilft uns, die Wartbarkeit unseres Codes zu verbessern und die Performance des OXID eShops zu steigern.

Neuerungen und Optimierungen im Detail
--------------------------------------

Änderungen bei der Compilation im Metapackage finden Sie unter `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v7.0.2...v7.0.3>`_.

Die Korrekturen finden Sie im `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.4/CHANGELOG-7.0.md>`_.

Aktualisierte Komponenten
^^^^^^^^^^^^^^^^^^^^^^^^^

Wir haben die folgenden Komponenten und Module aktualisiert:

* `OXID eShop CE (Update von 7.0.3 auf 7.0.4) <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.4/CHANGELOG-7.0.md>`_

* `Apex theme (Update von 1.2.0 auf 1.2.1) <https://github.com/OXID-eSales/apex-theme/blob/v1.2.1/CHANGELOG-1.x.md>`_

* `Twig admin theme (Update von 1.2.0 auf 2.3.0) <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.3.0/CHANGELOG-2.x.md>`_
* `Twig component CE (Update von 2.2.0 auf 2.3.0) <https://github.com/OXID-eSales/twig-component/blob/v2.3.0/CHANGELOG.md>`_
* `Twig component PE (Update von 2.2.0 auf 2.3.0) <https://github.com/OXID-eSales/twig-component-pe/blob/v2.3.0/CHANGELOG.md>`_
* `Twig component EE (Update von 2.2.0 auf 2.3.0) <https://github.com/OXID-eSales/twig-component-ee/blob/v2.3.0/CHANGELOG.md>`_

* `OXID eShop demo data CE/PE (Update von 8.0.0 auf 8.0.1) <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.1/CHANGELOG.md>`_
* `OXID eShop demo data EE (Update von 8.0.1 auf 8.0.2) <https://github.com/OXID-eSales/oxideshop_demodata_ee/blob/v8.0.2/CHANGELOG.md>`_


Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält die folgenden Komponenten:

* `OXID eShop CE 7.0.4 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.4/CHANGELOG-7.0.md>`_
* `OXID eShop PE 7.0.0 <https://github.com/OXID-eSales/oxideshop_pe/blob/v7.0.0/CHANGELOG.md>`_
* `OXID eShop EE 7.0.1 <https://github.com/OXID-eSales/oxideshop_ee/blob/v7.0.1/CHANGELOG.md>`_
* `Apex theme 1.2.1 <https://github.com/OXID-eSales/apex-theme/blob/v1.2.1/CHANGELOG-1.x.md>`_
* `Twig admin theme 2.3.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.3.0/CHANGELOG-2.x.md>`_
* `Twig component CE 2.3.0 <https://github.com/OXID-eSales/twig-component/blob/v2.3.0/CHANGELOG.md>`_
* `Twig component PE 2.3.0 <https://github.com/OXID-eSales/twig-component-pe/blob/v2.3.0/CHANGELOG.md>`_
* `Twig component EE 2.3.0 <https://github.com/OXID-eSales/twig-component-ee/blob/v2.3.0/CHANGELOG.md>`_

* `OXID eShop composer plugin 7.1.1 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.1.1/CHANGELOG.md>`_
* `OXID eShop Views Generator 2.1.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.1.0/CHANGELOG.md>`_
* `OXID eShop demo data installer 3.1.1 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.1.1/CHANGELOG.md>`_
* `OXID eShop demo data CE/PE 8.0.1 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.1/CHANGELOG.md>`_
* `OXID eShop demo data EE 8.0.2 <https://github.com/OXID-eSales/oxideshop_demodata_ee/blob/v8.0.2/CHANGELOG.md>`_
* `OXID eShop doctrine migration integration 5.1.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.1.0/CHANGELOG.md>`_
* `OXID eShop facts 4.1.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.1.0/CHANGELOG.md>`_
* `Unified Namespace Generator 4.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v4.1.0/CHANGELOG.md>`_

* `GDPR Opt-In 3.0.1 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v3.0.1/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 2.0.2 <https://github.com/OXID-eSales/usercentrics/blob/v2.0.2/CHANGELOG.md>`_
* `Visual CMS 4.0.2 <https://github.com/OXID-eSales/visual_cms_module/blob/v4.0.2/CHANGELOG-4.0.md>`_ (PE/EE)
* `WYSIWYG Editor + Media Library 3.0.2 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v3.0.2/CHANGELOG.md>`_
* `Makaira 2.1.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.2/CHANGELOG.md>`_

Installation
------------

Zum Installieren oder Aktualisieren folgen Sie den Anleitungen im Abschnitt *Installation*:

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>`  |br|
:doc:`Patch-Update installieren <../../installation/update/patch-update>`

.. Intern: , Status: