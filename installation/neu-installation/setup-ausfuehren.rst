Setup ausführen
===============

Um Ihren OXID eShop startbereit zu machen, führen Sie das Setup entweder webbasiert oder per Kommandozeile aus.

Im folgende beschreiben wir das webbasierte Setup.

Alternativ können Sie das Setup per Kommandozeile ausführen. Weitere Informationen finden Sie unter :ref:`installation/neu-installation/setup-kommandozeile:Setup per Kommandozeile`.


.. |schritt| image:: ../../media/icons/schritt.jpg
              :class: no-shadow

|schritt| Setup starten
-----------------------

Stellen Sie sicher, dass während des Setup Konfigurationsparameter geschrieben werden können, und starten Sie das Setup.


1. Öffnen Sie eine Shell und wechseln Sie ins Verzeichnis des Shops.

   .. code:: bash

      cd /var/www/oxideshop/source

2. Stellen Sie sicher, dass folgende Dateien nicht schreibgeschützt sind:

   * :file:`.htaccess`
   * :file:`config.inc.php`

3. Öffnen Sie einen Browser und rufen Sie ``www.ihreshopurl.de/setup`` auf.

   Ersetzen Sie dabei ``www.ihreshopurl.de`` durch die URL, unter der ihr OXID eShop erreichbar sein wird.

   Das Setup startet.

|schritt| Voraussetzungen
-------------------------

Farbige Symbole zeigen an, ob die Systemvoraussetzungen erfüllt sind:

.. |install-pass| image:: ../../media/icons/install-pass.png
                   :class: no-shadow
.. |install-pmin| image:: ../../media/icons/install-pmin.png
                   :class: no-shadow
.. |install-fail| image:: ../../media/icons/install-fail.png
                   :class: no-shadow
.. |install-null| image:: ../../media/icons/install-null.png
                   :class: no-shadow

* |install-pass| Die Voraussetzung ist erfüllt.
* |install-pmin| Die Voraussetzung ist nicht oder nur teilweise erfüllt. Der OXID eShop funktioniert trotzdem und kann installiert werden.
* |install-fail| Die Voraussetzung ist nicht erfüllt. Der OXID eShop funktioniert nicht ohne diese Voraussetzung und kann nicht installiert werden.
* |install-null| Die Voraussetzung konnte nicht geprüft werden.

1. Wählen Sie die Sprache für die Installation.
2. Stellen Sie sicher, dass alle Systemvoraussetzungen erfüllt sind, um den OXID eShop installieren und störungsfrei betreiben zu können.
   Bei Konfigurationsproblemen wenden Sie sich an Ihren OXID Hosting Partner oder Internet Service Provider (ISP).
3. Sobald alle Systemvoraussetzungen erfüllt sind (es sind keine roten Markierungen vorhanden), betätigen Sie die Schaltfläche :guilabel:`Setup beginnen`.

|schritt| Willkommen
--------------------

1. Legen Sie Hauptlieferland und Sprache des Shops fest.
   Sie können weitere Lieferländer und/oder Sprachen später jederzeit hinzufügen.
2. Empfohlen: Aktivieren Sie das Kontrollkästchen für die regelmäßige Prüfung auf Aktualisierungen.
3. Optional: Bei der Installation einer Community Edition bestätigen Sie die Verbindung zu den OXID Servern zur Verbesserung der Produktqualität.
4. Wählen Sie die Schaltfläche :guilabel:`Shopinstallation beginnen`.

|schritt| Lizenzbedingungen
---------------------------
Prüfen Sie die Lizenzbedingungen und akzeptieren Sie sie.

|schritt| Datenbank
-------------------

Erstellen Sie eine Datenbank oder binden Sie eine bestehende Datenbank ein.

:guilabel:`Datenbank Hostname oder IP Adresse`

   Sie haben folgende Möglichkeiten:

   * Wenn sich Datenbank und Webserver auf demselben Server befinden, lassen Sie den Standardwert `localhost` stehen. Das ist für die meisten Shops der Standard.
   * Ist Ihre Datenbank ausgelagert, geben Sie den Hostnamen oder die IP-Adresse Ihres Datenbankservers an. Ist dabei die Angabe eines Ports erforderlich, steht dieser nach dem Hostnamen und einem Doppelpunkt (``Hostname:Port``).

:guilabel:`Datenbank Name`

   Sie haben folgende Möglichkeiten:

   * Tragen Sie den Namen Ihrer ausgelagerten Datenbank ein.
   * Wenn Sie noch keine Datenbank haben, dann tragen Sie einen Namen für eine Datenbank ein, die das System beim Setup erstellt.

:guilabel:`Datenbank Benutzername` und :guilabel:`Datenbank Passwort`

   Geben Sie die Zugangsdaten zur Datenbank ein und bewahren Sie sie an einem sicheren Ort.

:guilabel:`Demodaten`

   Entscheiden Sie, ob Sie den Shop vorkonfiguriert mit Beispielartikeln installieren möchten.

   Demodaten sind empfehlenswert, wenn Sie sich zunächst in einer Testinstallation mit dem Shop vertraut machen möchten.

   Sie können die Demodaten jederzeit löschen, wenn Sie den Shop mit eigenen Artikeln befüllen wollen.


Wenn Sie noch keine Datenbank haben, wählen Sie die Schaltfläche :guilabel:`Datenbank jetzt erstellen`.

Wenn Sie eine existierende Datenbank eingebunden haben, erscheint eine Meldung, dass die Datenbank überschrieben wird und dass die erforderlichen Tabellen und Daten nun in dieser Datenbank gespeichert werden.


|schritt| Verzeichnisse & Login
-------------------------------

Passen Sie bei Bedarf die Verzeichnis-Einstellungen an und legen Sie die Zugangsdaten für den Administrationsbereich des Shops fest.

Notieren Sie sich die die folgenden Einstellungen und bewahren Sie die Daten an einem sicheren Ort auf:


:guilabel:`Shop-URL`

   Zeigt die URL an, unter der Ihr eShop erreichbar sein wird.


:guilabel:`Verzeichnis auf dem Server zum Shop`

   Gibt den internen Pfad zum Shop auf dem Server an (beispielsweise `/var/www/oxideshop/source/`).

   Passen Sie den Pfad beispielsweise dann an, wenn Sie mehrere Shops haben.

   Sie brauchen den Pfad im letzten Schritt des Setups.

:guilabel:`Verzeichnis auf dem Server zum TMP Verzeichnis`

   Benennt das Verzeichnis, in dem die temporären Dateien des Shops, beispielsweise für Smarty- oder SEO-Cache, gespeichert werden.

   Hintergrund: Manche Module fordern Sie von Zeit zu Zeit auf, temporäre Dateien manuell zu löschen.


:guilabel:`Administrator E-Mail` und :guilabel:`Administrator Passwort`

   Tragen Sie die E-Mail-Adresse und das Passwort des Administrators ein.

   Mit diesen Daten melden Sie sich nach dem Setup im Administrationsbereich an.

|schritt| Lizenz
----------------

Wenn Sie eine Enterprise oder Professional Edition haben, tragen Ihren Lizenzschlüssel ein, den sie mit Kauf des OXID eShop erhalten haben.

Der Lizenzschlüssel steht auf dem Lieferschein, der Ihnen per E-Mail zugeschickt wurde.

Wählen Sie :guilabel:`Lizenzschlüssel speichern`.

|schritt| Fertigstellen
-----------------------

Setzen Sie aus Sicherheitsgründen die Datei `config.inc.php` in den `read-only`-Modus. Testen Sie den Shop.

1. Öffnen Sie die Konsole Ihres Systems und wechseln Sie in das Verzeichnis des Shops (`/var/www/ocideshop/source/`).
2. Führen Sie folgenden Befehl aus:

   .. code:: bash

      chmod 0444 config.inc.php

3. Öffnen Sie den Shop als Kunde und als Administrator:

* Der Link :guilabel:`Zum Shop` führt Sie zur Startseite Ihres Shops.
* Der Link :guilabel:`Zur Shop Administration` führt Sie zum Administrationsbereich.



.. Intern: oxbaaf, Status: