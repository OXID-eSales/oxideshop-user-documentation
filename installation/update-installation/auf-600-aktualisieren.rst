Auf 6.0.0 aktualisieren
=======================

Dieses Dokument beschreibt das Update auf OXID eShop 6.0.0. Es unterscheidet sich grundlegend von einem Standard-Update und sollte nur von einem OXID eShop Version 4.10.6 oder 5.3.6 ausgehen. Haben Sie einen Shop mit einer anderen Version im Einsatz, muss dieser zuerst auf einen Shop dieser Versionen aktualisiert werden.

Grundlage der Beschreibung ist ein OXID eShop, der bereits betrieben wird. Er verfügt über einen eingepflegten Warenkatalog (Artikel und Kategorien) und Benutzer, die im Shop eingekauft haben. Aufgrund der Komplexität des Updates zeigt dieses Dokument nur den Rahmen der Update-Installation auf. Alle Details und Einzelschritte entnehmen Sie bitte der Entwicklerdokumentation. Abhängig von Ihrem OXID eShop können die beschriebenen Einzelschritte erforderlich oder aber auch nicht relevant sein. Machen Sie sich daher gründlich mit dem Ablauf des Updates vertraut und prüfen Sie, inwieweit die jeweiligen Arbeitsschritte auf den zu aktualisierenden Shop zutreffen.

Führen Sie das Update immer erst in einer Testumgebung, einer Kopie Ihres aktuellen Shops, aus. Erstellen Sie zuvor eine Sicherung der Shopdateien und der Datenbank. Deaktivieren Sie alle Module und prüfen Sie, ob der Shop prinzipiell funktioniert. Testen Sie nach dem Update den Shop erneut und legen Sie dabei besonderen Wert auf die Funktionen des Bestellprozesses, auf Zahlungs- und Versandarten.

Arbeitet der Shop korrekt, kann das Update auch im Live-System ausgeführt werden. Kopieren Sie während des Updates im Live-System eine :file:`index.html` in das Hauptverzeichnis des Shops, in der Sie auf aktuelle Wartungsarbeiten hinweisen. Sie können den Shop auch deaktivieren und die Datei :file:`offline.html` zur Informationen Ihrer Kunden nutzen.

.. |schritt| image:: ../../media/icons-de/schritt.jpg

|schritt| Datenbank
-------------------
Dieses Dokument beschreibt alle Änderungen im OXID eShop, welche die Datenbank betreffen. Erfahren Sie hier alles über den Wechsel zur Database Engine InnoDB und zum Database Abstraction Layer Doctrine DBAL, über Änderungen in der Datenbank-API, im Master/Slave-Verhalten der Enterprise Edition sowie über den Wegfall des Loggings von MySQL-Abfragen und das Speichern von Sessions in der Datenbank.

Bevor die datenbankrelevanten Schritte durchgeführt werden, müssen die Datenbanktabellen und -felder bis auf wenige Ausnahmen auf UTF-8 umgestellt worden sein.

Dokument in der Entwicklerdokumentation: `https://docs.oxid-esales.com/developer/en/6.0/update/eshop_from_53_to_6/database.html <https://docs.oxid-esales.com/developer/en/6.0/update/eshop_from_53_to_6/database.html>`_

|schritt| Dateien und Ordner
----------------------------
Im Dokument wird beschrieben, wie Dateien und Ordner eines OXID eShop 4 bzw. 5 angepasst werden müssen. Dazu muss ein OXID eShop 6 parallel zum bestehenden OXID eShop 4 oder 5 installiert werden. Danach sind die Anweisungen auszuführen, welche eigene Scripts, die Konfigurationsdateien, die Sprachdateien, eigene Smarty-Plugins, die Log-Dateien sowie Dateien aus den Verzeichnissen :file:`/bin`, :file:`/export` und :file:`/log` betreffen.

Dokument in der Entwicklerdokumentation: `https://docs.oxid-esales.com/developer/en/6.0/update/eshop_from_53_to_6/files.html <https://docs.oxid-esales.com/developer/en/6.0/update/eshop_from_53_to_6/files.html>`_

|schritt| Module
----------------
Wenn Sie eigene Module in Ihrem OXID eShop einsetzen, erhalten Sie in diesem Dokument eine Anleitung, wie diese für den OXID eShop 6 portiert werden müssen. Darin wird zwischen einer minimalen und einer vollen Anpassung unterschieden. Letztere garantiert die bestmögliche Integration der Module in den neuen Shop und wird daher empfohlen.

Dokument in der Entwicklerdokumentation: `https://docs.oxid-esales.com/developer/en/6.0/update/eshop_from_53_to_6/modules.html <https://docs.oxid-esales.com/developer/en/6.0/update/eshop_from_53_to_6/modules.html>`_

|schritt| Theme
---------------
Das Dokument gibt einige Hinweise zur Umstellung eines Shops auf das neue Standard-Theme "Flow", welches das Theme "Azure" des OXID eShop 4 & 5 abgelöst hat.

Dokument in der Entwicklerdokumentation: `https://docs.oxid-esales.com/developer/en/6.0/update/eshop_from_53_to_6/theme.html <https://docs.oxid-esales.com/developer/en/6.0/update/eshop_from_53_to_6/theme.html>`_

|schritt| Neue und entfernte Funktionen
---------------------------------------
Der Abschnitt informiert zum einen über Funktionen, die aus dem Shop in einzelne Module ausgelagert wurden. Module für die Tags, den Lexware-Export, die erweiterte Bestellverwaltung (Bestellübersicht und Packliste), die Facebook-Integration, das Captcha und das Gästebuch erhielten eigene Repositories in GitHub. Sie sind kompatibel mit OXID eShop 6. Zum anderen werden Bibliotheken benannt, die aus dem OXID eShop entfernt wurden. Das sind Bibliotheken für JpGraph, Facebook API, Smarty, PHPMailer und InvoicePDF. Weitere Änderungen betreffen das Exception Handling, den generischen Export, die sogenannten DynPages und den Editor WYSIWYG Pro.

Dokumente in der Entwicklerdokumentation: `https://docs.oxid-esales.com/developer/en/6.0/update/eshop_from_53_to_6/features/index.html <https://docs.oxid-esales.com/developer/en/6.0/update/eshop_from_53_to_6/features/index.html>`_

.. Intern: oxbahw, Status: