OXID eShop Compilation 7.4.1
============================

Veröffentlichungsdatum: TBD

Optimierungen & Fehlerbehebungen
--------------------------------

Composer 2.9 Kompatibilität
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Composer 2.9 führt einen automatischen Sicherheits-Audit
durch und bricht die Installation ab, wenn Pakete mit
bekannten Sicherheitsproblemen enthalten sind. Bei der
OXID eShop 7.4.0 Compilation konnte dies dazu führen, dass
die Installation mit den Standardeinstellungen von
Composer 2.9 fehlschlug.

In der Compilation 7.4.1 wurden die betroffenen Pakete
aktualisiert, so dass die Installation mit den
Standardeinstellungen von Composer 2.9 problemlos
funktioniert.

Die betroffenen Pakete wurden aktualisiert:

* ``composer/composer`` von 2.8.12 auf 2.9.8
* ``symfony/process`` von v7.3.4 auf v7.4.8

OXID eShop 7.4.1 kann sowohl mit Composer CLI 2.8 als auch
mit Composer CLI 2.9 problemlos installiert werden.

Content & Medien Bundle
^^^^^^^^^^^^^^^^^^^^^^^

**Media Library Module** (v4.1.0 auf v4.2.0, oder v3.0.0 bleibend):

* Neu: SVG-Upload-Inhaltsvalidierung — Dateien mit Skripten, Foreign Objects, ``on*``-Event-Handlern oder ``javascript:``/``data:``-URLs werden abgelehnt
* Neu: MIME-Typ-Validierung bei jedem Upload — Dateien, deren erkannter Content-Type nicht zur deklarierten Dateiendung passt, werden abgelehnt
* Neu: Inhaltsvalidierung für Rasterbilder (jpg, jpeg, gif, png, webp, avif) — Dateien, die nicht als gültiges Bild geparst werden können, werden abgelehnt
* Neu: ``FileFormatRegistry`` zur Zuordnung erlaubter Dateiendungen zu akzeptierten MIME-Typen; Integratoren können zusätzliche Formate per Service-Konfiguration registrieren
* Neu: ``ContentValidatorInterface`` für formatspezifische Inhaltsprüfungen; getaggte Services werden von der Upload-Kette automatisch erkannt
* Neu: ``FilePathInterface::getExtension()`` liefert die kleingeschriebene Dateiendung
* Geändert: Einheitliche Dateinamen-Bereinigung bei Upload und Umbenennen
* Geändert: ``composer.json`` deklariert nun ``ext-dom``
* Sicherheit: Path-Traversal-Zeichen (``/``, ``\``, ``..``-Segmente, Null-Bytes) in Upload-Dateinamen werden abgelehnt
* Behoben (durch die obigen Validierungen): `#0007937 <https://bugs.oxid-esales.com/view.php?id=7937>`_ und `#0007938 <https://bugs.oxid-esales.com/view.php?id=7938>`_
* Behoben: Strg+Klick-Mehrfachauswahl funktionierte aufgrund einer falschen Event-Button-Prüfung nicht

**WYSIWYG Editor** (v6.0.1 auf v6.0.3):

* Behoben: Summernote-Toolbar-Dropdowns öffneten sich nicht aufgrund eines Bootstrap-5-Event-Delegation-Konflikts
* Behoben: Inhalte wurden gelöscht, wenn Emojis in Text-Widgets verwendet wurden (`#0007619 <https://bugs.oxid-esales.com/view.php?id=7619>`_)
* Behoben: Fehlerhafte Bootstrap-Style-Imports, die Shop-Styles beeinflussten

**Visual CMS** (v9.1.0 auf v9.2.1, nur Professional und Enterprise Edition):

* Neu: Verschachtelte Aktivitätsgruppen mit UND/ODER-Logik für komplexe zeitbasierte Sichtbarkeitsregeln von Widgets
* Neu: Ausschlusszeiträume für Aktivitätszeiträume
* Behoben: Widget-Eigenschaften von Spalten-Widgets wurden nicht angezeigt, wenn die Bearbeitung eines anderen Widgets und des Spalten-Widgets gleichzeitig geöffnet war
* Behoben: Beim Befehl ``ddoevisualcms:migrate:veparse-to-vetree`` wird das Flag "Widget-Modus" nun für konvertierte "veparse"-Inhalte aktiviert
* Behoben: Inhalte wurden gelöscht, wenn Emojis in Text-Widgets verwendet wurden (`#0007619 <https://bugs.oxid-esales.com/view.php?id=7619>`_)
* Behoben: Medien-URLs in Text-Widgets werden nun beim Befehl ``ddoevisualcms:migrate:urls-to-ids`` migriert
* Behoben: Datumsauswahl-Felder respektieren jetzt die im Shop konfigurierte Datumsformat-Einstellung
* Behoben: Karussell-Widget verlor Bilder und Links nach erneutem Öffnen des Bearbeitungsdialogs

Hinweis für Integratoren:

* Die Upload-Validator-Kette enthält jetzt ``MimeTypeValidator`` und ``ContentValidatorChain`` nach dem ``FileExtensionValidator``. Module, die ``UploadedFileValidatorChainInterface`` vollständig ersetzen, müssen beide Validatoren in derselben Reihenfolge auflisten, um den Upload-Inhaltsschutz zu erhalten.
* ``FilePathInterface`` enthält die neue Methode ``getExtension()``. Module, die dieses Interface selbst implementieren, müssen die Methode ergänzen — sie gibt die kleingeschriebene Dateiendung zurück.

Entwickler-Werkzeuge
^^^^^^^^^^^^^^^^^^^^

**OXID eShop Unified Namespace Generator** (v5.2.0 auf v5.2.1):

* Behoben: Dateipfad-Normalisierung für Sub-Namespaces, die Backslashes enthalten

.. _packages-741:

Packages
--------

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop CE Compilation enthält die folgenden Pakete:

* APEX Theme v3.0.2
* Eye-Able Assist v3.0.3
* GDPR Opt-In Module v4.3.0
* Makaira Connect Essential 2.1.4
* Media Library Module v4.2.0 (oder v3.0.0 bleibend)
* OXID Cookie Management powered by Usercentrics v3.2.1
* OXID eShop CE von v7.4.0 auf v7.4.2
* OXID eShop Composer Plugin v7.3.0
* OXID eShop Demodata CE v8.1.0
* OXID eShop Demodata Installer v3.3.0
* OXID eShop Doctrine Migration Wrapper v5.4.0
* OXID eShop Facts v4.3.0
* OXID eShop Unified Namespace Generator v5.2.1
* OXID eShop Views Generator v2.2.0
* Twig Admin Theme v3.0.1
* Twig Component v2.7.0
* WYSIWYG Editor Module von v6.0.1 auf v6.0.3 (oder v5.0.1 bleibend): `Changelog <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v6.0.3/CHANGELOG.md>`_

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop PE Compilation enthält zusätzlich die
folgenden Pakete:

* OXID eShop Demodata PE v8.1.0
* OXID eShop PE von v7.4.0 auf v7.4.2
* Twig Component PE v2.5.0
* Visual CMS Modul von v9.1.0 auf v9.2.1 (oder v8.0.2 bleibend)

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop EE Compilation enthält zusätzlich die
folgenden Pakete:

* OXID eShop Demodata EE v8.2.0
* OXID eShop EE von v7.4.0 auf v7.4.2
* Twig Component EE v2.5.0

OXID eShop EE B2B Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop EE B2B Compilation enthält zusätzlich die
folgenden Pakete:

* OXID eShop B2B Approval Procedure Modul von v7.4.0 auf v7.4.1
* OXID eShop B2B Basket Modul v7.4.0
* OXID eShop B2B Budget Modul v7.4.0
* OXID eShop B2B Bulk Orders Modul v7.4.0
* OXID eShop B2B Buying Agent Modul v7.4.0
* OXID eShop B2B Custom Prices Modul v7.4.0
* OXID eShop B2B Offers Modul v7.4.0
* OXID eShop B2B Quick Orders Modul v7.4.0
* OXID eShop B2B Scheduled Orders Modul v7.4.0
* OXID eShop B2B Service Products Modul v7.4.0
* OXID eShop B2B Services Modul v7.4.0

Für weitere Informationen zu Veröffentlichungen der
B2B Edition, siehe die (passwortgeschützte)
`OXID eShop Enterprise B2B Edition <https://docs.oxid-esales.com/b2b/de/7.4/releases/b2b-edition-740.html>`_
Dokumentation.

Kompatible OXID Erweiterungen
-----------------------------

Die kompatiblen OXID Erweiterungen entsprechen denen der
Version 7.4.0. Weitere Informationen finden Sie in den
`Release Notes der OXID eShop Compilation 7.4.0 <oxid-eshop-740>`.

Update
------

Führen Sie die folgenden Befehle aus, um Ihren OXID eShop
von 7.4.0 auf 7.4.1 zu aktualisieren:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate
