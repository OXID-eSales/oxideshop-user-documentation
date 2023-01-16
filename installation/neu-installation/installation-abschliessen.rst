Installation abschließen
========================

Setup-Verzeichnis
-----------------
Nach erfolgreicher Installation wird das Verzeichnis :file:`/setup` automatisch gelöscht.

Damit soll verhindert werden, dass das Setup zu einem späteren Zeitpunkt erneut aufgerufen werden kann.

Kontrollieren Sie, ob das Löschen des Verzeichnisses erfolgreich war.

Datei- und Verzeichnisrechte
----------------------------
Für einen fehlerfreien Betrieb benötigt der Shop Schreibrechte für einige Verzeichnisse (Dateirechte auf 777 oder 775).

Stellen Sie sicher, dass die Schreibrechte für die Verzeichnisse :file:`/source/out/pictures`, :file:`/source/out/media`, :file:`/source/log`, :file:`/source/export`, :file:`/source/tmp` und :file:`/var` gesetzt sind, ggf. auch rekursiv in alle Unterverzeichnisse.

Die Dateien :file:`.htaccess` und :file:`config.inc.php` aus dem Hauptverzeichnis müssen nach abgeschlossenem Setup schreibgeschützt sein (Dateirechte auf 444).


.. Intern: oxbaag, Status: