OXID eShop Compilation 7.6.0
============================

Veröffentlichungsdatum: TBD

.. todo: release date

.. note::

   OXID eShop 7.6 unterstützt weiterhin **PHP 8.3, 8.4 und 8.5** (Mindestversion PHP 8.3); der
   PHP-Versionsstand bleibt gegenüber 7.5 unverändert.

Neuheiten
---------

Content & Medien Bundle 12
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Mit OXID eShop 7.6 ist das neue **Content & Medien Bundle 12** vorinstalliert. Es besteht
aus folgenden Komponenten:

* **Mediathek 6**
* **WYSIWYG-Editor 8**
* **Visual CMS 12** (ausschließlich Enterprise und Professional Edition)

Highlights:

* **Visual CMS 12 — dynamische Blöcke (zentrale Neuerung):** Mit den dynamischen Blöcken
  lassen sich CMS-Inhalte an fest definierten Positionen im Theme („Blöcken") einblenden.
  Welcher Inhalt an einem Block erscheint, weisen Sie im Admin-Bereich zu — ohne das
  Template zu bearbeiten; bestimmend ist der **Kontext** der Zuordnung: global oder gebunden
  an einen bestimmten Artikel, eine Kategorie oder einen Hersteller; spezifische Zuordnungen
  haben dabei Vorrang vor allgemeinen. Innerhalb des Blocks greifen die gewohnten
  Sichtbarkeits-Steuerungen des Visual CMS unverändert weiter — **zeitgesteuert** (Datum und
  Uhrzeit, je Zeile/Widget) und **gerätespezifisch** (Sichtbarkeit je Bildschirmgröße, je
  Widget).

  So erscheint ein Aktions-Banner zum Beispiel gezielt nur auf einer bestimmten
  Kategorieseite, und einzelne Elemente darin nur in einem Aktionszeitraum oder nur auf
  bestimmten Geräten. Vier Blöcke (vor und nach dem Kopf- bzw. Fußbereich) sind
  vorkonfiguriert; weitere Blöcke lassen sich einrichten. Die Funktion ist ab Werk
  deaktiviert und wird in den Moduleinstellungen aktiviert. Ausführliche Anleitung und
  Beispiele finden Sie in der Visual-CMS-Dokumentation.
* **Visual CMS 12 — individuelle Styles jetzt als SCSS:** eigene Styles in CMS-Inhalten
  werden ab Visual CMS 12 als **SCSS** statt LESS interpretiert. Bestehende Inhalte können
  Sie vorab mit ``./vendor/bin/oe-console ddoevisualcms:migrate:less-to-scss --dry-run`` prüfen.
* **Mediathek 6 — fehlerfreie Inhalte ab Werk:** Ein mitgeliefertes Fallback-Bild wird
  automatisch gesetzt, sodass Seiten auch bei fehlenden oder gelöschten Medien sauber
  rendern — ohne eigene Einrichtung. Das Fallback-Medium ist gegen versehentliches Löschen
  geschützt; fehlende Medien lassen sich über Diagnose-Meldungen schneller auffinden.
* **WYSIWYG-Editor 8 — stabilere CMS-Links & Medien-URLs:** CMS-Ident-Links werden korrekt
  aufgelöst (kein 404), Twig-Ausdrücke im Filter bleiben erhalten, Medien-URLs werden
  als ``oeMediaUrl`` statt hartkodiert gespeichert.

.. note::

   Beim Update wählen Sie eine der drei angebotenen Bundle-Versionen (12, 11 oder 8); das
   lässt sich wie in der :doc:`Update-Anleitung <../installation/update>` beschrieben
   vorkonfigurieren. Ältere Linien (z. B. Visual CMS 9.x/10.x, Mediathek 4.x, WYSIWYG 6.x)
   werden nicht weitergeführt — Bestandsinstallationen wechseln auf eine der angebotenen
   Versionen.

.. note::

   **Hinweis für Erweiterungen:** Mediathek 6 ist ein Major-Release. Die Methoden
   ``MediaFacadeInterface::getMedia()`` und ``getMediaUrl()`` haben einen zusätzlichen
   optionalen Parameter erhalten — aufrufender Code bleibt kompatibel; Module, die dieses
   Interface implementieren oder dekorieren, müssen angepasst werden.

Konfigurierbarer Rate Limiter fürs Storefront
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Neu in 7.6 (in CE v7.6.0 enthalten): ein optionaler Storefront-Request-Rate-Limiter,
standardmäßig deaktiviert. Er begrenzt regelbasiert die Aufruf-Häufigkeit von
Storefront-Aktionen — von einer groben, globalen Begrenzung (bremst einzelne, zu häufig
aufrufende Clients) bis zu gezielten Regeln für sensible Aktionen wie den Login. Antwortet
mit ``429`` + ``Retry-After`` / ``X-RateLimit-*``; Erweiterungs-Hook ``RateLimitExceededEvent``;
Konsolen-Befehl ``oe:rate-limiter:prune`` (Cron). Er ist ein eigenständiger Limiter zusätzlich
zum bereits seit 7.5 verfügbaren API-Rate-Limiter; beide arbeiten unabhängig voneinander.

Sicherheits-Baseline
^^^^^^^^^^^^^^^^^^^^

Mehrere Verbesserungen härten den Shop über die gesamte Compilation hinweg:

* **Stärkeres Passwort-Hashing:** Der Standard-bcrypt-Cost wurde angehoben
  (`#0007727 <https://bugs.oxid-esales.com/view.php?id=7727>`_).
* **Vertrauenswürdige Proxies:** Die Remote-Adress-Auflösung nutzt jetzt Symfonys
  ``Request::getClientIp()``. Proxy-Header werden standardmäßig **nicht** mehr
  vertraut; vertrauenswürdige IPs werden über den DI-Parameter
  ``oxid_esales.request.trusted_proxies`` konfiguriert.
* **HTTPS hinter SSL-Offloadern** wird über Forwarded-Header vertrauenswürdiger
  Proxies erkannt.
* **APEX — externe Produkt-URL abgesichert:** externe URLs werden escaped und das
  Schema geprüft (XSS-/Scheme-Injection-Härtung).
* **DSGVO-konforme Löschung:** Beim Löschen eines Benutzers per ID werden jetzt alle
  zugehörigen Datensätze per Cascade entfernt
  (`#0007138 <https://bugs.oxid-esales.com/view.php?id=7138>`_).

Modernes Fundament — Migrationen, Modul-Lifecycle, Console
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die technische Basis wird in einem planbaren Rahmen weiter modernisiert — alte
Methoden bleiben nutzbar, der neue Weg ist aufgezeigt:

* **Datenbank-Migrationen über DI registrierbar:** Doctrine-Migrationen lassen sich
  über das DI-Tag ``oxid_esales.migration_path_provider``
  (``MigrationPathProviderInterface``) bereitstellen. Das kommt Components zugute und
  ist auch für Module der zukünftig bevorzugte Weg.
* **Neuer Konsolen-Befehl** ``oe:database:migrate`` zum Ausführen der Migrationen.
* **Services vor Aktivierung:** Module können über eine optionale
  ``bootstrap-services.yaml`` ausgewählte Services bereitstellen — geladen für jedes
  installierte Modul, unabhängig vom Aktivierungszustand.
* **Saubere Console-Rückgabewerte:** Konsolen-Befehle liefern konsistente Exit-Codes
  (0 = Erfolg, 1 = Fehler) — CI-/Automatisierungs-tauglich.

.. note::

   **Hinweis für Theme- und Modul-Entwickler:** Der Vite-basierte Asset-Build wurde
   aktualisiert (Vite-Versionssprung, Sass 1.80). Dadurch steigt die für den
   **Asset-Build** benötigte Node-Version: **APEX-Theme** Node 20.19+, die Module des
   Content & Medien Bundles — **Mediathek**, **WYSIWYG-Editor** und **Visual CMS** —
   Node 22.12+ bzw. 22.13+. Dies betrifft ausschließlich den Asset-Build; der
   Shop-Betrieb selbst ändert sich dadurch nicht.

Fortgeführte Modernisierung (Deprecations)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Im Zuge der Modernisierung sind einige Wege als veraltet markiert; die bisherigen
Methoden bleiben nutzbar, der neue Weg ist jeweils benannt. Auszug:

* Modul-``metadata.php``-Events (``onActivate`` / ``onDeactivate``) → DI-Event-Subscriber.
* ``oxid-esales/oxideshop-doctrine-migration-wrapper`` / ``oe-eshop-db_migrate`` →
  ``oe:database:migrate``.
* BC-Autoloader für Legacy-Klassennamen (z. B. ``oxarticle``, ``oxorder``) — ebenso die
  Generierung der zugehörigen BC-Klassen-Aliase im Unified-Namespace-Generator.
* ``Argon2IPasswordHashService``; ``UtilsServer::getRemoteAddress()`` /
  ``ViewConfig::getRemoteAddress()``.

Die vollständige Deprecation-Liste finden Sie im
`CE-Changelog 7.6 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.6.0/CHANGELOG-7.6.md>`_.

.. _fixes-760:

Optimierungen & Fehlerbehebungen
--------------------------------

* #0006025 Groß-/Kleinschreibung von Spaltennamen in der Admin-Bestell-Artikelsuche: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=6025>`_
* #0007073 Bereits zugeordnete Produkte erscheinen nicht mehr unter „All available Products" im Kategorie-Zuordnungs-Popup: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7073>`_
* #0007770 Endlos-Redirect und falsche URL-Generierung behoben: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7770>`_
* Admin-Login erzeugt keine PHP-Warnung mehr, wenn die Anfrage keinen ``Accept-Language``-Header hat: `PR-999 <https://github.com/OXID-eSales/oxideshop_ce/pull/999>`_
* Adress-Auswahl-Validierung in Konto und Checkout korrigiert.

* APEX #0007703 Produktdetail-Tabs rendern wieder Inhalt: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7703>`_
* APEX #0007880 Preisberechnung in Bestellübersichts-E-Mails korrigiert: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7880>`_
* APEX #0007866 fehlendes ``oxwactions``-Template ergänzt: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7866>`_
* APEX Bestellhistorie „Shipped"-Status korrigiert: `PR-72 <https://github.com/OXID-eSales/apex-theme/pull/72>`_
* APEX #0008006 Empfehlungslisten-Seite (``cl=recommlist``) rendert wieder (übrig gebliebene Smarty-``->``-Syntax entfernt); Heading-Titel, Autor und Suchbegriff werden escaped: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=8006>`_
* APEX Review-Seite (``cl=review``) rendert bei aktivierten Reviews wieder (Produkt-Rating im Reviews-Widget auf Nicht-Produktseiten übersprungen).

* Twig-Admin #0007837 Feld-Controls bei ungespeicherten/vererbten Selektionslisten: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7837>`_
* Twig-Admin #0007953 Kategorie als Haupt-Kategorie am Produkt setzen: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7953>`_
* Twig-Admin: In den AJAX-Zuweisungslisten im Admin (z. B. Artikel, Gruppen oder Zubehör zuordnen) lässt sich die Darstellung einer Spalte jetzt über einen eigenen Formatter anpassen.

* WYSIWYG-Editor: CMS-Ident-Links/Twig-Filter korrigiert, Medien-URLs als ``oeMediaUrl``, Image-URL-Cache cross-frame, führendes ``<style>``-Tag bleibt bei der DOMPurify-Sanitierung erhalten.
* WYSIWYG-Editor: Der Migrationsbefehl ``ddoewysiwyg:migrate:urls-to-ids`` konvertiert Medien-Referenzen nun in allen ``img src``- und ``a href``-Attributen (statt nur in markierten Bildern), meldet jede konvertierte und jede nicht auflösbare Referenz und kann den Bericht per ``--report-file`` als CSV ausgeben.
* Mediathek: angefragte Medien-ID bleibt in der Ausnahme ohne Fallback, Medien-URL-Cache Frame-Sharing; hochgeladene Objekte zeigen den gespeicherten Dateinamen; neu angelegte Ordner erscheinen oben.

* GDPR Opt-In: exportierte Dateien erhalten eine Dateiendung.
* Demodata CE: korrekte SEO-Identifier für „Passwort vergessen"-Seiten.

.. _packages-760:

Packages
--------

.. note:: Die 7.6-Compilation besteht aus **CE, PE und EE** (B2B ist **nicht** Teil der
   initialen 7.6-Compilation).

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

**Mit funktionaler 7.6-Änderung:**

* OXID eShop CE **v7.5.1 → v7.6.0**: `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.6.0/CHANGELOG-7.6.md>`_
* APEX Theme **v3.1.0 → v3.2.0**: `Changelog <https://github.com/OXID-eSales/apex-theme/blob/v3.2.0/CHANGELOG-3.x.md>`_
* WYSIWYG Editor Module **v7.0.1 → v8.0.1** (Content & Medien Bundle 12; alternativ v7.1.1 für Bundle 11 oder v5.0.1 für Bundle 8): `Changelog <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v8.0.1/CHANGELOG.md>`_
* Media Library Module **v5.1.0 → v6.0.0** (Content & Medien Bundle 12; alternativ v5.2.0 für Bundle 11 oder v3.0.0 für Bundle 8): `Changelog <https://github.com/OXID-eSales/media-library-module/blob/v6.0.0/CHANGELOG.md>`_
* GDPR Opt-In Module **v4.4.0 → v4.5.0**: `Changelog <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.5.0/CHANGELOG.md>`_
* Twig Admin Theme **v3.1.0 → v3.2.0**: `Changelog <https://github.com/OXID-eSales/twig-admin-theme/blob/v3.2.0/CHANGELOG-3.x.md>`_
* Unified Namespace Generator **v5.3.1 → v5.4.0**: `Changelog <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.4.0/CHANGELOG.md>`_
* OXID Cookie Management powered by Usercentrics **v3.3.0 → v3.4.0** *(nur 7.6-Kompatibilität)*: `Changelog <https://github.com/OXID-eSales/usercentrics/blob/v3.4.0/CHANGELOG.md>`_
* Demodata CE **v8.1.0 → v8.1.1**: `Changelog <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.1.1/CHANGELOG.md>`_
* Doctrine Migration Wrapper **v5.5.0 → v6.0.0** *(Paket ist deprecated — ersetzt durch* ``oe:database:migrate``\ *)*: `Changelog <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v6.0.0/CHANGELOG-6.x.md>`_

**Ohne funktionale 7.6-Änderung** (nur Branch-Initialisierung / Workflow / Test-Anpassungen)
— bleiben auf ihrer 7.5-Version:

* OXID eShop Composer Plugin v7.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.4.0/CHANGELOG-7.x.md>`_
* Twig Component v2.8.1: `Changelog <https://github.com/OXID-eSales/twig-component/blob/v2.8.1/CHANGELOG-2.x.md>`_
* Demodata Installer v3.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_
* DB Views Generator v2.2.0: `Changelog <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* Facts v4.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.4.0/CHANGELOG-4.x.md>`_

**Extern:**

* Eye-Able Assist v3.0.3 (unverändert)
* Makaira Connect Essential **2.2.0 → 2.2.1**

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop PE Compilation enthält zusätzlich die folgenden Pakete:

* OXID eShop PE **v7.5.1 → v7.6.0**
* OXID eShop Demodata PE **v8.1.0 → v8.1.1**
* Twig Component PE v2.6.0 (unverändert)
* Visual CMS Modul **v10.0.1 → v12.0.0** (Content & Medien Bundle 12; alternativ v11.1.0 für Bundle 11 oder v8.0.2 für Bundle 8)

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop EE Compilation enthält zusätzlich die folgenden Pakete:

* OXID eShop EE **v7.5.1 → v7.6.0**
* OXID eShop Demodata EE **v8.2.0 → v8.2.1**
* Twig Component EE **v2.6.0 → v2.7.0**

.. COMMENTED OUT — does NOT render:
   B2B is not part of the initial 7.6 compilation (hence no EE-B2B section).

.. COMMENTED OUT — PROVISIONAL, does NOT render (not even in preview):
   Compatible extensions are released AFTER the compilation; no final 7.6 tags exist yet.
   Versions below are PROSPECTIVE — taken from the "Unreleased" changelog headers on each
   module's b-7.6.x branch (graphql-base → v14.0.0, confirmed by PO). The changelog links
   point at these prospective tags and will 404 until the module is actually tagged.
   When a module is provably released: verify its final version, then uncomment its line
   (adjust version/link if the released tag differs). Raw (German) content below:

   Kompatible OXID Erweiterungen
   -----------------------------

   Die kompatiblen Erweiterungen werden nachgelagert zur Compilation veröffentlicht; die
   folgenden Versionen sind voraussichtlich (final mit dem jeweiligen Modul-Release):

   * OXAPI GraphQL Base Modul **v14.0.0** (voraussichtlich): `Changelog <https://github.com/OXID-eSales/graphql-base-module/blob/v14.0.0/CHANGELOG-v14.md>`_
   * OXAPI GraphQL Configuration Access Modul **v4.1.0** (voraussichtlich): `Changelog <https://github.com/OXID-eSales/graphql-configuration-access/blob/v4.1.0/CHANGELOG.md>`_
   * OXAPI GraphQL Storefront Modul **v5.1.0** (voraussichtlich): `Changelog <https://github.com/OXID-eSales/graphql-storefront-module/blob/v5.1.0/CHANGELOG.md>`_
   * OXAPI GraphQL Storefront Administration Modul **v5.0.0** (voraussichtlich): `Changelog <https://github.com/OXID-eSales/graphql-storefront-administration/blob/v5.0.0/CHANGELOG.md>`_
   * OXAPI GraphQL Orders Information Modul **v2.3.0** (voraussichtlich): `Changelog <https://github.com/OXID-eSales/graphql-orders-information-module/blob/v2.3.0/CHANGELOG.md>`_
   * OXID Security Modul **v4.1.0** (voraussichtlich): `Changelog <https://github.com/OXID-eSales/security-module/blob/v4.1.0/CHANGELOG.md>`_
   * OXID eShop Admin Tools **v2.1.0** (voraussichtlich): `Changelog <https://github.com/OXID-eSales/admin-tools-module/blob/v2.1.0/CHANGELOG.md>`_
   * OXID eShop Country VAT Administration **v2.6.0** (voraussichtlich): `Changelog <https://github.com/OXID-eSales/country-vat-module/blob/v2.6.0/CHANGELOG.md>`_
   * OXID eShop Geo-Blocking Modul **v2.6.0** (voraussichtlich): `Changelog <https://github.com/OXID-eSales/geo-blocking-module/blob/v2.6.0/CHANGELOG.md>`_
   * OXID eShop Shipping Cost Compensation Modul **v1.4.0** (voraussichtlich): `Changelog <https://github.com/OXID-eSales/freeshipping-coupons-module/blob/v1.4.0/CHANGELOG.md>`_
   * OXID eShop eVAT Modul **v4.5.0** (voraussichtlich): `Changelog <https://github.com/OXID-eSales/vat_tbe_services/blob/v4.5.0/CHANGELOG.md>`_
   * OXID eShop Consistency Check Component **v3.1.0** (voraussichtlich): `Changelog <https://github.com/OXID-eSales/consistency-check-tool/blob/v3.1.0/CHANGELOG.md>`_
   * OXID Modul Template **v5.3.0** (voraussichtlich): `Changelog <https://github.com/OXID-eSales/module-template/blob/v5.3.0/CHANGELOG.md>`_
   * OXID Examples Modul **v2.2.0** (voraussichtlich): `Changelog <https://github.com/OXID-eSales/examples-module/blob/v2.2.0/CHANGELOG.md>`_
   * OXID ERP Schnittstelle (extern; Version folgt mit dem Release)

Update
------

Der Update-Vorgang wird Schritt für Schritt in unserer
:doc:`Update-Anleitung <../installation/update>` beschrieben.

Installation
------------

Wenn Sie OXID eShop 7.6 neu installieren möchten, folgen Sie bitte unserer
:doc:`Installationsanleitung <../installation/neu-installation/index>`.
