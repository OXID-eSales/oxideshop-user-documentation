Update ausführen
****************
1. Sicherungskopien anfertigen
++++++++++++++++++++++++++++++
Erstellen Sie eine Sicherungskopie aller Shopdateien und von der Datenbank.

2. Dateien kopieren
+++++++++++++++++++
Kopieren Sie alle Dateien aus dem Verzeichnis/copy_thisin das Hauptverzeichnis Ihres Shops. Das Hauptverzeichnis ist das Verzeichnis, in dem sich die Dateiconfig.inc.phpbefindet.

3. Module deaktivieren
++++++++++++++++++++++
Alle im Shop aktiven Module sollten während des Updates deaktiviert sein. Gehen Sie dafür im Administrationsbereich zuErweiterungen-\>Module. Wählen Sie nacheinander alle aufgelisteten und aktiven Module und betätigen Sie die SchaltflächeDeaktivierenauf der RegisterkarteStamm.

4. Datenbank updaten
++++++++++++++++++++
Das Update-Paket enthält das Verzeichnis/updateAppmit einem kleinen Programm, welches die Datenbank-Updates durchführt. Kopieren Sie das Verzeichnis/updateAppin das Hauptverzeichnis Ihres Shops. Sie können das Programm entweder per Kommandozeile oder mit dem Browser aufrufen.

4.1 Aufruf per Kommandozeile
++++++++++++++++++++++++++++
Wechseln Sie auf der Konsole in das Verzeichnis/updateAppund führen Sie den Befehlphp run_cli.phpaus.

4.2 Aufruf mit dem Browser
++++++++++++++++++++++++++
Rufen Sie mit Ihrem Browser\www.ihreshopurl.de/updateAppauf. Ersetzen Sie dabeiwww.ihreshopurl.dedurch die URL Ihres Shops.

Bitte beachten Sie, dass größere Updates bei großen Datenbanken viel Zeit beanspruchen können. Das Datenbank-Update kann dann bis zu mehreren Stunden dauern. Löschen Sie das Verzeichnis/updateApp, wenn das Datenbank-Update fertig ist!

5. Temporäre Dateien löschen und Views aktualisieren
++++++++++++++++++++++++++++++++++++++++++++++++++++
Löschen Sie alle Dateien und Ordner außer der.htaccessaus dem Verzeichnis/tmpdes Shops. Wurden im Shop Änderungen an der Datenbank vorgenommen (meistens bei einem Major Release), müssen die Views aktualisiert werden. Gehen Sie dafür im Administrationsbereich des OXID eShop zuService-\>Toolsund klicken Sie auf die SchaltflächeVIEWS jetzt updaten.

6. Templates anpassen
+++++++++++++++++++++
Das Verzeichnis/changed_fullenthält Templates und weitere Dateien des Shops. Sollten Sie einen Shop ohne angepasste Templates und Dateien aktualisieren, so können Sie die Dateien aus dem Verzeichnis/tpldirekt in den Shop kopieren.

Wurden Templates und Dateien geändert, müssen die Änderungen in die im eShop vorhandenen Dateien übernommen werden. In diesem Fall ist es notwendig, für jede Datei aus dem Verzeichnis/changed_fullzu entscheiden, ob sie direkt kopiert werden kann oder ob die vorhandene Datei angepasst werden muss. Vererbte Templates aus einem benutzerdefinierten Theme (Custom) müssen gegebenenfalls auch geändert werden.

Änderungen an den Templates sind in den Verzeichnissen/templ_docu_adminund/templ_docu_azuredokumentiert. Ist einer dieser Ordner nicht vorhanden, gab es keine Änderungen für Dateien des Administrationsbereichs oder des Themes. Haben sich Sprachdateien, die.htaccess, dieconfig.inc.phpoder andere Dateien geändert, ermitteln Sie diese Änderungen am besten mit einem Dateivergleich.

Falls Sie nicht wissen, ob die Dateien in Ihrem eShop angepasst sind, gehen Sie wie folgt vor:

* Laden Sie sich aus OXID eXchange das Prüfscript oxchkversion.php.

*  `Oxchkversion für Enterprise und Professional Edition <http://exchange.oxid-esales.com/de/en/OXID-Produkte/Weitere-OXID-Extensions/Oxchkversion-3-2-1-Stable-EE-PE-4-0-x-4-9-x-5-2-x.html>`_
*
*  `Oxchkversion für Community Edition <http://exchange.oxid-esales.com/de/en/OXID-Produkte/Weitere-OXID-Extensions/Oxchkversion-CE-3-2-1-Stable-CE-4-7-x-4-9-x.html>`_
* \
* Kopieren Sie die Datei
* oxchkversion.php
* in das Hauptverzeichnis Ihres Shops.
* Rufen Sie in Ihrem Browser
* http://www.ihreshop.de/oxchkversion.php
* auf.

* Ersetzen Sie dabei
* www.ihreshop.de
* durch die URL Ihres eShop.

Das Prüfscript teilt Ihnen mit, ob und an welcher Stelle der Shop nicht dem Originalzustand entspricht. Löschen Sie die Datei nach abgeschlossener Prüfung.

Hinweis: Seit OXID eShop 4.8.0/5.1.0 ist diese Prüfung in den Administrationsbereich des Shops integriert. Sie können es später jederzeit unter Service-\>Diagnosewerkzeug aufrufen.

.. Intern: oxaaaj, Status: