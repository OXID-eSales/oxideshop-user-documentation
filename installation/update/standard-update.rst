Standard-Update
===============


Führen Sie ein Update des OXID eShop aus.

Mit den folgenden Schritten aktualisieren Sie die Compilation beispielsweise von einer bestehenden Version 6.3.x auf die Version 6.4.1.

.. ATTENTION::
   **Datenverlust**

   Führen Sie das Update immer erst in einer Testumgebung, einer Kopie Ihres aktuellen Shops, aus.

   Erstellen Sie zuvor eine Sicherung der Shop-Dateien und der Datenbank.

   Deaktivieren Sie alle Module und prüfen Sie, ob der Shop prinzipiell funktioniert.

   Testen Sie nach dem Update den Shop erneut. Prüfen Sie besonders die Funktionen des Bestellprozesses, die Zahlungs- und Versandarten.

.. |schritt| image:: ../../media/icons/schritt.jpg
              :class: no-shadow

|schritt| Update-Ziel vorgeben
------------------------------

Um das Update auszuführen, wechseln Sie ins Hauptverzeichnis des Shops. Aktualisieren Sie in der Datei :file:`composer.json`, die sich im Hauptverzeichnis des Shops befindet, die Version des Metapackage.


1. Wechseln Sie ins Hauptverzeichnis des Shops (in unserem Beispiel `/var/www/oxideshop/`).

   .. code:: bash

      cd /var/www/oxideshop/

2. Passen Sie im folgenden Beispielbefehl die Versions-Nummer des Metapackage entsprechend der neuen Shop-Edition an:

   .. code:: bash

      composer require --no-update oxid-esales/oxideshop-metapackage-<Typ der Edition: ce, pe oder ee>:v<Versions-Nummer>

3. Führen Sie den Befehl aus, in unserem Beispiel für das Update einer Community Edition 6.3.1 zu 6.4.1:

   .. code:: bash

      composer require --no-update oxid-esales/oxideshop-metapackage-ce:v6.4.1




|schritt| Abhängigkeiten aktualisieren
--------------------------------------

Aktualisieren Sie die benötigten Bibliotheken.

Führen Sie dazu den folgenden Composer-Befehl aus.

Optional: Wenn Sie die entwicklungsbezogenen Dateien nicht brauchen, verwenden Sie den Parameter :command:`--no-dev`.

.. todo: #HR: in welchem Fall brauche ich die entwicklungsbezogenen Dateien?

.. code:: bash

   composer update --no-plugins --no-scripts --no-dev


|schritt| Neue Compilation beziehen
-----------------------------------

Führen Sie die Skripte aus, um die neue Compilation zu beziehen.

Bestätigen Sie dabei für Shop-Dateien, Themes und Module, dass das Update bestehende Dateien überschreibt.


.. code:: bash

   composer update --no-dev


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



|schritt| Wenn nötig: Datenbank-Views generieren
------------------------------------------------

Je nach Änderungen und Shop-Edition kann es sein, dass der Shop in den Wartungsmodus geht.

Wenn der Shop nach dem Update im Wartungsmodus ist, generieren Sie die Datenbank-Views mit folgendem Befehl neu:

.. code:: bash

   vendor/bin/oe-eshop-db_views_generate


Das Update ist beendet. Wenn Sie den Shop als Administrator öffnen, wird die neue Version rechts oben angezeigt.


.. Intern: oxbaix, Status:
