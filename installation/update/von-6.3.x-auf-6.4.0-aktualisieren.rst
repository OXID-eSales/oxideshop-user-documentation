Von 6.3.x auf 6.4.0 aktualisieren
=================================

.. todo #tbd: EN nachziehen #HR: dieses Dok anpassen (6.3.1 auf 6.4 )oder obsolet? Gibt es spezielle Prozedur? -- diese Proz behalten

Führen Sie ein Minor-Update des OXID eShop aus.

Mit den folgenden Schritten aktualisieren Sie die Compilation beispielsweise von einer bestehenden Version 6.3.x auf die Version 6.4.0.

.. ATTENTION::
   **Datenverlust**

   Führen Sie das Update immer erst in einer Testumgebung, einer Kopie Ihres aktuellen Shops, aus.

   Erstellen Sie zuvor eine Sicherung der Shopdateien und der Datenbank.

   Deaktivieren Sie alle Module und prüfen Sie, ob der Shop prinzipiell funktioniert.

   Testen Sie nach dem Update den Shop erneut. Prüfen Sie besonders die Funktionen des Bestellprozesses, die Zahlungs- und Versandarten.

.. |schritt| image:: ../../media/icons/schritt.jpg
              :class: no-shadow

|schritt| Update-Ziel vorgeben
------------------------------

Aktualisieren Sie in der Datei :file:`composer.json`, die sich im Hauptverzeichnis des Shops befindet, die Version des Metapackage.


1. Passen Sie im folgenden Beispielbefehl die Versions-Nummer des Metapackage an die verwendete Shop-Edition an:

   .. code:: bash

      composer require --no-update oxid-esales/oxideshop-metapackage-<Typ der Edition: ce, pe oder ee>**:v**<Versions-Nummer>

2. Führen Sie den Befehl aus, in unserem Beispiel für das Update einer Community Edition 6.3.1 zu 6.4.0:

   .. code:: bash

      composer require --no-update oxid-esales/oxideshop-metapackage-ce:v6.4.0

3. Aktualisieren Sie die Versionen im ``require-dev``-Bereich:

   .. hint::

      Auch wenn Sie in den folgenden Schritten die Compilation ohne die Dev-Pakete installieren, prüft Composer deren Abhängigkeiten.

      Diese Anpassung ist somit zwingend notwendig.

   .. code:: bash

      composer require --dev --no-update oxid-esales/testing-library:^v8.0.0 oxid-esales/oxideshop-ide-helper:^v4.1.0

.. todo Metapackage prüfen, welche testing lib



|schritt| Abhängigkeiten aktualisieren
--------------------------------------

Aktualisieren Sie die benötigten Bibliotheken.

1. Öffnen Sie eine Shell im Hauptverzeichnis des Shops.

   .. code:: bash

      cd /var/www/oxideshop

2. Führen Sie den folgenden Composer-Befehl aus.

   Optonal: Wenn Sie die entwicklungsbezogenen Dateien nicht brauchen, verwenden Sie den Parameter :command:`--no-dev`.

   .. code:: bash

      composer update --no-plugins --no-scripts --no-dev

|schritt| Neue Compilation beziehen
-----------------------------------

Führen Sie die Skripte aus, um die neue Compilation zu beziehen:

.. code:: bash

   composer update --no-dev

Bestätigen Sie dabei für Shopdateien, Themes und Module, dass das Update bestehende Dateien überschreibt.

|schritt| Temporäre Dateien löschen
-----------------------------------

Um sicherzustellen, dass die zwischengespeicherten Elemente keine Inkompatibilitäten enthalten, leeren Sie das Verzeichnis :file:`/tmp`.

.. code:: bash

   rm -rf source/tmp/*

|schritt| Datenbank migrieren
-----------------------------

Migrieren Sie die Datenbank.

.. code:: bash

   vendor/bin/oe-eshop-db_migrate migrations:migrate

Wenn nichts zu migrieren ist, erscheint die Meldung `PHP Warning:  require_once(migrate.php): failed to open stream: No such file or directory in /var/www/oxides`

|schritt| Optional: Datenbank-Views generieren
----------------------------------------------

Je nach Änderungen und Shop-Edition kann es sein, dass der Shop in den Wartungsmodus geht, solange die Datenbank-Views nicht neu generiert werden.

Prüfen Sie den Shop und führen Sie bei Bedarf den folgenden Befehl aus.

.. todo #HR/#AF: how do I identify that the db views have to be generated?

Eine Enterprise Edition enthalt Datenbank-Views der Subshops. Vor allem hier kann deshalb das Aktualisieren der Datenbank-Views nötig sein.

.. code:: bash

   vendor/bin/oe-eshop-db_views_generate


Das Update ist beendet. Wenn Sie den Shop als Administrator öffnen, wird die neue Version rechts oben angezeigt.


.. Intern: oxbaix, Status: