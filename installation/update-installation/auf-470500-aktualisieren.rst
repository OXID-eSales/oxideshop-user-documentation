Auf 4.7.0/5.0.0 aktualisieren
=============================

Diese Anleitung beschreibt das Update auf OXID eShop Version 4.7.0 (Community und Professional Edition) und Version 5.0.0 (Enterprise Edition). Es unterscheidet sich grundlegend vom Standard-Update und kann nur auf einen OXID eShop Version 4.6.5, 4.6.6, 4.6.7 oder 4.6.8 angewandt werden. Haben Sie eine vorhergehende Shopversion im Einsatz, muss diese zuerst auf eine dieser Versionen aktualisiert werden.

Hinweis: Um das Update nach dieser Anleitung ausführen zu können, müssen OXID eShop 4.6.5 bis 4.6.8 und OXID eShop 4.7.0/5.0.0 auf dem gleichen Server installiert sein. Der OXID eShop 4.6.5 bis 4.6.8 ist der zu aktualisierende Shop. Beim OXID eShop 4.7.0/5.0.0 handelt es sich um eine komplette Neuinstallation.

Wir empfehlen dringend, das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, auszuführen. Testen Sie anschließend den Shop und legen Sie dabei besonderen Wert auf die Funktionen des Bestellprozesses, auf Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden. Alternativ können Sie das Update auch im Live-System erneut ausführen. Kopieren Sie während des Updates im Live-System eine index.html in das Hauptverzeichnis des Shops, in der Sie auf aktuelle Wartungsarbeiten hinweisen. Sie können den Shop auch deaktivieren und die Datei offline.html zur Informationen Ihrer Kunden nutzen.

Das Update kann unter Verwendung der Anwendung *updateApp*  ausgeführt werden. Dabei wird die Datenbank aktualisiert und es werden ein eigenes Theme und/oder installierte Module in den neuen Shop verschoben. Wenn Sie einen stark angepassten Shop haben und Theme und/oder Module selbst kopieren oder verschieben wollen, lesen Sie bitte den Abschnitt `Manuelles Update <#c13391>`_ .

Update per Script
-----------------

1. Sicherungskopien anfertigen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Erstellen Sie eine Sicherungskopie aller Shopdateien und der Datenbank Ihres bestehenden OXID eShop 4.6.5 bzw. 4.6.6.

2. Neuen Shop installieren
^^^^^^^^^^^^^^^^^^^^^^^^^^
Installieren Sie einen OXID eShop 4.7.0/5.0.0 auf dem gleichen Server, auf dem der OXID eShop 4.6.5 bzw. 4.6.6 läuft.

3. Alte Datenbank verbinden
^^^^^^^^^^^^^^^^^^^^^^^^^^^
Verbinden Sie den OXID eShop 4.7.0/5.0.0 mit der Datenbank des OXID eShop 4.6.5 bzw. 4.6.6. Editieren Sie dafür die Konfigurationsdateiconfig.inc.phpdes OXID eShop 4.7.0/5.0.0 und ändern Sie die Einträge für den Datenbanknamen, den Datenbankbenutzer und dessen Passwort.

4. updateApp ausführen
^^^^^^^^^^^^^^^^^^^^^^
Das Update-Paket enthält das Verzeichnis/updateAppmit einem kleinen Programm, welches die Datenbank bearbeitet sowie Theme und/oder Module in den neuen Shop verschiebt. Kopieren Sie das Verzeichnis/updateAppin das Hauptverzeichnis des installierten OXID eShop 4.7.0/5.0.0.

Rufen Sie in Ihrem Browserwww.ihreshopurl.de/updateAppauf. Ersetzen Sie dabeiwww.ihreshopurl.dedurch die URL Ihres OXID eShop 4.7.0/5.0.0. Das Programm fragt, ob es Theme und Module in den neuen Shop verschieben soll. Bejahen Sie diese Frage, müssen Sie den Pfad zum OXID eShop 4.6.5 bzw. 4.6.6 angeben. Sie finden den Pfad in der Konfigurationsdateiconfig.inc.phpdes OXID eShop 4.6.5 bzw. 4.6.6.

Bitte beachten Sie, dass Updates bei großen Datenbanken viel Zeit beanspruchen können. Setzen Sie den Parameter *max_execution_time*  in derphp.inider Test- oder Entwicklungsumgebung auf einen angemessenen Wert, um ein Timeout bei der Verarbeitung zu vermeiden. Löschen Sie das Verzeichnis/updateApp, wenn das Datenbank-Update fertig ist.

5. Views aktualisieren
^^^^^^^^^^^^^^^^^^^^^^
Gehen Sie im Administrationsbereich des OXID eShop 4.7.0/5.0.0 zuService-\>Toolsund aktualisieren Sie die Views. Falls Sie sich nicht im Administrationsbereich anmelden können, setzen Sie vorübergehend den Parameter *blSkipViewUsage*  in der Konfigurationsdateiconfig.inc.phpauf\"true\".

6. Artikelbilder kopieren
^^^^^^^^^^^^^^^^^^^^^^^^^
Kopieren Sie alle Artikelbilder aus dem OXID eShop 4.6.5 bzw. 4.6.6 in den OXID eShop 4.7.0/5.0.0. Diese befinden sich standardmäßig im Verzeichnis/out/pictures.

7. Templates anpassen
^^^^^^^^^^^^^^^^^^^^^
Passen Sie die Templates eines eigenen Themes an den OXID eShop 4.7.0/5.0.0 an. Die Template-Dokumentation befindet sich im Update-Paket und unterteilt sich in/templ_docu_application_views_admin,/templ_docu_application_views_azureund/templ_docu_out_azure. Theme\"Basic\"ist nicht mehr länger Bestandteil des Shops. Basiert Ihr eigenes Theme darauf, sollten Sie auf Theme\"Azure\"umstellen. Wie das Theme\"Basic\"weiter mit OXID eShop 4.7.0/5.0.0 verwendet werden kann, erklärt dieses englische Tutorial auf OXIDforge: `http://oxidforge.org/en/use-basic-theme-from-version-4-7-and-5-0-on.html <https://oxidforge.org/en/use-basic-theme-from-version-4-7-and-5-0-on.html>`_ .

8. Temporäre Dateien löschen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Löschen Sie alle Dateien und Ordner außer der.htaccessaus dem Verzeichnis/tmpdes Shops.

9. Theme und Module aktivieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Aktivieren Sie im Administrationsbereich ggf. das eigene Theme und/oder die Module.

----------

Manuelles Update
----------------

1. Sicherungskopien anfertigen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Erstellen Sie eine Sicherungskopie aller Shopdateien und der Datenbank Ihres bestehenden OXID eShop 4.6.5 bzw. 4.6.6.

2. Neuen Shop installieren
^^^^^^^^^^^^^^^^^^^^^^^^^^
Installieren Sie einen OXID eShop 4.7.0/5.0.0 auf dem gleichen Server, auf dem der OXID eShop 4.6.5 bzw. 4.6.6 läuft.

3. Alte Datenbank verbinden
^^^^^^^^^^^^^^^^^^^^^^^^^^^
Verbinden Sie den OXID eShop 4.7.0/5.0.0 mit der Datenbank des OXID eShop 4.6.5 bzw. 4.6.6. Editieren Sie dafür die Konfigurationsdateiconfig.inc.phpdes OXID eShop 4.7.0/5.0.0 und ändern Sie die Einträge für den Datenbanknamen, den Datenbankbenutzer und dessen Passwort.

4. Datenbank aktualisieren
^^^^^^^^^^^^^^^^^^^^^^^^^^
Führen Sie die SQL-Anweisungen aus der Datei49955.sqlaus. Verwenden Sie dafür beispielsweise die Eingabemöglichkeiten im Administrationsbereich des Shops unterService-\>Toolsoder Tools wie phpMyAdmin. Die Datei49955.sqlbefindet sich im Verzeichnis/updateApp/updates/sqldes Update-Paketes.

5. Views aktualisieren
^^^^^^^^^^^^^^^^^^^^^^
Gehen Sie im Administrationsbereich des OXID eShop 4.7.0/5.0.0 zuService-\>Toolsund aktualisieren Sie die Views.

6. Theme installieren
^^^^^^^^^^^^^^^^^^^^^
Soll ein eigenes Theme verwendet werden, führen Sie bitte nachfolgende Installationsschritte aus.

* Legen Sie Verzeichnisse für das Theme unter
* /out
* und
* /application/views
* an
* Kopieren Sie die Verzeichnisse mit den Sprachdateien, den Templates und die Metadata-Datei
* theme.php
* in das Verzeichnis
* /application/views/[theme]
* Kopieren Sie die Verzeichnisse mit den Stylesheet- und JavaScript-Dateien sowie Bilder des Themes nach
* /out/[theme]

7. Module installieren
^^^^^^^^^^^^^^^^^^^^^^
Stellen Sie sicher, dass die Module für die neue Shopversion vorbereitet sind.

* Kopieren Sie die Module in das Verzeichnis
* /modules

8. Artikelbilder kopieren
^^^^^^^^^^^^^^^^^^^^^^^^^
Kopieren Sie alle Artikelbilder aus dem OXID eShop 4.6.5 bzw. 4.6.6 in den OXID eShop 4.7.0/5.0.0. Diese befinden sich standardmäßig im Verzeichnis/out/pictures.

9. Templates anpassen
^^^^^^^^^^^^^^^^^^^^^
Passen Sie die Templates eines eigenen Themes an den OXID eShop 4.7.0/5.0.0 an.

10. Theme und Module aktivieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Aktivieren Sie im Administrationsbereich ggf. das eigene Theme und/oder die Module.

Das Update ist abgeschlossen. Tragen Sie die korrekte Shop-URL in die Konfigurationsdateiconfig.inc.phpdes OXID eShop 4.7.0/5.0.0 ein. Die Dateien des OXID eShop 4.6.5 bzw. 4.6.6 werden nicht mehr benötigt, sobald der aktualisierte Shop live geht. Auch die bei der Neuinstallation des OXID eShop 4.7.0/5.0.0 erstellte Datenbank kann gelöscht werden.

.. Intern: oxaace, Status: