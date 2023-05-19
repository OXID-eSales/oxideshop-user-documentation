Patch-Update installieren
=========================

Führen Sie bei Bedarf ein Patch-Update Ihres OXID eShops durch.

Mit den folgenden Schritten aktualisieren Sie die Compilation beispielsweise von einer bestehenden Version 6.5.x auf die Version 6.5.2.

.. include:: /_static/reuse/note_dataloss.rst



|procedure|

1. Aktualisieren Sie Composer auf Version 2.2.x.

   .. attention::

      Composer 2.3.x wird nicht unterstützt.

      Wenn Sie Composer 2.3.x haben, installieren Sie Composer 2.2.x beispielsweise wie folgt:

      .. code:: bash

         sudo composer selfupdate 2.2.12

#. Wechseln Sie ins Hauptverzeichnis des Shops (in unserem Beispiel `/var/www/oxideshop/`).

   .. code:: bash

      cd /var/www/oxideshop/

#. Aktualisieren Sie in der Datei :file:`composer.json`, die sich im Hauptverzeichnis des Shops befindet, die Version des Metapackage.
   |br|
   Dazu tun Sie Folgendes:

   a. Passen Sie im folgenden Beispielbefehl die Versions-Nummer des Metapackage entsprechend der neuen Shop-Edition an:

      .. code:: bash

         composer require --no-update oxid-esales/oxideshop-metapackage-<Typ der Edition: ce, pe oder ee>:v<Versions-Nummer>

   b. Führen Sie den Befehl aus, in unserem Beispiel für das Update einer Community Edition 6.5.1 zu 6.5.2:

      .. code:: bash

         composer require --no-update oxid-esales/oxideshop-metapackage-ce:v6.5.2

#. Aktualisieren Sie die benötigten Bibliotheken.
   |br|
   Führen Sie dazu den folgenden Composer-Befehl aus.
   |br|
   Optional: Wenn Sie die entwicklungsbezogenen Dateien nicht brauchen, verwenden Sie den Parameter :command:`--no-dev`.

   .. todo: #HR: in welchem Fall brauche ich die entwicklungsbezogenen Dateien?

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
