Minor Update installieren
=========================

Aktualisieren Sie die Compilation beispielsweise von einer bestehenden Version 7.0.x auf Version 7.1.x.

.. include:: /_static/reuse/note_dataloss.rst

Kompatibilität von Drittanbieter-Modulen sicherstellen
------------------------------------------------------

Wenn Sie Module oder Themes von Drittanbietern verwenden, fragen Sie den Drittanbieter, ob diese Themes und Module mit der neuen Version des OXID eShops kompatibel sind.

Hintergrund: Normalerweise enthält ein Minor Update keine breaking changes. Alle Module von Drittanbietern funktionieren nach dem Update wie zuvor.

In Ausnahmefällen können sich Änderungen jedoch so auswirken, dass Module von Drittanbietern nicht mehr funktionieren.

Update ausführen
----------------

Aktualisieren Sie Ihren OXID eShop auf die aktuelle Version.

|prerequisites|

Sie haben :productname:`OXID eShop` 7.0.x.

|procedure|

1. Deaktivieren Sie alle Module.
#. Aktualisieren Sie Composer auf Version 2.7.

   Installieren Sie Composer 2.7 beispielsweise wie folgt:

   .. code:: bash

      composer selfupdate 2.7.1

#. Aktualisieren Sie in der Datei :file:`composer.json` die Version des Metapackage.
   |br|
   Passen Sie dazu wie im folgenden Beispiel den Namen des Metapackage der gewünschten Shop-Edition an.
   |br|
   Beispiel für ein Update einer Community Edition mit dem Metapackage-Namen ``7.1.0``:

   .. todo: #HR: Verifizieren

   .. code:: bash

      composer require --no-update oxid-esales/oxideshop-metapackage-ce:v7.1.0

#. Aktualisieren Sie die Abhängigkeiten.
   |br|
   Öffnen Sie eine Shell im Hauptverzeichnis des Shops und führen Sie den nachstehenden Composer-Befehl aus.
   |br|
   Dadurch werden alle benötigten Bibliotheken aktualisiert.
   |br|
   Den Parameter :command:`--no-dev` geben Sie an, wenn Sie die entwicklungsbezogenen Dateien nicht brauchen.

   .. code:: bash

      composer update --no-plugins --no-scripts --no-dev

#. Um die neue Compilation zu beziehen und das Update auszuführen, führen Sie die Skripte aus.
   |br|
   Führen Sie dazu den folgenden Befehl aus.
   |br|


   .. note::

      Durch das Update werden mögliche Änderungen überschrieben, die Sie im Verzeichnis :file:`source` an Modulen oder Themes vorgenommen haben.

      Hintergrund: Bei einem Shop-Update lädt Composer die neuen Daten zunächst ins Verzeichnis :file:`vendor`. Anschließend werden die Daten ins Verzeichnis :file:`source` kopiert. Damit werden die Dateien des Shops, der Module und der Themes ersetzt.

      Ihre individuellen Anpassungen des OXID Shops oder Änderungen an Modulen von Fremdherstellern sind nur dann vorm Überschreiben durch das Update sicher, wenn Sie die Änderungen durch eine der Erweiterungsmöglichkeiten des OXID eShops (Component, Modul, Child-Theme) vorgenommen haben.

      Weitere Informationen finden Sie in der Entwickler-Dokumentation unter

      * `Module skeleton: metadata, composer, and structure <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/skeleton/index.html>`_
      * `How to create a theme installable via composer? <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/theme/theme_via_composer.html>`_


   .. attention::

      **Abfragen bestätigen**

      Während des Updates werden Sie gefragt, welche Pakete überschrieben werden dürfen.

      Damit nur kompatible und getestete Pakete installiert werden und es nicht zu Inkonsistenzen und Fehlfunktionen durch fehlerhaft implementierte Module oder Themes kommen kann, müssen Sie die Abfragen mit :technicalname:`Ja` bestätigen.


      Empfehlungen:

      * Wenn Sie die Erweiterungsmöglichkeiten des OXID eShops nutzen, folgen Sie den Anweisungen in der `Entwickler-Dokumentation <https://docs.oxid-esales.com/developer/en/latest/>`_.
      * Holen Sie zum Erstellen von Modulen oder Child-Themes die Unterstützung einer OXID-Partner-Agentur ein. Dies erleichtert Ihnen alle künftigen Updates.
        |br|
        Eine Liste der von OXID zertifizierten Partneragenturen finden Sie unter `oxid-esales.com/partner/partner-finden/ <https://www.oxid-esales.com/partner/partner-finden/>`_.
      * Wenn Sie Module oder Themes von Drittanbietern verwenden, fragen Sie den Drittanbieter, ob diese Themes und Module mit der neuen Version des OXID eShops kompatibel sind.
        |br|
        Hintergrund: Normalerweise enthält ein Minor Update keine breaking changes. Alle Module von Drittanbietern funktionieren nach dem Update wie zuvor.
        |br|
        In Ausnahmefällen können sich Änderungen jedoch so auswirken, dass Module von Drittanbietern nicht mehr funktionieren.

   .. code:: bash

      composer update --no-dev

#. Um sicherzustellen, dass die zwischengespeicherten Elemente keine Inkompatibilitäten enthalten, leeren Sie das Verzeichnis :file:`tmp`.
   |br|
   Führen Sie dazu den folgenden Befehl aus.

   .. code:: bash

      rm -rf source/tmp/*

#. Migrieren Sie die Datenbank.
   |br|
   Führen Sie dazu den folgenden Befehl aus.

   .. code:: bash

      vendor/bin/oe-eshop-db_migrate migrations:migrate

#. Generieren Sie die Datenbank-Views neu.
   |br|
   Hintergrund: Je nach Änderungen und Shop-Edition kann es sein, dass der Shop nach dem Update in den Wartungsmodus geht.
   |br|
   Um dem vorzubeugen, generieren Sie die Datenbank-Views mit folgendem Befehl neu:

   .. code:: bash

      vendor/bin/oe-eshop-db_views_generate

#. Aktivieren Sie alle Module.

.. Intern: oxbajz, Status:
