Patch-Update installieren
=========================

Führen Sie bei Bedarf ein Patch-Update Ihres OXID eShops durch.

Mit den folgenden Schritten aktualisieren Sie die Compilation beispielsweise von einer bestehenden Version 7.0.2 auf die Version 7.0.3.

.. include:: /_static/reuse/note_dataloss.rst

|procedure|

1. Aktualisieren Sie Composer auf Version 2.7.

   Installieren Sie Composer 2.7 beispielsweise wie folgt:

   .. code:: bash

      composer selfupdate 2.7.1

#. Wechseln Sie ins Hauptverzeichnis des Shops (in unserem Beispiel `/var/www/oxideshop/`).

   .. code:: bash

      cd /var/www/oxideshop/

#. Aktualisieren Sie in der Datei :file:`composer.json`, die sich im Hauptverzeichnis des Shops befindet, die Version des Metapackage.
   |br|
   Dazu tun Sie Folgendes:

   a. Passen Sie im folgenden Beispielbefehl die Versions-Nummer des Metapackage entsprechend der neuen Shop-Edition an:

      .. code:: bash

         composer require --no-update oxid-esales/oxideshop-metapackage-<Typ der Edition: ce, pe oder ee>:v<Versions-Nummer>

   b. Führen Sie den Befehl aus, in unserem Beispiel für das Update einer Enterprise Edition 7.0.2 zu 7.0.3:

      .. code:: bash

         composer require --no-update oxid-esales/oxideshop-metapackage-ee:v7.0.3

#. Aktualisieren Sie die benötigten Bibliotheken.
   |br|
   Führen Sie dazu den folgenden Composer-Befehl aus.
   |br|
   Optional: Wenn Sie die entwicklungsbezogenen Dateien brauchen, lassen Sie den Parameter :command:`--no-dev` weg.

   .. code:: bash

      composer update --no-plugins --no-scripts --no-dev

#. Laden Sie die neue Compilation herunter.
   |br|
   Führen Sie dazu den folgenden Composer-Befehl aus.

   .. code:: bash

      composer update --no-dev

#. Bestätigen Sie für Shop-Dateien, Themes und Module, dass das Update bestehende Dateien überschreibt.

#. Um sicherzustellen, dass die zwischengespeicherten Elemente keine Inkompatibilitäten enthalten, leeren Sie das Verzeichnis :file:`/tmp`.

   .. code:: bash

      rm -rf source/tmp/*

#. Migrieren Sie die Datenbank.

   .. code:: bash

      vendor/bin/oe-eshop-db_migrate migrations:migrate

#. Generieren Sie die Datenbank-Views neu.
   |br|
   Hintergrund: Je nach Änderungen und Shop-Edition kann es sein, dass der Shop nach dem Update in den Wartungsmodus geht.
   |br|
   Um dem vorzubeugen, generieren Sie die Datenbank-Views mit folgendem Befehl neu:

   .. code:: bash

      vendor/bin/oe-eshop-db_views_generate

|result|

Das Update ist beendet. Wenn Sie den Shop als Administrator öffnen, wird die neue Version rechts oben angezeigt.


.. Intern: oxbajy, Status:
