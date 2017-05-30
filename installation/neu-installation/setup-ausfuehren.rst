Setup ausführen
===============
Über das webbasierte Setup wird der OXID eShop installiert und konfiguriert. Öffnen Sie einen Browser und rufen Sie ``www.ihreshopurl.de/setup`` auf. Ersetzen Sie dabei ``www.ihreshopurl.de`` durch die URL, unter der ihr OXID eShop erreichbar sein wird.

Das Setup startet. Es besteht aus 6 bzw. 7 Schritten. Für die Enterprise und die Professional Edition ist ein zusätzlicher Schritt erforderlich, damit der Lizenzkey eingegeben werden kann.

Während der Installation werden bestimmte Werte in die :file:`.htaccess` und die :file:`config.inc.php` geschrieben. Beide Dateien befinden sich im Hauptverzeichnis des Shops und sollten für die Dauer des Setups nicht schreibgeschützt sein.

1. Voraussetzungen
------------------
Im ersten Schritt des Setups werden die Systemvoraussetzungen geprüft. Wählen Sie die Sprache für die Installation aus. Die Anzeige wird direkt auf die gewählte Sprache umgestellt.

Farbige Symbole zeigen an, ob die Systemvoraussetzungen erfüllt sind:

.. |install-pass| image:: ../../media/icons-de/install-pass.png
.. |install-pmin| image:: ../../media/icons-de/install-pmin.png
.. |install-fail| image:: ../../media/icons-de/install-fail.png
.. |install-null| image:: ../../media/icons-de/install-null.png

* |install-pass| Die Voraussetzung ist erfüllt.
* |install-pmin| Die Voraussetzung ist nicht oder nur teilweise erfüllt. Der OXID eShop funktioniert trotzdem und kann installiert werden.
* |install-fail| Die Voraussetzung ist nicht erfüllt. Der OXID eShop funktioniert nicht ohne diese Voraussetzung und kann nicht installiert werden.
* |install-null| Die Voraussetzung konnte nicht überprüft werden.

Stellen Sie sicher, dass alle Systemvoraussetzungen erfüllt sind, um den OXID eShop installieren und störungsfrei betreiben zu können. Bei Konfigurationsproblemen wenden Sie sich bitte an Ihren OXID Hosting Partner oder Internet Service Provider (ISP). Sobald alle Systemvoraussetzungen erfüllt sind (es sind keine roten Markierungen vorhanden), betätigen Sie die Schaltfläche :guilabel:`Setup beginnen`.

2. Willkommen
-------------
Region, Hauptlieferland und Sprache des Shops können im zweiten Schritt des Setups festgelegt werden. Mit Region geben Sie an, auf welche Wirtschaftsregion das Angebot des Shops ausgerichtet ist. Derzeit wird zwischen Deutschland, Österreich, Schweiz (DACH) und Sonstige unterschieden. Sie können weitere Lieferländer und/oder Sprachen später jederzeit hinzufügen.

Bestätigen Sie die Option :guilabel:`Verbindung mit den OXID Servern erlauben`. Dadurch werden zusätzliche Produktinformationen im Administrationsbereich angezeigt (eCommerce Services). Auch über Updates für den Shop und die installierten Module soll zukünftig bei aktivierter Option informiert werden. Für die Professional und die Enterprise Edition wird später auch eine Online-Prüfung der verwendeten Lizenz erfolgen. Bitte beachten Sie, dass in keinem Fall geschäftsrelevante Daten (Benutzer, Umsatz etc.) übermittelt werden.

Aktivieren Sie auch das Kontrollkästchen für die regelmäßige Prüfung auf Aktualisierungen. Drücken Sie die Schaltfläche :guilabel:`Shopinstallation beginnen`.

3. Lizenzbedingungen
--------------------
Auf dieser Seite des Setups werden Ihnen die Lizenzbedingungen angezeigt. Bitte informieren Sie sich über die Lizenzbedingungen für Ihren OXID eShop. Sind Sie damit einverstanden, wählen Sie :guilabel:`Ich akzeptiere die Lizenzbedingungen` aus und klicken Sie dann auf :guilabel:`Weiter`.

4. Datenbank
------------
Im vierten Schritt des Setups werden die Daten für die von Ihnen erstellte Datenbank benötigt.

:guilabel:`Datenbank Hostname oder IP Adresse` |br|
Sie können den Defaultwert localhost stehen lassen, wenn sich Datenbank und Webserver auf dem gleichen Server befinden. Das ist für die meisten Shops der Standard. Ist die Datenbank ausgelagert, muss der Hostname oder die IP-Adresse des Datenbankservers angegeben werden. Ist dabei die Angabe eines Ports erforderlich, steht dieser nach dem Hostnamen und einem Doppelpunkt (Hostname:Port).

:guilabel:`Datenbank Name` |br|
Tragen Sie den Namen der zuvor erstellten Datenbank ein.

:guilabel:`Datenbank Benutzername` und :guilabel:`Datenbank Passwort` |br|
Geben Sie die Zugangsdaten zur Datenbank ein.

:guilabel:`Demodaten` |br|
Entscheiden Sie, ob Sie den Shop vorkonfiguriert mit Beispielartikeln installieren möchten. Demodaten sind empfehlenswert, wenn Sie sich zunächst in einer Testinstallation mit dem Shop vertraut machen möchten. Sie können die Demodaten jederzeit löschen, wenn Sie den Shop mit eigenen Artikeln befüllen wollen.

Auch wenn Sie Ihren Shop ohne Demodaten installieren, müssen Sie auf Demoshops nicht verzichten. Auf unserer Website gibt es vorbereitete Demoshops zum Anschauen und Ausprobieren. Sie können die meisten Funktionen testen. Einige Funktionen sind jedoch im Demoshop-Modus aus Sicherheitsgründen eingeschränkt. Keine Sorge, dass Sie an den Demoshops etwas kaputt machen könnten. Diese werden stündlich zurückgesetzt.

*  `Demoshop Professional Edition <https://demoshop.oxid-esales.com/professional-edition>`_ 
*  `Demoshop Community Edition <https://demoshop.oxid-esales.com/community-edition>`_ 

:guilabel:`UTF-8 Zeichenkodierung benutzen` |br|
Die UTF-8 Zeichenkodierung ist dann sinnvoll, wenn Sie viele verschiedene Sprachen mit unterschiedlichen Zeichensätzen, beispielsweise Deutsch und Russisch, verwenden möchten.

Betätigen Sie die Schaltfläche :guilabel:`Datenbank jetzt erstellen`. In einigen besonderen Konstellationen kann damit die Datenbank auch direkt erstellt werden, ohne dass sie vorher manuell angelegt werden musste. Da Ihre Datenbank bereits existiert, werden alle erforderlichen Tabellen und Daten nun in dieser Datenbank gespeichert.

5. Verzeichnisse \& Login
-------------------------
Im nächsten Schritt des Setups lassen sich die Verzeichnis-Einstellungen anpassen und die Zugangsdaten für den Administrationsbereich des Shops festlegen. Die Setup-Routine erkennt die Verzeichnisse automatisch und schlägt diese vor. Eine Änderung ist in den allermeisten Fällen nicht notwendig.

:guilabel:`Shop-URL` |br|
Es wird die URL angezeigt, unter der Ihr eShop erreichbar sein wird.

:guilabel:`Verzeichnis auf dem Server zum Shop` |br|
Der interne Pfad zum Shop auf dem Server wird ausgegeben.

:guilabel:`Verzeichnis auf dem Server zum TMP Verzeichnis` |br|
Benennt das Verzeichnis, in dem die temporären Dateien des Shops, beispielsweise für Smarty- oder SEO-Cache, gespeichert werden.

Tragen Sie zusätzlich die E-Mail-Adresse und das Passwort des Administrators ein. Mit diesen Daten können Sie sich nach abgeschlossenem Setup im Administrationsbereich anmelden. Bewahren Sie diese Zugangsdaten an einem sicheren Ort auf.

6. Lizenz
---------
Shopbetreiber mit einer Enterprise oder Professional Edition tragen hier den Lizenzschlüssel ein, den sie mit Kauf des OXID eShop erhalten haben. Der Lizenzschlüssel steht auf dem Lieferschein, der Ihnen per E-Mail zugeschickt wurde. Weiter mit :guilabel:`Lizenzschlüssel speichern`.

7. Fertigstellen
----------------
Das Setup ist nun erfolgreich abgeschlossen. Über den Link :guilabel:`Zum Shop` gelangen Sie zur Startseite Ihres Shops. Der Link :guilabel:`Zur Shop Administration` führt Sie direkt zum Administrationsbereich.

.. Intern: oxaaaf, Status: