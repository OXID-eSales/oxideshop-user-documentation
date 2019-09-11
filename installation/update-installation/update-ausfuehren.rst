Update ausführen
================

1. Sicherungskopien anfertigen
------------------------------

Erstellen Sie eine Sicherungskopie aller Shopdateien und von der Datenbank.

2. Dateien kopieren
-------------------

Kopieren Sie alle Dateien aus dem Verzeichnis :file:`/copy_this` in das Hauptverzeichnis Ihres Shops. Das Hauptverzeichnis ist das Verzeichnis, in dem sich die Datei :file:`config.inc.php` befindet.

3. Module deaktivieren
----------------------

Alle im Shop aktiven Module sollten während des Updates deaktiviert sein. Gehen Sie dafür im Administrationsbereich zu :menuselection:`Erweiterungen --> Module`. Wählen Sie nacheinander alle aufgelisteten und aktiven Module und betätigen Sie die Schaltfläche :guilabel:`Deaktivieren` auf der Registerkarte :guilabel:`Stamm`.

4. Datenbank updaten
--------------------

Das Update-Paket enthält das Verzeichnis :file:`/updateApp` mit einem kleinen Programm, welches die Datenbank-Updates durchführt. Kopieren Sie das Verzeichnis :file:`/updateApp` in das Hauptverzeichnis Ihres Shops. Sie können das Programm entweder per Kommandozeile oder mit dem Browser aufrufen.

4.1 Aufruf per Kommandozeile
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Wechseln Sie auf der Konsole in das Verzeichnis :file:`/updateApp` und führen Sie den Befehl :command:`php run_cli.php` aus.

4.2 Aufruf mit dem Browser
^^^^^^^^^^^^^^^^^^^^^^^^^^
Rufen Sie mit Ihrem Browser ``www.ihreshopurl.de/updateApp`` auf. Ersetzen Sie dabei ``www.ihreshopurl.de`` durch die URL Ihres Shops.

Bitte beachten Sie, dass größere Updates bei großen Datenbanken viel Zeit beanspruchen können. Das Datenbank-Update kann dann bis zu mehreren Stunden dauern. Löschen Sie das Verzeichnis :file:`/updateApp`, wenn das Datenbank-Update fertig ist!

5. Temporäre Dateien löschen und Views aktualisieren
----------------------------------------------------

Löschen Sie alle Dateien und Ordner außer der :file:`.htaccess` aus dem Verzeichnis :file:`/tmp` des Shops. Wurden im Shop Änderungen an der Datenbank vorgenommen (meistens bei einem Major Release), müssen die Views aktualisiert werden. Gehen Sie dafür im Administrationsbereich des OXID eShop zu :menuselection:`Service --> Tools` und klicken Sie auf die Schaltfläche :guilabel:`VIEWS jetzt updaten`.

6. Templates anpassen
---------------------

Das Verzeichnis :file:`/changed_full` enthält Templates und weitere Dateien des Shops. Sollten Sie einen Shop ohne angepasste Templates und Dateien aktualisieren, so können Sie die Dateien aus dem Verzeichnis :file:`/tpl` direkt in den Shop kopieren.

Wurden Templates und Dateien geändert, müssen die Änderungen in die im eShop vorhandenen Dateien übernommen werden. In diesem Fall ist es notwendig, für jede Datei aus dem Verzeichnis :file:`/changed_full` zu entscheiden, ob sie direkt kopiert werden kann oder ob die vorhandene Datei angepasst werden muss. Vererbte Templates aus einem benutzerdefinierten Theme (Custom) müssen gegebenenfalls auch geändert werden.

Änderungen an den Templates sind in den Verzeichnissen :file:`/templ_docu_admin` und :file:`/templ_docu_flow` bzw. :file:`/templ_docu_azure` dokumentiert. Ist einer dieser Ordner nicht vorhanden, gab es keine Änderungen für Dateien des Administrationsbereichs oder des Themes. Haben sich Sprachdateien, die :file:`.htaccess`, die :file:`config.inc.php` oder andere Dateien geändert, ermitteln Sie diese Änderungen am besten mit einem Dateivergleich.

Falls Sie nicht wissen, ob die Dateien in Ihrem eShop angepasst sind, gehen Sie wie folgt vor:

* Laden Sie sich aus OXID eXchange das Prüfscript :file:`oxchkversion.php`. |br|
  `Oxchkversion für Enterprise und Professional Edition <http://exchange.oxid-esales.com/de/en/OXID-Produkte/Weitere-OXID-Extensions/Oxchkversion-3-2-1-Stable-EE-PE-4-0-x-4-9-x-5-2-x.html>`_ |br|
  `Oxchkversion für Community Edition <http://exchange.oxid-esales.com/de/en/OXID-Produkte/Weitere-OXID-Extensions/Oxchkversion-CE-3-2-1-Stable-CE-4-7-x-4-9-x.html>`_
* Kopieren Sie die Datei :file:`oxchkversion.php` in das Hauptverzeichnis Ihres Shops.
* Rufen Sie in Ihrem Browser ``http://www.ihreshop.de/oxchkversion.php`` auf.
* Ersetzen Sie dabei ``www.ihreshop.de`` durch die URL Ihres eShop.

Das Prüfscript teilt Ihnen mit, ob und an welcher Stelle der Shop nicht dem Originalzustand entspricht. Löschen Sie die Datei nach abgeschlossener Prüfung.

.. hint:: Seit OXID eShop 4.8.0/5.1.0 ist diese Prüfung in den Administrationsbereich des Shops integriert. Sie können es später jederzeit unter :menuselection:`Service --> Diagnosewerkzeug` aufrufen.

---------------------------------------------------------------------------------------------------

Probleme mit der PDF-Rechnung
-----------------------------

Ab OXID eShop Version 4.8.0 wird das Modul für die PDF-Rechnung in das Verzeichnis :file:`/modules/oe/invoicepdf` installiert. Da aber das bisherige Verzeichnis :file:`/modules/invoicepdf` bei einem Update von 4.7.* nicht gelöscht wird, funktioniert das Erstellen von Rechnungen nicht.

Bitte löschen Sie das Verzeichnis :file:`/modules/invoicepdf` manuell. Gehen Sie anschließend im Administrationsbereich des Shops zur Modulverwaltung. Sie erhalten einen Hinweis, dass für ein registriertes Modul das Modulverzeichnis fehlt. Beantworten Sie die Frage, ob alle Modulinformationen entfernt werden sollen, indem Sie die Schaltfläche :guilabel:`Ja` drücken.


.. Intern: oxaaaj, Status: