Setup per Kommandozeile
=======================

OXID eShop kann mit einem webbasierten Setup oder per Kommandozeile erstellt und konfiguriert werden. Dieses Dokument beschreibt das Setup per Kommandozeile.

Während der Installation werden bestimmte Werte in die :file:`.htaccess` und die :file:`config.inc.php` geschrieben. Beide Dateien befinden sich im Hauptverzeichnis des Shops und sollten für die Dauer des Setups nicht schreibgeschützt sein.

.. |schritt| image:: ../../media/icons/schritt.jpg
              :class: no-shadow

|schritt| Shop anlegen und konfigurieren
----------------------------------------
OXID eShop wird mit dem Kommando ``oe:setup:shop`` für OXID eShop console erstellt. Dabei werden die folgenden Parameter übergeben:

* ``--db-host=`` - Hostname oder IP-Adresse des Datenbank-Servers. Standard: ``localhost`` (Datenbank und Webserver auf gleichem Server)
* ``--db-port=`` - Port des Datenbank-Servers. Standard: 3306
* ``--db-name=`` - Name der Datenbank
* ``--db-user=`` - Datenbankbenutzer
* ``--db-password=`` - Passwort für den Datenbankbenutzer
* ``--shop-url`` - URL, über die der Shop erreichbar sein wird
* ``--shop-directory`` - interner Pfad zum Shop auf dem Server
* ``--compile-directory`` - Verzeichis für die temporären Dateien des Shops
* ``--language`` - Sprache für den Shop, Sprachkürzel nach ISO 639-1

Beispiel: Shop anlegen und konfigurieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code:: bash

   ./vendor/bin/oe-console oe:setup:shop --db-host=localhost --db-port=3306 --db-name=CE700 --db-user=root --db-password=oxid --shop-url=http://ce700.local --shop-directory=/var/www/oxideshop/source --compile-directory=/var/www/oxideshop/source/tmp --language=de

|schritt| Demodaten installieren
--------------------------------
Um dem Shop Demodaten hinzuzufügen, müssen diese zunächst per Composer aus dem der Shop-Edition entsprechenden GitHub-Repository bezogen werden. Anschließend werden die Demodaten mit dem Kommando ``oe:setup:demodata`` für OXID eShop console installiert.

Beispiel
^^^^^^^^

.. code:: bash

   composer config repositories.oxid-esales/oxideshop-demodata-ce vcs https://github.com/OXID-eSales/oxideshop_demodata_ce
   composer require oxid-esales/oxideshop-demodata-ce:v7.0.0

   vendor/bin/oe-console oe:setup:demodata

|schritt| Shop-Administrator anlegen
------------------------------------
Das Kommando ``oe:admin:create-user`` erstellt den Shop-Administrator und verwendet folgende Parameter:

* ``--admin-email=`` - E-Mail-Adresse des Shop-Administrators, Zugangsdaten für den Administrationsbereich
* ``--admin-password=`` - Passwort des Shop-Administrators, Zugangsdaten für den Administrationsbereich


Beispiel: Shop-Administrator anlegen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code:: bash

   ./vendor/bin/oe-console oe:admin:create-user --admin-email=max.mustermann@oxid-esales.com --admin-password=******

|schritt| Lizenz für PE/EE hinterlegen
--------------------------------------
OXID eShop Professional und Enterprise Edition benötigen für den produktiven Betrieb einen gültigen Lizenzschlüssel. Dieser kann mit dem Kommando ``oe:license:add`` für OXID eShop console hinzugefügt werden. Dabei wird der Lizenzschlüssel als Parameter übergeben.

.. code:: bash

   ./vendor/bin/oe-console oe:license:add <license-key>

Mit dem Kommando ``oe:license:clear`` können alle Lizenzschlüssel eines Shops gelöscht werden.

|schritt| Module installieren
-----------------------------
Module können mit dem Kommando ``oe:module:install`` der OXID eShop console installiert werden. Das Kommando ``oe:module:uninstall`` entfernt ein angegebenes Modul aus dem Shop. Alle Informationen dazu finden Sie in der englischsprachigen Entwicklerdokumentation: https://docs.oxid-esales.com/developer/en/7.0-rc.1/development/modules_components_themes/module/tutorials/module_setup.html und https://docs.oxid-esales.com/developer/en/7.0-rc.1/development/modules_components_themes/module/uninstall/index.html.


.. Intern: oxbaju, Status:
