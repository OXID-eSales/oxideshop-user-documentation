Installation prüfen
===================

Setup-Verzeichnis
-----------------

Nach erfolgreicher Installation wird das Verzeichnis :file:`/setup` automatisch gelöscht. Damit soll verhindert werden, dass das Setup zu einem späteren Zeitpunkt erneut aufgerufen werden kann. Kontrollieren Sie, ob das Löschen des Verzeichnisses erfolgreich war.

Datei- und Verzeichnisrechte
----------------------------

Für einen fehlerfreien Betrieb benötigt der Shop Schreibrechte für einige Verzeichnisse (Dateirechte auf 777 oder 775). Bitte stellen Sie sicher, dass die Schreibrechte für die Verzeichnisse :file:`/out/pictures`, :file:`/log`, :file:`/tmp` und :file:`/export` gesetzt sind, ggf. auch rekursiv in alle Unterverzeichnisse.

Die Dateien :file:`.htaccess` und :file:`config.inc.php` aus dem Hauptverzeichnis müssen nach abgeschlossenem Setup schreibgeschützt sein (Dateirechte auf 444).

Prüfscript oxchkversion.php
---------------------------

:file:`oxchkversion.php` ist ein Script zum Überprüfen der Konsistenz Ihres OXID eShop. Damit werden alle .php-Dateien und Templates geprüft, indem deren MD5-Checksumme über einen Webservice mit den in einer Datenbank gespeicherten Werten verglichen wird. So kann sichergestellt werden, dass alle Shopdateien mit dem FTP-Programm korrekt auf den Webserver kopiert wurden.

Das Prüfscript kann im OXID eXchange kostenfrei heruntergeladen werden:

* `Oxchkversion für Enterprise und Professional Edition <http://exchange.oxid-esales.com/de/en/OXID-Produkte/Weitere-OXID-Extensions/Oxchkversion-3-2-1-Stable-EE-PE-4-0-x-4-9-x-5-2-x.html>`_
* `Oxchkversion für Community Edition <http://exchange.oxid-esales.com/de/en/OXID-Produkte/Weitere-OXID-Extensions/Oxchkversion-CE-3-2-1-Stable-CE-4-7-x-4-9-x.html>`_

 Seit der Veröffentlichung des OXID eShop 4.8.0/5.1.0 im Oktober 2013 ist das Prüfscript auch in das Diagnosewerkzeug integriert, welches im Administrationsbereich des Shops aufgerufen werden kann.

.. Intern: oxaaag, Status: