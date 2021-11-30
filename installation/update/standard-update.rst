Standard-Update
===============

Dieses Dokument beschreibt Patch-Updates des OXID eShop. Mit den folgenden Schritten wird die Compilation von einer bestehenden
Version 6.4.x auf eine höhere Version 6.4.x aktualisiert.

.. todo #tbd: prüfen

Das Update sollte immer erst in einer Testumgebung, einer Kopie Ihres aktuellen Shops, ausgeführt werden. Erstellen Sie zuvor eine Sicherung der Shopdateien und der Datenbank. Deaktivieren Sie alle Module und prüfen Sie, ob der Shop prinzipiell funktioniert. Testen Sie nach dem Update den Shop erneut und legen Sie dabei besonderen Wert auf die Funktionen des Bestellprozesses, auf Zahlungs- und Versandarten.

.. |schritt| image:: ../../media/icons/schritt.jpg
              :class: no-shadow

|schritt| Update-Ziel vorgeben
------------------------------

Aktualisieren Sie die Version des Metapackage in der Datei :file:`composer.json`, die sich im Hauptverzeichnis des Shops befindet.

Passen Sie dazu im folgenden Befehl der Name des Metapackage an die verwendete Shop Edition an, und führen Sie den Befehl aus.

In unserem Beispiel aktualisieren Sie eine Community Edition von Version 6.4.0 zu Version 6.4.1:

.. code:: bash

   composer require --no-update oxid-esales/oxideshop-metapackage-ce:v6.4.1


|schritt| Abhängigkeiten aktualisieren
--------------------------------------

Öffnen Sie eine Shell im Hauptverzeichnis des Shops und führen Sie den nachstehenden Composer-Befehl aus.
Dadurch werden alle benötigten Bibliotheken aktualisiert. Der Parameter :command:`--no-dev` wird angegeben,
wenn die entwicklungsbezogenen Dateien nicht benötigt werden.

.. code:: bash

   composer update --no-plugins --no-scripts --no-dev

|schritt| Neue Compilation beziehen
-----------------------------------
Mit einem zweiten Composer-Befehl werden alle Scripts ausgeführt, um die neue Compilation zu beziehen. Für Shopdateien,
Themes und Module muss jeweils bestätigt werden, dass das Update bestehende Dateien überschreibt.

.. code:: bash

   composer update --no-dev

|schritt| Temporäre Dateien löschen
-----------------------------------

Um sicherzustellen, dass die zwischengespeicherten Elemente keine Inkompatibilitäten enthalten, muss das Verzeichnis :file:`/tmp` geleert werden.

.. code:: bash

   rm -rf source/tmp/*

|schritt| Datenbank migrieren
-----------------------------

DMigrieren Sie Datenbank.


.. code:: bash

   vendor/bin/oe-eshop-db_migrate migrations:migrate

|schritt| Optional: Views generieren
------------------------------------
Je nach Änderungen und Shop-Edition kann es sein, dass der Shop in den Wartungsmodus geht, solange die Views nicht neu generiert werden.

.. code:: bash

   vendor/bin/oe-eshop-db_views_generate

.. hint::

   Wird üblicherweise beim Update einer Enterprise Edition benötigt. #tbd wenn EE, dann vermutlich nötig

Damit ist das Update beendet.


.. Intern: oxbaix, Status:
