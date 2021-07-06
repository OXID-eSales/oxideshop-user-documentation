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

Beispiel
^^^^^^^^

.. code:: bash

   bin/oe-console oe:setup:shop --db-host=localhost --db-port=3306 --db-name=CE700 --db-user=root --db-password=oxid --shop-url=http://ce700.local --shop-directory=/var/www/oxideshop/source --compile-directory=/var/www/oxideshop/source/tmp --language=de

|schritt| Shop-Administrator anlegen
------------------------------------
Das Kommando ``oe:admin:create-user`` erstellt einen Shop-Administrator und verwendet folgende Parameter:

* ``--admin-email=`` - E-Mail-Adresse des Shop-Administrators, Zugangsdaten für den Administrationsbereich
* ``--admin-password=`` - Passwort des Shop-Administrators, Zugangsdaten für den Administrationsbereich
* ``admin_rights`` - Administratorrechte in einer Enterprise Edition (optionaler Parameter) |br|
  ``malladmin`` - Administrator des Shops und aller Subshops (Default) |br|
  ``admin_rights`` - Administrator eines spezifischen Subshops
* ``admin_shopid`` - ID dieses spezifischen Subshops (optionaler Parameter, Default ist 1)

Beispiel
^^^^^^^^

.. code:: bash

   bin/oe-console oe:admin:create-user --admin-email=max.mustermann@oxid-esales.com --admin-password=******

-----------------------------------------------------------------------------------------

Available commands in 6.3.0:
  help                               Displays help for a command
  list                               Lists commands
oe
  oe:module:activate                 Activates a module.
  oe:module:apply-configuration      Applies configuration for installed modules.
  oe:module:deactivate               Deactivates a module.
  oe:module:install-configuration    Install module configuration into project configuration file.Module configuration already present in the project configuration file will be overwritten.
  oe:module:uninstall-configuration  Uninstall module configuration from project configuration file.


.. Intern: oxba, Status: