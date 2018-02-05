Standard-Update ab 6.0.0
========================

Dieses Dokument beschreibt Patch- und Minor-Updates ab Version 6.0.0 des OXID eShop. Mit den folgenden Schritten wird die Compilation von einer bestehenden Version 6.x.x auf eine höhere Version 6.x.x aktualisiert.

Das Update sollte immer erst in einer Testumgebung, einer Kopie Ihres aktuellen Shops, ausgeführt werden. Erstellen Sie zuvor eine Sicherung der Shopdateien und der Datenbank. Deaktivieren Sie alle Module und prüfen Sie, ob der Shop prinzipiell funktioniert. Testen Sie nach dem Update den Shop erneut und legen Sie dabei besonderen Wert auf die Funktionen des Bestellprozesses, auf Zahlungs- und Versandarten.

.. |schritt| image:: ../../media/icons-de/schritt.jpg

|schritt| Update-Ziel vorgeben
------------------------------
In die Datei :file:`composer.json`, die sich im Hauptverzeichnis des Shops befindet, muss die Version eingetragen werden, auf welche aktualisiert werden soll. Öffnen Sie die Datei in einem Editor und tragen Sie die gewünschte Version für das Metapackage ein. Beispiel: ``"oxid-esales/oxideshop-metapackage-ce": "^v6.0.0",``

|schritt| Abhängigkeiten aktualisieren
--------------------------------------
Öffnen Sie eine Shell im Hauptverzeichnis des Shops und führen Sie den nachstehenden Composer-Befehl aus. Dadurch werden alle benötigten Bibliotheken aktualisiert.

.. code:: bash

   composer update --no-plugins --no-scripts

|schritt| Neue Compilation beziehen
-----------------------------------
Mit einem zweiten Composer-Befehl werden alle Scripts ausgeführt, um die neue Compilation zu beziehen. Für Shopdateien, Themes und Module muss jeweils bestätigt werden, dass das Update bestehende Dateien überschreibt.

.. code:: bash

   composer update

|schritt| Datenbank migrieren
-----------------------------
Der dritte und letzte Composer-Befehl führt die Migration der Datenbank aus, falls dies erforderlich ist.

.. code:: bash

   vendor/bin/oe-eshop-db_migrate migrations:migrate

Damit ist das Update beendet.

.. Intern: oxbaic, Status: