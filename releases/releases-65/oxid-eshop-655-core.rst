OXID eShop 6.5.5 Core Edition
=============================

Die OXID eShop 6.5.5 Core Edition ist eine Alternative zur
Standard-Compilation 6.5.5. Sie enthält den gleichen
Shop-Kern und seine Abhängigkeiten, jedoch ohne die
mitgelieferten Module und deren Abhängigkeiten. So können
Sie Module unabhängig über Composer verwalten.

Hintergrund
-----------

Die Standard-Compilation OXID eShop 6.5.5 legt den
Shop-Kern und alle Module auf feste Versionen fest.
OXID eShop 6.5 erhält kritische Sicherheitsfixes auf
Best-Effort-Basis, die Compilation als Ganzes erhält
jedoch keine neuen Releases mehr. Dadurch kann es
vorkommen, dass Sie einzelne Module nicht unabhängig
aktualisieren können.

Die 6.5.5 Core Edition löst dies durch ein Metapackage,
das nur den Shop-Kern und seine Infrastruktur enthält.
Sie entscheiden selbst, welche Module Sie installieren
und in welcher Version.

Was sich ändert
---------------

* Das Standard-Metapackage
  (``oxid-esales/oxideshop-metapackage-ce`` bzw. PE/EE)
  wird durch das entsprechende Core-Edition-Metapackage
  ersetzt.
* Der Shop-Kern bleibt in der gleichen Version — dies
  ist kein Upgrade.
* Zuvor in der Compilation enthaltene Module müssen als
  explizite Composer-Anforderungen hinzugefügt werden,
  wenn Sie sie behalten möchten.

Die vollständige Liste der nicht enthaltenen Module und
die Migrationsanleitung finden Sie unter
:doc:`Core Edition <../../installation/core-edition>`.

.. note::

   Wir empfehlen das Update auf die aktuelle OXID eShop
   Version (7.x) für vollen Support, aktive Wartung und
   die neuesten Sicherheitsverbesserungen. Die Core
   Edition für 6.5 richtet sich an Shops, die nicht
   sofort auf 7.x migrieren können.

Bestandteile der Core Edition (CE)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* OXID eShop CE 6.14.4: `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.14.4/CHANGELOG.md>`_
* OXID eShop Composer Plugin 5.2.2: `Changelog <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.2.2/CHANGELOG.md>`_
* OXID eShop DB Views Generator 1.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v1.3.0/CHANGELOG.md>`_
* OXID eShop Demodata CE 6.0.5: `Changelog <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v6.0.5/CHANGELOG.md>`_
* OXID eShop Demodata Installer 1.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v1.4.0/CHANGELOG.md>`_
* OXID eShop Doctrine Migration Wrapper 3.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v3.4.0/CHANGELOG.md>`_
* OXID eShop Facts 2.4.1: `Changelog <https://github.com/OXID-eSales/oxideshop-facts/blob/v2.4.1/CHANGELOG.md>`_
* OXID eShop Unified Namespace Generator 2.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v2.3.0/CHANGELOG.md>`_
* Theme "Flow" 3.8.1: `Changelog <https://github.com/OXID-eSales/flow_theme/blob/v3.8.1/CHANGELOG.md>`_
* Theme "Wave" 1.8.0: `Changelog <https://github.com/OXID-eSales/wave-theme/blob/v1.8.0/CHANGELOG.md>`_

Erfordert Composer 2.7.7. Infrastruktur-Abhängigkeiten
(Symfony, Doctrine, Monolog, PHPMailer, Smarty etc.)
sind im Metapackage festgelegt.

Die folgenden Module und deren Abhängigkeiten aus der
Standard-Compilation 6.5.5 sind **nicht enthalten**:

* WYSIWYG Editor + Mediathek 2.4.2
* Klarna 5.5.3
* Makaira 1.4.5
* GDPR Opt-In 2.3.3
* PayPal 6.5.0
* Cookie Management powered by Usercentrics 1.2.1
* PAYONE 1.9.0

Bestandteile der Core Edition (PE)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Enthält alles aus der CE Core Edition, zusätzlich:

* OXID eShop PE 6.5.3
* OXID eShop Demodata PE 6.0.5

Nicht enthalten (zusätzlich zu den CE-Modulen oben):

* Visual CMS 3.7.0

Bestandteile der Core Edition (EE)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Enthält alles aus der PE Core Edition, zusätzlich:

* OXID eShop EE 6.8.1
* OXID eShop Demodata EE 6.0.5

Nicht enthalten (zusätzlich zu den CE- und PE-Modulen
oben):

* Unzer Payment for OXID 1.2.1 und dessen Abhängigkeiten

Migration
---------

Um einen bestehenden 6.5.5-Shop zur Core Edition zu
migrieren, folgen Sie den Anweisungen in der
:doc:`Core Edition Migrationsanleitung
<../../installation/core-edition>`.
