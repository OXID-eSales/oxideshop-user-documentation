Installation vorbereiten
========================

Für die Neu-Installation des OXID eShop 6.2 sind einige Vorbereitungen notwendig.

.. |schritt| image:: ../../media/icons/schritt.jpg
              :class: no-shadow

|schritt| Composer installieren
-------------------------------

Die Installation des OXID eShop 6 basiert nicht mehr auf gepackten und herunterladbaren Installationspaketen, sondern wird mit Hilfe von Composer ausgeführt. Composer ist ein Dependency Manager für PHP, ein Tool, welches Abhängigkeiten von Programmbestandteilen eines Projektes berücksichtigt, während es die Dateien dieses Projekts in ein definiertes Verzeichnis installiert.

Für die Neu-Installation des OXID eShop wird Composer benötigt. Eine Anleitung zur Installation finden Sie im Abschnitt "Getting Started" der Composer-Seiten: http://getcomposer.org.

|schritt| Shopdateien bereitstellen
-----------------------------------

Die Shopdateien werden durch Composer bereitgestellt. Abhängig von der Shop-Edition müssen dafür unterschiedliche Kommandos in der Shell ausgeführt werden. Die Shopdateien werden in einem Unterverzeichnis gespeichert, welches im Kommando mit :command:`your_project_name` angegeben wird. Dabei wird von dem Verzeichnis ausgegangen, in dem das Kommando in der Shell abgesetzt wird. Der Parameter :command:`--no-dev` wird angegeben, wenn die entwicklungsbezogenen Dateien nicht benötigt werden.

.. hint:: Für die Installation der Professional und Enterprise Edition benötigen Sie zusätzlich die Zugangsdaten, die Sie mit der E-Mail zum aktuellen Release erhalten haben.

Community Edition
^^^^^^^^^^^^^^^^^

:command:`composer create-project --no-dev oxid-esales/oxideshop-project your_project_name dev-b-6.2-ce`

Professional Edition
^^^^^^^^^^^^^^^^^^^^

:command:`composer create-project --no-dev oxid-esales/oxideshop-project your_project_name dev-b-6.2-pe`

Enterprise Edition
^^^^^^^^^^^^^^^^^^

:command:`composer create-project --no-dev oxid-esales/oxideshop-project your_project_name dev-b-6.2-ee`

Nachdem Composer seine Arbeit beendet hat, existiert das mit *your_project_name* benannte neue Verzeichnis. Dieses ist das Hauptverzeichnis (Root) des Projektes und enthält alle Dateien, die für die Installation des OXID eShop benötigt werden.

|schritt| Apache konfigurieren
------------------------------

Das Hauptverzeichnis muss nun in ein Verzeichnis verschoben werden, auf das der HTTP-Server zugreifen kann. Das Document Root-Verzeichnis des Apache muss auf das Verzeichnis :file:`/source` des Hauptverzeichnisses verweisen.

|schritt| Datei- und Verzeichnisrechte anpassen
-----------------------------------------------

Der HTTP-Server benötigt zur Laufzeit Lese- und Schreibzugriff für folgende Verzeichnisse und ihre Unterverzeichnisse:

:file:`/source/export` |br|
:file:`/source/log/` |br|
:file:`/source/out/pictures/` |br|
:file:`/source/out/media/` |br|
:file:`/source/tmp/` |br|
:file:`/var/`

Zusätzlich benötigt auch der CLI-Benutzer (Command Line Interface) Lese- und Schreibzugriff für das Verzeichnis :file:`/var/`.

Für das webbasierte Setup muss der HTTP-Server auf folgendes Verzeichnis und diese Dateien schreibend zugreifen können:

:file:`/source/Setup` |br|
:file:`/source/config.inc.php` |br|
:file:`/source/.htaccess`

|schritt| Datenbank anlegen
---------------------------

OXID eShop benötigt eine MySQL-Datenbank, um darin alle Artikel, Kategorien, Kunden- und Bestelldaten sowie weitere Informationen speichern zu können. Die meisten Webhoster bieten Datenbankzugriff über eine spezielle Website, wie beispielsweise phpMyAdmin an. Wenn Sie dabei Hilfe benötigen, wenden Sie sich bitte an Ihren OXID Hosting Partner oder Internet Service Provider (ISP).

Legen Sie jetzt eine neue MySQL-Datenbank an. Der Name der Datenbank ist frei wählbar und könnte beispielsweise :db:`oxid_eshop` lauten. Merken Sie sich den Namen der Datenbank und die vergebenen Zugangsdaten zur Datenbank (Benutzername und Passwort). Diese Daten werden benötigt, wenn Sie das Setup ausführen.


.. Intern: oxbaad, Status: