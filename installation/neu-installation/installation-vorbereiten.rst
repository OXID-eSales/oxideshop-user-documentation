Installation vorbereiten
========================

Für die Neu-Installation des OXID eShop 7.0 sind einige Vorbereitungen notwendig.

.. |schritt| image:: ../../media/icons/schritt.jpg
              :class: no-shadow

|schritt| Composer installieren
-------------------------------

Die Installation des OXID eShop 7 basiert nicht mehr auf gepackten und herunterladbaren Installationspaketen, sondern wird mit Hilfe von Composer ausgeführt. Composer ist ein Dependency Manager für PHP, ein Tool, welches Abhängigkeiten von Programmbestandteilen eines Projektes berücksichtigt, während es die Dateien dieses Projekts in ein definiertes Verzeichnis installiert.

Für die Neu-Installation des OXID eShop brauchen Sie Composer. Siehe unter :ref:`installation/neu-installation/server-und-systemvoraussetzungen:Server und Systemvoraussetzungen` Abschnitt :ref:`installation/neu-installation/server-und-systemvoraussetzungen:Composer`.

Eine Anleitung zur Installation finden Sie im Abschnitt "Getting Started" der Composer-Seiten unter: http://getcomposer.org.

|schritt| Shop-Dateien bereitstellen
------------------------------------

Die Shop-Dateien werden durch Composer bereitgestellt. Abhängig von der Shop-Edition müssen dafür unterschiedliche Kommandos in der Shell ausgeführt werden. Die Shop-Dateien werden in einem Unterverzeichnis gespeichert, welches im Kommando mit :command:`your_project_name` angegeben wird. Dabei wird von dem Verzeichnis ausgegangen, in dem der Befehl in der Shell abgesetzt wird. Der Parameter :command:`--no-dev` wird angegeben, wenn die entwicklungsbezogenen Dateien nicht benötigt werden.

.. hint:: Für die Installation der Professional und Enterprise Edition benötigen Sie zusätzlich die Zugangsdaten, die Sie mit der E-Mail zum aktuellen Release erhalten haben.

Community Edition
^^^^^^^^^^^^^^^^^

:command:`composer create-project --no-dev oxid-esales/oxideshop-project your_project_name dev-b-7.0-ce`

Professional Edition
^^^^^^^^^^^^^^^^^^^^

:command:`composer create-project --no-dev oxid-esales/oxideshop-project your_project_name dev-b-7.0-pe`

Enterprise Edition
^^^^^^^^^^^^^^^^^^

:command:`composer create-project --no-dev oxid-esales/oxideshop-project your_project_name dev-b-7.0-ee`

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

OXID eShop benötigt eine MySQL-Datenbank, um darin Artikel, Kategorien, Kunden- und Bestelldaten sowie weitere
Informationen zu speichern.

Die meisten Webhoster bieten Datenbankzugriff über eine spezielle Website,
wie beispielsweise phpMyAdmin an. Wenn Sie dabei Hilfe benötigen, wenden Sie sich bitte an Ihren
OXID Hosting Partner oder Internet Service Provider (ISP).


Sie haben folgenden Möglichkeiten:

* Empfohlen: Legen Sie eine neue MySQL-Datenbank an. Den Namen der Datenbank können Sie frei wählen, beispielsweise :db:`oxid_eshop`.

 Merken Sie sich den Namen der Datenbank und die Zugangsdaten zur Datenbank (Benutzername und Passwort).

 Diese Daten benötigen Sie, um nach dem Installieren das Setup ausführen.

* Alternativ: Legen Sie die Datenbank während des Setup an.


.. Intern: oxbaad, Status: