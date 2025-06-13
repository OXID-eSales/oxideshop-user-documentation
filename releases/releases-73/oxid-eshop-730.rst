OXID eShop Compilation 7.3.0
============================

.. todo: #HR: Veröffentlichungsdatum: tbd

Änderungen
----------

* Nutzen Sie die volle Kompatibilität mit PHP 8.2 bis 8.4.

  Die Software unterstützt PHP-Versionen bis einschließlich PHP 8.4. Beachten Sie jedoch die Änderungen im Rundungsverhalten von Gleitkommazahlen in PHP 8.4, da diese im Vergleich zu PHP 8.3 zu abweichenden Berechnungsergebnissen führen können.

  .. todo: #tbd: URLs prüfen

  Weitere Informationen finden Sie unter `Server- und Systemvoraussetzungen <https://docs.oxid-esales.com/eshop/de/7.3/installation/neu-installation/server-und-systemvoraussetzungen.html>`_ im Abschnitt `PHP <https://docs.oxid-esales.com/eshop/de/7.3/installation/neu-installation/server-und-systemvoraussetzungen.html#php>`_.

* Optimieren Sie die Verwaltung von OXID-Controllern.

  Registrieren Sie OXID-Controller als Services im Dependency Injection Container (DIC), um eine einfachere Handhabung, bessere Testbarkeit und flexiblere Erweiterbarkeit zu ermöglichen.

  .. todo: #tbd: Link prüfen

  Weitere Informationen finden Sie in der Entwicklerdokumentation (Englisch) unter `Controller as a service <https://docs.oxid-esales.com/developer/en/7.3/development/tell_me_about/controller_as_service.html>`_.

* Vereinfachen Sie die Verwaltung von Umgebungsvariablen.

  Verwenden Sie eine `.env`-Datei, um Umgebungsvariablen zu definieren und sicher in Ihre OXID eShop-Anwendung zu integrieren. So lassen sich sensible Konfigurationswerte und umgebungsspezifische Einstellungen einfacher verwalten.

  .. todo: #tbd: Link prüfen

  Weitere Informationen finden Sie in der Entwicklerdokumentation (Englisch) unter `Environment variables <https://docs.oxid-esales.com/developer/en/7.3/development/modules_components_themes/project/environment.html>`_.


Fehlerbehebungen
----------------

* Die Auflösung der Shop-ID berücksichtigt nun SSL-Sprach-URLs.
* Prüfung auf E-Mail-Existenz bei Wechsel von Kunden- zu Gastkonto: `#0006860 <https://bugs.oxid-esales.com/view.php?id=6860>`_
* Korrekte Berechnung der Versandkosten nach Login im Warenkorb und Checkout: `#0007682 <https://bugs.oxid-esales.com/view.php?id=7682>`_
* Fehler beim Hinzufügen einer fünften Sprache im Shop behoben: `#0007683 <https://bugs.oxid-esales.com/view.php?id=7683>`_
* Korrekte Anzeige der Bestellsummen im Admin bei Verwendung einer abweichenden Basiswährung: `#0005922 <https://bugs.oxid-esales.com/view.php?id=5922>`_
* Ausnahmebehandlung, wenn ein Produkt gelöscht wird, während es sich im Warenkorb befindet: `#0007391 <https://bugs.oxid-esales.com/view.php?id=7391>`_
* Verbesserte Moduldaten-Cache-Verwaltung unter hoher Last
* "Zu Warenkorb hinzufügen" erzwingt nun das Neuladen des Bestellbestätigungsschritts: `#0007254 <https://bugs.oxid-esales.com/view.php?id=7254>`_


Komponenten
-----------

Aktualisierte Komponenten
^^^^^^^^^^^^^^^^^^^^^^^^^

Folgende Komponenten und Module wurden aktualisiert:

* WYSIWYG-Editor + Mediathek: v4.2.0 → v5.0.0 `Changelog <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v5.0.0/CHANGELOG.md>`__
* APEX Theme: v2.0.0 → v2.1.0 `Changelog <https://github.com/OXID-eSales/apex-theme/blob/v2.1.0/CHANGELOG-2.x.md>`__
* GDPR Opt-In-Modul: v4.1.0 → v4.2.0 `Changelog <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.2.0/CHANGELOG.md>`__
* Mediathek-Modul: v2.1.1 → v3.0.0 `Changelog <https://github.com/OXID-eSales/media-library-module/blob/v3.0.0/CHANGELOG.md>`__
* OXID eShop CE: v7.2.0 → v7.3.0 `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.3.0/CHANGELOG-7.3.md>`__
* Composer Plugin: v7.2.0 → v7.3.0 `Changelog <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.3.0/CHANGELOG-7.x.md>`__
* Doctrine Migration Integration: v5.3.0 → v5.4.0 `Changelog <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.4.0/CHANGELOG-5.x.md>`__
* OXID eShop Facts: v4.2.0 → v4.3.0 `Changelog <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.3.0/CHANGELOG-4.x.md>`__
* Unified Namespace Generator: v5.1.0 → v5.2.0 `Changelog <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.2.0/CHANGELOG.md>`__
* Twig Admin Theme: v2.5.0 → v2.6.1 `Changelog <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.6.1/CHANGELOG-2.x.md>`__
* Twig-Komponente: v2.5.0 → v2.6.0 `Changelog <https://github.com/OXID-eSales/twig-component/blob/v2.6.0/CHANGELOG-2.x.md>`__
* OXID Cookie Management powered by usercentrics: v3.0.0 → v3.1.0 `Changelog <https://github.com/OXID-eSales/usercentrics/blob/v3.1.0/CHANGELOG.md>`__
* Visual CMS: v7.0.3 → v8.0.1
* OXID eShop PE: v7.2.0 → v7.3.0
* Demodaten EE: v8.0.3 → v8.1.0
* OXID eShop EE: v7.2.0 → v7.3.0


Bestandteile der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält folgende Komponenten:

* `OXID eShop CE 7.3.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.3.0/CHANGELOG-7.3.md>`_
* OXID eShop PE 7.3.0
* OXID eShop EE 7.3.0

* `Apex Theme 2.1.0 <https://github.com/OXID-eSales/apex-theme/blob/v2.1.0/CHANGELOG-2.x.md>`_

* `Twig Admin Theme 2.6.1 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.6.1/CHANGELOG-2.x.md>`_
* `Twig-Komponente CE 2.6.0 <https://github.com/OXID-eSales/twig-component/blob/v2.6.0/CHANGELOG-2.x.md>`_
* Twig-Komponente PE 2.6.0
* Twig-Komponente EE 2.6.0

* `Composer-Plugin 7.3.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.3.0/CHANGELOG-7.x.md>`_
* `Views Generator 2.2.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* `Demodaten-Installer 3.3.0 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_

* `Demodaten CE 8.0.2 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.2/CHANGELOG.md>`_
* Demodaten PE 8.0.2
* Demodaten EE 8.1.0

* `Doctrine Migration Integration 5.4.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.4.0/CHANGELOG-5.x.md>`_
* `OXID eShop Facts 4.3.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.3.0/CHANGELOG-4.x.md>`_
* `Unified Namespace Generator 5.2.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.2.0/CHANGELOG.md>`_

* `GDPR Opt-In 4.2.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.2.0/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 3.1.0 <https://github.com/OXID-eSales/usercentrics/blob/v3.1.0/CHANGELOG.md>`_
* Visual CMS 8.0.1 (PE/EE)

* `WYSIWYG Editor 5.0.0 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v5.0.0/CHANGELOG.md>`_
* `Mediathek 3.0.0 <https://github.com/OXID-eSales/media-library-module/blob/v3.0.0/CHANGELOG.md>`_
* `Makaira 2.1.3 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.3/CHANGELOG.md>`_
* `Eye-Able 3.0.3 <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/blob/v3.0.3/CHANGELOG.md>`_


Installation
------------

Zur Installation oder Aktualisierung folgen Sie den Anweisungen unter :doc:`Installation <../../installation/index>`.


Kompatible Module
------------------

Eine Übersicht über die zugehörigen OXID-Module finden Sie unter :doc:`Kompatible Module für OXID eShop 7.3.0 <oxid-eshop-730-modules>`.


.. Intern: , Status:
