Von 6.1.x auf 6.2.0 aktualisieren
=================================

Dieses Dokument beschreibt das Update von OXID eShop 6.1.0 und höher auf OXID eShop 6.2.0. Es unterscheidet sich vor allem durch die Übernahme der Modulkonfigurationen aus der Datenbank von einem Standard-Update.

.. |schritt| image:: ../../media/icons/schritt.jpg
              :class: no-shadow

Aktualisierung des Shops
------------------------
|schritt| In der Datei :file:`composer.json`, die sich im Hauptverzeichnis des Shops befindet, müssen Version geändert werden. Das betrifft die Sektion "require" und falls benötigt "require-dev". Beispiel für einen OXID eShop Community Edition 6.2.0:

.. code:: json

   "require": {
      "oxid-esales/oxideshop-metapackage-ce": "v6.2.0"
   },
   "require-dev": {
      "oxid-esales/testing-library": "^v7.0.1",
      "incenteev/composer-parameter-handler": "^v2.0.0",
      "oxid-esales/oxideshop-ide-helper": "^v3.1.2",
      "oxid-esales/azure-theme": "^v1.4.2"
   },

Sie finden die Werte für Ihre Shop-Edition im jeweiligen Repository des OXID eShop Projektes:

* Community Edition: https://github.com/OXID-eSales/oxideshop_project/blob/b-6.2-ce/composer.json
* Professional Edition: https://github.com/OXID-eSales/oxideshop_project/blob/b-6.2-pe/composer.json
* Enterprise Edition: https://github.com/OXID-eSales/oxideshop_project/blob/b-6.2-ee/composer.json

|schritt| Leeren Sie das Verzeichnis mit den temporären Dateien des Shops, indem Sie beispielsweise eine Shell im Hauptverzeichnis des Shops aufrufen und folgendes Kommando eingeben:

.. code:: bash

   rm -rf source/tmp/*

|schritt| Führen Sie in der Shell den nachstehenden Composer-Befehl aus, um die Abhängigkeiten zu aktualisieren. Der Parameter :command:`--no-dev` wird angegeben, wenn die entwicklungsbezogenen Dateien nicht benötigt werden.

.. code:: bash

   composer update --no-plugins --no-scripts --no-dev

|schritt| Kopieren Sie nun die Datei :file:`overridablefunctions.php` vom Verzeichnis :file:`/vendor` des Shops in das Verzeichnis :file:`/source`.

.. code:: bash

    cp vendor/oxid-esales/oxideshop-ce/source/overridablefunctions.php source/

|schritt| Mit einem zweiten Composer-Befehl werden alle Scripts ausgeführt, um die neue Compilation zu beziehen. Für Shopdateien, Themes und Module muss jeweils bestätigt werden, dass das Update bestehende Dateien überschreibt. Haben Sie eigene Module mit ``"type": "path"`` in Ihre Datei :file:`composer.json` eingebunden, beantworten Sie die Nachfrage zum Überschreiben bitte mit Nein.

.. code:: bash

   composer update --no-dev

|schritt| Der dritte und letzte Composer-Befehl führt die Migration der Datenbank aus.

.. code:: bash

   vendor/bin/oe-eshop-db_migrate migrations:migrate

---------------------------------------------------------------------------------------------------

Aktualisierung der Modulkonfigurationen
---------------------------------------
In diesem Arbeitsschritt werden Einstellungen und Aktivierungsstatus der zum Shop gehörenden Module aus der Datenbank in Konfigurationsdateien :file:`*.yml` transferiert.

|schritt| Mit dem nachfolgenden Composer-Kommando, welches im Hauptverzeichnis des Shops aufgerufen wird, installieren Sie die OXID eShop update component.

.. code:: bash

   composer require --no-interaction oxid-esales/oxideshop-update-component

|schritt| Für alle Module, die sich im Verzeichnis :file:`source/modules` befinden, wird eine Standardkonfiguration erstellt. Dafür wird die neue OXID eShop Console mit folgendem Kommando aufgerufen:

.. code:: bash

   vendor/bin/oe-console oe:oxideshop-update-component:install-all-modules

|schritt| Die vorhandenen Moduldaten (Moduleinstellungen, Klassenerweiterungsketten, Aktivierungsstatus) werden aus der Datenbank in die Konfigurationsdateien :file:`*.yml` übertragen.

.. code:: bash

   vendor/bin/oe-console oe:oxideshop-update-component:transfer-module-data

Nach diesem Arbeitsschritt sollte in der Konfigurationsdatei aller zuvor aktiven Module die Option `configured = true` sein. Die Konfigurationsdatei enthält jetzt auch die Moduleinstellungen. Es sind die selben, die im Administrationsbereich beim Modul festgelegt wurden.

|schritt| Um Datenredundanz und Probleme bei der Aktivierung von Modulen zu vermeiden, werden deren Status und Einstellungen aus der Datenbank entfernt.

.. code:: bash

   vendor/bin/oe-console oe:oxideshop-update-component:delete-module-data-from-database

|schritt| Alle Module, die zuvor aktiv waren, werden aktiviert und die Moduleinstellungen wiederhergestellt.

.. code:: bash

   vendor/bin/oe-console oe:module:apply-configuration

|schritt| Deinstallieren Sie die OXID eShop update component.

.. code:: bash

   composer remove oxid-esales/oxideshop-update-component

---------------------------------------------------------------------------------------------------

Alte Dateien entfernen
----------------------
|schritt| Die Datei :file:`xd_reciever.htm` aus dem Verzeichnis :file:`/source` wird nicht mehr benötigt und sollte gelöscht werden.

---------------------------------------------------------------------------------------------------

Fehlersuche und -behebung
-------------------------
Hinweise auf mögliche Probleme bei der Übernahme von Status und Einstellungen der Module finden sich im Dokument `Update from 6.1.x to 6.2.0 <https://docs.oxid-esales.com/developer/en/6.2/update/#troubleshooting>`_ der
englischsprachigen Entwicklerdokumentation.


.. Intern: oxbaiy, Status: