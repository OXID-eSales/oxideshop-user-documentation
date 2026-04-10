OXID eShop Compilation 7.5.0
============================

Veröffentlichungsdatum: TBD

Neuheiten
---------

Content & Medien Bundle 10
^^^^^^^^^^^^^^^^^^^^^^^^^^

OXID eShop 7.5 bringt das neue **Content & Medien Bundle 10**
mit sich. Dieses enthält folgende Erweiterungen:

* Mediathek 5
* WYSIWYG-Editor 7
* Visual CMS 10 (nur Enterprise und Professional Edition)

Visual CMS 10 ist die konsequente Weiterentwicklung der mit
Visual CMS 9 eingeführten Architektur. Die wichtigsten
Neuerungen:

**Visual CMS 10** (nur Professional und Enterprise Edition):

* **"Anything-First"-Bearbeitung:** Wählen Sie ein beliebiges
  Gerät als Ausgangspunkt für das Design. Passen Sie die
  Widget-Größen explizit für jedes Gerät an — volle
  Kontrolle über alle Breakpoints.
* **Gerätetypabhängige Widget-Größen:** Separate
  Konfiguration für Smartphone, Tablet (Hoch-/Querformat),
  Desktop und große Bildschirme.
* **Gerätetyp-Umschalter** im Editor zum schnellen Wechsel
  zwischen Viewports.
* **Verschachtelte Aktivitätsgruppen:** UND/ODER-Logik für
  komplexe zeitbasierte Sichtbarkeitsregeln von Widgets,
  einschließlich Ausschlusszeiträumen.
* **Lokalisierte Datums-/Zeitanzeige** in den
  Aktivitätseinstellungen, 12h/24h-Unterstützung.
* **TypeScript:** JavaScript-Dateien auf TypeScript migriert.
* **Bootstrap Icons** ersetzen Font Awesome im Admin-Bereich.

**WYSIWYG-Editor 7:**

* **Erweiterbar durch Module:** Neue Twig-Blöcke
  ``ddoe_wysiwyg_plugins`` und
  ``ddoe_wysiwyg_summernote_options`` erlauben es Modulen,
  den Editor mit eigenen Plugins und Optionen zu erweitern.
* **Alt-Text-Migration:** Neuer Befehl
  ``ddoewysiwyg:migrate:alt-texts`` ersetzt fehlende oder
  leere Alt-Attribute auf Medienbildern.
* **Bootstrap Icons** ersetzen Font Awesome.

**Mediathek 5:**

* **Suche nach Medien-ID:** Das Suchfeld findet Medien
  nun auch anhand der Medien-ID, nicht nur anhand des
  Dateinamens.
* **QueryBuilder:** Repository-Schicht auf QueryBuilder
  umgestellt.
* **Bootstrap Icons** ersetzen Font Awesome.

Wenn Sie die Vorgängerversionen beibehalten möchten, können
Sie Ihr Update vorkonfigurieren. Weitere Informationen
finden Sie in unserer
:doc:`Update-Anleitung <../installation/update>`.

PHP 8.5 Unterstützung
^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop 7.5 Compilation und alle unten aufgeführten
Erweiterungen wurden mit **PHP 8.3, 8.4 und 8.5** getestet.
Die Mindestversion ist PHP 8.3. PHP 8.2 wird nicht mehr
unterstützt.

API-Entrypoint
^^^^^^^^^^^^^^

Eine neue API-Schicht (``api.php``) auf Basis des Symfony
HttpKernel ermöglicht es, beliebige Shop-Funktionen als
API-Endpunkte bereitzustellen. Das Routing erfolgt über
PHP 8 ``#[Route]``-Attribute. Die API ist JSON-basiert und
zustandslos. Vier Authentifizierungsmodelle stehen zur
Verfügung: öffentlich, JWT-Token, Frontend-Session und
Admin-Session.

Zusammen mit OXAPI (GraphQL) bietet der Shop damit zwei
komplementäre Schnittstellen: OXAPI für das umfangreiche
Produkt- und Commerce-Datenmodell und benutzerdefinierte
API-Endpunkte für individuelle Anforderungen.

Neuer Such-Service
^^^^^^^^^^^^^^^^^^

OXID eShop 7.5 bietet eine neue, austauschbare Sucharchitektur.
Das neue ``ProductSearchServiceInterface`` ermöglicht es, die
eingebaute SQL-Suche durch externe Suchmaschinen wie
Meilisearch oder Elasticsearch zu ersetzen. Bei
einem Ausfall der externen Suche greift der Shop automatisch
auf die SQL-Suche zurück.

Weitere Informationen finden Sie in der
`Entwicklerdokumentation <https://docs.oxid-esales.com/developer/en/7.5/>`_.

Neuer E-Mail-Service
^^^^^^^^^^^^^^^^^^^^

OXID eShop 7.5 enthält einen neuen E-Mail-Service, der auf
dem Symfony Mailer basiert. Der Service bietet saubere
Schnittstellen und eine erweiterbare Architektur, die
moderne E-Mail-Transporte (API-basierte Anbieter,
OAuth2-Authentifizierung, warteschlangenbasierter Versand)
ermöglicht. In der 7.x-Serie läuft der neue Service
alternativ zum bestehenden System.

HTML-Sanitizer
^^^^^^^^^^^^^^

Ein neuer, auf dem Symfony HtmlSanitizer basierender
Sicherheitsfilter bereinigt HTML-Inhalte automatisch, bevor
sie im Shop angezeigt werden. Der neue Twig-Filter
``sanitize_html`` entfernt potenziell gefährliche
HTML-Elemente wie Script-Tags, Event-Handler und unsichere
Iframes. Die erlaubten HTML-Elemente und -Attribute sind
konfigurierbar. Module können die Konfiguration bei Bedarf
anpassen.

Sicherheitsverbesserungen
^^^^^^^^^^^^^^^^^^^^^^^^^

Mehrere Verbesserungen stärken die Sicherheit des Shops:

* **Sensible GET-Parameter entfernt:** Zustandsändernde
  Operationen (z. B. Artikel auf die Merkliste setzen,
  Gutschein entfernen) wurden von GET-Links mit
  Session-Tokens in der URL auf POST-Formulare mit
  versteckten Feldern umgestellt. Session-IDs und
  CSRF-Tokens sind nicht mehr in URLs sichtbar.
* **Bootstrap-3-Bereinigung:** Verbliebene Bootstrap-3-
  CSS-Klassen im APEX Theme wurden entfernt. Templates
  verwenden nun ausschließlich Bootstrap-5-Klassen.
* **HTML-Sanitizer:** Siehe oben.

Performance-Verbesserungen
^^^^^^^^^^^^^^^^^^^^^^^^^^

Mehrere gezielte Optimierungen verbessern die Ladezeiten:

* Leere Warenkörbe werden frühzeitig erkannt — keine
  unnötigen Berechnungen mehr bei jedem Seitenaufruf.
* Deaktivierte Module beeinflussen die Renderzeit der
  Storefront nicht mehr.
* Unnötige Instanziierungen der Warenkorb-Komponente
  wurden eliminiert.

.. _fixes:

Optimierungen & Fehlerbehebungen
--------------------------------

* #0007881 Model extension chain bypass: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7881>`_
* #0007877 composer/composer fälschlicherweise in require statt require-dev: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7877>`_
* #0007907 Hilfetext für Rabattmengen verdeutlicht: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7907>`_
* #0007178 Kategorie-Dropdown wird für Kategorien ohne sichtbare Unterkategorien nicht mehr angezeigt: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7178>`_
* #0007921 Template-Erweiterungen für Modul-Templates rendern korrekt: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7921>`_

* Menü-Zähler für herstellerspezifische Menübereiche korrigiert: `PR-10 <https://github.com/OXID-eSales/twig-admin-theme/pull/10>`_
* Falsche Produktbild-Anzahl 13 statt 12 korrigiert: `PR-14 <https://github.com/OXID-eSales/twig-admin-theme/pull/14>`_

* #0007922 Produktgalerie und Grid-Bilder respektieren nun die Einstellung blConvertImagesToWebP, Hover-Bild auf mobilen Viewports nicht mehr defekt: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7922>`_

.. _packages:

Packages
--------

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop CE Compilation enthält die folgenden Pakete:

* APEX Theme von v3.0.2 auf v3.1.0: `Changelog <https://github.com/OXID-eSales/apex-theme/blob/v3.1.0/CHANGELOG-3.x.md>`_
* Eye-Able Assist v3.0.3
* GDPR Opt-In Module von v4.3.0 auf v4.4.0: `Changelog <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.4.0/CHANGELOG.md>`_
* Makaira Connect Essential von 2.1.4 auf 2.2.0: `Changelog <https://github.com/MakairaIO/oxid-connect-essential/blob/2.2.0/CHANGELOG.md>`_
* Media Library Module von v4.1.0 auf v5.0.0 (oder v4.1.0 oder v3.0.0 bleibend): `Changelog <https://github.com/OXID-eSales/media-library-module/blob/v5.0.0/CHANGELOG.md>`_
* OXID Cookie Management powered by Usercentrics von v3.2.1 auf v3.3.0: `Changelog <https://github.com/OXID-eSales/usercentrics/blob/v3.3.0/CHANGELOG.md>`_
* OXID eShop CE von v7.4.0 auf v7.5.0: `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.5.0/CHANGELOG-7.5.md>`_
* OXID eShop Composer Plugin von v7.3.0 auf v7.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.4.0/CHANGELOG-7.x.md>`_
* OXID eShop Demodata CE v8.1.0
* OXID eShop Demodata Installer v3.3.0
* OXID eShop Doctrine Migration Wrapper von v5.4.0 auf v5.5.0: `Changelog <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.5.0/CHANGELOG-5.x.md>`_
* OXID eShop Facts von v4.3.0 auf v4.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.4.0/CHANGELOG-4.x.md>`_
* OXID eShop Unified Namespace Generator von v5.2.0 auf v5.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.3.0/CHANGELOG.md>`_
* OXID eShop Views Generator v2.2.0
* Twig Admin Theme von v3.0.1 auf v3.1.0: `Changelog <https://github.com/OXID-eSales/twig-admin-theme/blob/v3.1.0/CHANGELOG-3.x.md>`_
* Twig Component von v2.7.0 auf v2.8.0: `Changelog <https://github.com/OXID-eSales/twig-component/blob/v2.8.0/CHANGELOG-2.x.md>`_
* WYSIWYG Editor Module von v6.0.2 auf v7.0.0 (oder v6.0.2 oder v5.0.1 bleibend): `Changelog <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v7.0.0/CHANGELOG.md>`_

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop PE Compilation enthält zusätzlich die
folgenden Pakete:

* OXID eShop Demodata PE v8.1.0
* OXID eShop PE von v7.4.0 auf v7.5.0
* Twig Component PE von v2.5.0 auf v2.6.0
* Visual CMS Modul von v9.2.0 auf v10.0.0 (oder v9.2.0 oder v8.0.2 bleibend)

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop EE Compilation enthält zusätzlich die
folgenden Pakete:

* OXID eShop Demodata EE v8.2.0
* OXID eShop EE von v7.4.0 auf v7.5.0
* Twig Component EE von v2.5.0 auf v2.6.0

OXID eShop EE B2B Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop EE B2B Compilation enthält zusätzlich die
folgenden Pakete:

* OXID eShop B2B Approval Procedure Modul von v7.4.0 auf v7.5.0
* OXID eShop B2B Basket Modul von v7.4.0 auf v7.5.0
* OXID eShop B2B Budget Modul von v7.4.0 auf v7.5.0
* OXID eShop B2B Bulk Orders Modul von v7.4.0 auf v7.5.0
* OXID eShop B2B Buying Agent Modul von v7.4.0 auf v7.5.0
* OXID eShop B2B Custom Prices Modul von v7.4.0 auf v7.5.0
* OXID eShop B2B Offers Modul von v7.4.0 auf v7.5.0
* OXID eShop B2B Quick Orders Modul von v7.4.0 auf v7.5.0
* OXID eShop B2B Scheduled Orders Modul von v7.4.0 auf v7.5.0
* OXID eShop B2B Service Products Modul von v7.4.0 auf v7.5.0
* OXID eShop B2B Services Modul von v7.4.0 auf v7.5.0

Für weitere Informationen zu Veröffentlichungen der
B2B Edition, siehe die (passwortgeschützte)
`OXID eShop Enterprise B2B Edition
<https://docs.oxid-esales.com/b2b/de/7.5/releases/b2b-edition-750.html>`_
Dokumentation.

Kompatible OXID Erweiterungen
-----------------------------

* OXAPI GraphQL Base Modul: `Dokumentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/7.5/>`_
* OXAPI GraphQL Configuration Access Modul: `Dokumentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/7.5/>`_
* OXAPI GraphQL Storefront Modul: `Dokumentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/7.5/>`_
* OXAPI GraphQL Storefront Administration Modul: `Dokumentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/7.5/>`_
* OXID ERP Schnittstelle 4.4: `Dokumentation [en] (passwortgeschützt) <https://docs.oxid-esales.com/interfaces/erp/en/4.4>`_
* OXID eShop Admin Tools 1.2: `Dokumentation <https://docs.oxid-esales.com/modules/admin-tools/de/1.2/>`_
* OXID eShop Country VAT Administration 2.5: `Dokumentation [en] (GitHub) <https://github.com/OXID-eSales/country-vat-module/blob/v2.5.0/README.md>`_
* OXID eShop Geo-Blocking Modul 2.5: `Dokumentation <https://docs.oxid-esales.com/modules/geo-blocking/de/2.5>`_
* OXID eShop Shipping Cost Compensation Modul 1.3: `Dokumentation <https://docs.oxid-esales.com/modules/freeshipping-coupons/de/1.3/>`_
* OXID eShop eVAT Modul 4.4: `Dokumentation <https://docs.oxid-esales.com/modules/vat-tbe-services/de/4.4>`_
* OXID Cookie Management powered by Usercentrics 3.3: `Dokumentation <https://docs.oxid-esales.com/modules/usercentrics/de/3.3/>`_
* GDPR Opt-In Module 4.4: `Dokumentation <https://docs.oxid-esales.com/modules/gdpr-optin/de/4.4/>`_
* OXID Security Modul: `Dokumentation <https://docs.oxid-esales.com/modules/security/de/latest/>`_
* OXID eShop Consistency Check Component: `Dokumentation [en] (GitHub) <https://github.com/OXID-eSales/consistency-check-tool>`_
* OXID Modul Template: `Dokumentation (GitHub) <https://github.com/OXID-eSales/module-template>`_
* OXID Examples Modul: `Dokumentation (GitHub) <https://github.com/OXID-eSales/examples-module>`_

.. todo:: Versionsnummern nachziehen: GraphQL-Module,
   Security Modul, Consistency Check, Modul Template,
   Examples Modul — sobald die Module released sind

Update
------

Der Update-Vorgang wird Schritt für Schritt in unserer
:doc:`Update-Anleitung <../installation/update>` beschrieben.

Installation
------------

Wenn Sie OXID eShop 7.5 neu installieren möchten, folgen
Sie bitte unserer
:doc:`Installationsanleitung <../installation/neu-installation/index>`.
