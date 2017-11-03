Neu-Installation
================

In diesem Abschnitt erfahren Sie, wie Sie den OXID eShop 6 neu installieren. Es gibt dabei eine entscheidende Änderung gegenüber den Shopversionen 4 und 5: die Installation basiert nicht mehr auf Installationspaketen. Die für den Shop benötigten Dateien werden mit Hilfe von Composer, dem Dependency Manager für PHP, bereitgestellt. Danach kann wie gewohnt das webbasierte Setup ausgeführt und der Shop installiert werden.

.. image:: ../../media/screenshots-de/oxbaae01.png
   :alt: Setup, Schritt 1
   :height: 440
   :width: 600

Eine englischsprachige Anleitung zur Installation finden Sie in der Entwicklerdokumentation: `<https://docs.oxid-esales.com/developer/en/6.0/getting_started/eshop_installation.html>`_.

-----------------------------------------------------------------------------------------

Server und Systemvoraussetzungen
--------------------------------
**Inhalte**: Server, Shared Hosting, Managed Server, Serverfarm mit Loadbalancing und Datenbankcluster, Linux, Webserver, Apache 2.2 + 2.4, MySQL 5.5 + 5.7, PHP 5.6 + 7.0, Composer, OpenSSL |br|
:doc:`Artikel lesen <server-und-systemvoraussetzungen>` |link|

Installation vorbereiten
------------------------
**Inhalte**: Composer installieren, Shopdateien bereitstellen, Apache konfigurieren, Datei- und Verzeichnisrechte anpassen, Datenbank anlegen |br|
:doc:`Artikel lesen <installation-vorbereiten>` |link|

Setup ausführen
---------------
**Inhalte**: Webbasiertes Setup, Prüfung der Systemvoraussetzungen, Region, Hauptlieferland und Sprache des Shops wählen, Lizenzbedingungen, Datenbank, Datenbankname, Datenbankbenutzer und -passwort angeben, Demodaten, Shopverzeichnisse, Zugangsdaten für Administrationsbereich festlegen, Shop-Administrator, Lizenzschlüssel eingeben (PE und EE) |br|
:doc:`Artikel lesen <setup-ausfuehren>` |link|

Installation abschließen
------------------------
**Inhalte**: Löschen des Setup-Verzeichnisses kontrollieren, Datei- und Verzeichnisrechte setzen, Schreibrechte für /out/pictures, /out/media, /log, /export, /tmp, Schreibschutz für .htaccess, config.inc.php  |br|
:doc:`Artikel lesen <installation-abschliessen>` |link|

.. Intern: oxbaae, Status: