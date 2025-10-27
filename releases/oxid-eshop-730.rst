OXID eShop Compilation 7.3.0
============================

Veröffentlichungsdatum: 17.08.2025

Neuheiten
---------

PHP Support
^^^^^^^^^^^

Support für PHP 8.2, 8.3 und 8.4.

.. hint::
  Vorsicht beim Rundungsverhalten in PHP 8.4, welches in unterschiedlichen Ergebnissen im Vergleich zu PHP 8.2 und 8.3 enden kann.
  
Für weitere Informationen, siehe `Server- und Systemvoraussetzungen <https://docs.oxid-esales.com/eshop/de/7.3/installation/neu-installation/server-und-systemvoraussetzungen.html#php>`_.

Controller Management
^^^^^^^^^^^^^^^^^^^^^

Für einfachere Verwaltung, bessere Testmöglichkeit und mehr Flexibilität können OXID Controller nun als Service registriert werden.

Für weitere Informationen, siehe `Controller as a Service <https://docs.oxid-esales.com/developer/en/7.3/development/tell_me_about/controller_as_service.html>`_ in der Entwicklerdokumentation.

Umgebungsvariablen
^^^^^^^^^^^^^^^^^^

Nutzen Sie eine `.env`-Datei, um Umgebungsvariablen zu definieren und diese sicher in die eigene OXID eShop Applikation zu integrieren. Das macht es einfacher sensible Konfigurationswerte und umgebungsspezifische Einstellungen zu verwalten.

Für weitere Informationen, siehe `Environment Variables <https://docs.oxid-esales.com/developer/en/7.3/development/modules_components_themes/project/environment.html>`_ in der Entwicklerdokumentation.

Optimierungen & Fehlerbehebungen
--------------------------------

* #0005922 Einfluss der Reihenfolge der Währungsliste auf die Bestellsumme: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=5922>`_
* #0006860 E-Mail Existenzprüfung beim Wechsel von Gast zu registriertem Nutzer: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=6860>`_
* #0007254 Verhalten der Bestellbestätigung, wenn etwas zum Warenkorb hinzugefügt wird: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7254>`_
* #0007391 Exception-Handling, wenn ein Produkt gelöscht wird, welches sich im Warenkorb befindet: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7391>`_
* #0007682 Lieferkostenberechnung nach Einloggen im Warenkorb oder Bestellprozess: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7682>`_
* #0007683 Hinzufügen einer fünften Sprache: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7683>`_
* #0007803 Nutzung der SSL-Konfiguration beim Auslesen der Shop-ID aus der Sprach-URL: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7803>`_
* #0007804 Cache-Performance von Moduldateien unter hoher Last: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7804>`_

Packages
--------

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop CE Compilation beinhaltet die folgenden Pakete:

* APEX Theme von v2.0.0 auf v2.1.0: `Changelog <https://github.com/OXID-eSales/apex-theme/blob/v2.1.0/CHANGELOG-2.x.md>`_
* Eye-Able Assist v3.0.3: `Changelog <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/blob/v3.0.3/CHANGELOG.md>`_
* GDPR Opt-In Module von v4.1.0 auf v4.2.0: `Changelog <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.2.0/CHANGELOG.md>`_
* Makaira Connect Essential 2.1.3: `Changelog <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.3/CHANGELOG.md>`_
* Media Library Module von v2.1.1 auf v3.0.0: `Changelog <https://github.com/OXID-eSales/media-library-module/blob/v3.0.0/CHANGELOG.md>`_
* OXID Cookie Management powered by Usercentrics von v3.0.0 auf v3.1.0: `Changelog <https://github.com/OXID-eSales/usercentrics/blob/v3.1.0/CHANGELOG.md>`_
* OXID eShop CE von v7.2.0 auf v7.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.3.0/CHANGELOG-7.3.md>`_
* OXID eShop Composer Plugin von v7.2.0 auf v7.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.3.0/CHANGELOG-7.x.md>`_
* OXID eShop Demodata CE v8.0.2: `Changelog <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.2/CHANGELOG.md>`_
* OXID eShop Demodata Installer v3.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_
* OXID eShop Doctrine Migration Wrapper von v5.3.0 auf v5.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.4.0/CHANGELOG-5.x.md>`_
* OXID eShop Facts von v4.2.0 auf v4.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.3.0/CHANGELOG-4.x.md>`_
* OXID eShop Unified Namespace Generator von v5.1.0 auf v5.2.0: `Changelog <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.2.0/CHANGELOG.md>`_
* OXID eShop Views Generator v2.2.0: `Changelog <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* Twig Admin Theme von v2.5.0 auf v2.6.1: `Changelog <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.6.1/CHANGELOG-2.x.md>`_
* Twig Component von v2.5.0 auf v2.6.0: `Changelog <https://github.com/OXID-eSales/twig-component/blob/v2.6.0/CHANGELOG-2.x.md>`_
* WYSIWYG Editor Module von v4.2.0 auf v5.0.0: `Changelog <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v5.0.0/CHANGELOG.md>`_

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop PE Compilation beinhaltet zusätzlich die folgenden Pakete:

* OXID eShop Demodata PE v8.0.2
* OXID eShop PE von v7.2.0 auf v7.3.0
* Twig Component PE v2.5.0
* Visual CMS Module von v7.0.3 auf v8.0.1

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop EE Compilation beinhaltet zusätzlich die folgenden Pakete:

* OXID eShop Demodata EE von v8.0.3 auf v8.1.0
* OXID eShop EE von v7.2.0 auf v7.3.0
* Twig Component EE v2.5.0

OXID eShop EE B2B Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop EE B2B Compilation beinhaltet zusätzlich die folgenden Pakete:

* OXID eShop B2B Approval Procedure Module von v7.2.0 auf v7.3.0
* OXID eShop B2B Basket Module von v7.2.0 auf v7.3.0
* OXID eShop B2B Budget Module von v7.2.0 auf v7.3.0
* OXID eShop B2B Bulk Orders Module von v7.2.0 auf v7.3.0
* OXID eShop B2B Buying Agent Module von v7.2.0 auf v7.3.0
* OXID eShop B2B Custom Prices Module von v7.2.0 auf v7.3.0
* OXID eShop B2B Offers Module von v7.2.0 auf v7.3.0
* OXID eShop B2B Quick Orders Module von v7.2.0 auf v7.3.0
* OXID eShop B2B Scheduled Orders Module von v7.2.0 auf v7.3.0
* OXID eShop B2B Service Products Module von v7.2.0 auf v7.3.0
* OXID eShop B2B Services Module von v7.2.0 auf v7.3.0

Für weitere Informationen zu Veröffentlichungen der B2B Edition, siehe die (passwortgeschützte) `OXID eShop Enterprise B2B Edition <https://docs.oxid-esales.com/b2b/de/7.3/releases/b2b-edition-730.html>`_ Dokumentation.

Kompatible OXID Erweiterungen
-----------------------------

* OXAPI GraphQL Base Modul 11.0: `Dokumentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/11.0/>`_
* OXAPI GraphQL Configuration Access Modul 2.1: `Dokumentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/11.0/>`_
* OXAPI GraphQL Storefront Modul 4.1: `Dokumentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/11.0/>`_
* OXID ERP Schnittstelle 4.2: `Dokumentation [en] (passwortgeschützt) <https://docs.oxid-esales.com/interfaces/erp/en/4.2>`_
* [NEW] OXID eShop Admin Tools 1.0: `Dokumentation <https://docs.oxid-esales.com/modules/admin-tools/de/1.0/>`_
* [NEW] OXID eShop Consistency Check Tool 1.0: `Dokumentation [en] (GitHub) <https://github.com/OXID-eSales/consistency-check-tool/blob/v1.0.0/README.md>`_
* OXID eShop Country VAT Administration 2.3: `Dokumentation [en] (GitHub) <https://github.com/OXID-eSales/country-vat-module/blob/v2.3.0/README.md>`_
* OXID eShop Geo-Blocking Modul 2.3: `Dokumentation <https://docs.oxid-esales.com/modules/geo-blocking/de/2.3>`_
* [NEW] OXID eShop Security Modul 2.0: `Dokumentation <https://docs.oxid-esales.com/modules/security/de/2.0/>`_
* OXID eShop Shipping Cost Compensation Modul 1.1: `Dokumentation <https://docs.oxid-esales.com/modules/freeshipping-coupons/de/1.1/>`_
* OXID eShop eVAT Modul 4.2: `Dokumentation <https://docs.oxid-esales.com/modules/vat-tbe-services/de/4.2>`_

Installation
------------

Zum Installieren oder Aktualisieren folgen Sie der Anleitung unter :doc:`Installation <../../installation/index>`.
