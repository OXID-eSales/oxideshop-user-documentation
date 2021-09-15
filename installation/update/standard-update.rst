Standard-Update
===============

Dieses Dokument beschreibt Patch- und Minor-Updates des OXID eShop. Mit den folgenden Schritten wird die Compilation von einer bestehenden Version 6.2.x auf eine höhere Version 6.2.x aktualisiert.

Das Update sollte immer erst in einer Testumgebung, einer Kopie Ihres aktuellen Shops, ausgeführt werden. Erstellen Sie zuvor eine Sicherung der Shopdateien und der Datenbank. Deaktivieren Sie alle Module und prüfen Sie, ob der Shop prinzipiell funktioniert. Testen Sie nach dem Update den Shop erneut und legen Sie dabei besonderen Wert auf die Funktionen des Bestellprozesses, auf Zahlungs- und Versandarten.

.. warning::

   Beim Update von OXID eShop 6.2.0 bis 6.2.4 auf OXID eShop 6.2.5 oder höher, muss zuvor Composer auf Version 2 aktualisiert werden.

.. |schritt| image:: ../../media/icons/schritt.jpg
              :class: no-shadow

|schritt| Update-Ziel vorgeben
------------------------------
In der Datei :file:`composer.json`, die sich im Hauptverzeichnis des Shops befindet, muss die Version des Metapackage aktualisiert werden.

Beispiel für ein Update einer Community Edition 6.2.0 zu 6.2.1:

.. code:: bash

   composer require --no-update oxid-esales/oxideshop-metapackage-ce:v6.2.1

.. hint::

   Der Name des Metapackage muss an die verwendete Shop-Edition angepasst werden.

Wenn Sie von Version 6.2.0, 6.2.1, 6.2.2 oder 6.2.3 auf 6.2.4 oder höher aktualisieren, muss anschließend noch der IDE Helper im ``require-dev`` Bereich aktualisiert werden.

.. code:: bash

   composer require --dev --no-update oxid-esales/oxideshop-ide-helper:^v4.0.0

.. warning::

   Auch wenn die Dev-Pakete nicht installiert werden, prüft Composer deren Abhängigkeiten. Diese Anpassung ist somit zwingend notwendig, wenn sie von den genannten Versionen auf 6.2.4 oder höher aktualisieren möchten.

|schritt| Abhängigkeiten aktualisieren
--------------------------------------
Öffnen Sie eine Shell im Hauptverzeichnis des Shops und führen Sie den nachstehenden Composer-Befehl aus. Dadurch werden alle benötigten Bibliotheken aktualisiert. Der Parameter :command:`--no-dev` wird angegeben, wenn die entwicklungsbezogenen Dateien nicht benötigt werden.

.. code:: bash

   composer update --no-plugins --no-scripts --no-dev

|schritt| Neue Compilation beziehen
-----------------------------------
Mit einem zweiten Composer-Befehl werden alle Scripts ausgeführt, um die neue Compilation zu beziehen. Für Shopdateien, Themes und Module muss jeweils bestätigt werden, dass das Update bestehende Dateien überschreibt.

.. code:: bash

   composer update --no-dev

|schritt| Temporäre Dateien löschen
-----------------------------------
Um sicherzustellen, dass die zwischengespeicherten Elemente keine Inkompatibilitäten enthalten, muss das Verzeichnis :file:`/tmp` geleert werden.

.. code:: bash

   rm -rf source/tmp/*

|schritt| Datenbank migrieren
-----------------------------
Der dritte und letzte Composer-Befehl führt die Migration der Datenbank aus, falls dies erforderlich ist.

.. code:: bash

   vendor/bin/oe-eshop-db_migrate migrations:migrate

|schritt| Optional: Views generieren
------------------------------------
Je nach Änderungen und Shop-Edition kann es sein, dass der Shop in den Wartungsmodus geht, solange die Views nicht neu generiert werden.

.. code:: bash

   vendor/bin/oe-eshop-db_views_generate

.. hint::

   Wird üblicherweise beim Update einer Enterprise Edition benötigt.

Damit ist das Update beendet.


.. Intern: oxbaix, Status:
