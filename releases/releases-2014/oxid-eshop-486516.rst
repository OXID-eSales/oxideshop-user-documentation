OXID eShop 4.8.6/5.1.6
**********************
Versionsbezeichnung: 5.1.6, Revision 0bbad38b90d6448c49fee2f2ab8d411638ac7670

Edition: Enterprise Edition

Versionsbezeichnung: 4.8.6, Revision 0bbad38b90d6448c49fee2f2ab8d411638ac7670

Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 04.06.2014

Allgemeines
-----------
Seit Freitag, den 13.06.2014 gilt das Gesetz zur Umsetzung der Verbraucherrechterichtlinie, welches zahlreiche Neuerungen für den Online-Handel mit sich bringt. Die neue Verbraucherrechterichtlinie reformiert vor allem das Widerrufsrecht bei Fernabsatzverträgen sowie die Informationspflicht und verlangt somit diverse Anpassungen seitens Online-Anbietern zum Stichtag. Ausführlichere Informationen finden Sie in unserem Blogbeitrag\" `Neue Verbraucherrechterichtlinie ab 13.06.2014 <http://blog.oxid-esales.com/2014/03/neue-verbraucherrechterichtlinie-ab-13-06-2014/>`_ \".

Für den OXID eShop 4.8.6/5.1.6 wurden in Abstimmung mit Trusted Shops alle erforderlichen Änderungen vorgenommen.

Neue Funktionen
---------------
Neue Verbraucherrechterichtlinie umgesetzt
++++++++++++++++++++++++++++++++++++++++++
Im Bestellschritt 4 muss der Kunde beim Kauf von Dienstleistungen und Download-Artikeln, den AGB und dem Widerrufsrecht zustimmen. Dafür wurde ein Kontrollkästchen, welches nicht vorangekreuzt ist, in die Bestellseite integriert. Der Kunde muss das Häkchen explizit setzen und somit den Wegfall des Widerrufsrechts für immaterielle Güter bestätigen.

Im Administrationsbereich muss bei den entsprechenden Artikeln auf der Registerkarte :guilabel:`Erweitert` das Kontrollkästchen :guilabel:`AGB bestätigen` aktiviert sein.

Verbesserungen und Anpassungen
------------------------------
Änderungen in der Datenbank
+++++++++++++++++++++++++++
Die Tabelle *oxarticles*  erhielt das neue Datenbankfeld *OXSHOWCUSTOMAGREEMENT* . Die Datenbank wurde um die Konfigurationsoption *blEnableIntangibleProdAgreement*  erweitert und der Tabelle *oxContents* wurden zwei neue Datensätze hinzugefügt.

Änderungen in Templates
+++++++++++++++++++++++
Es gab Änderungen in Templates des Themes \"Azure\" und des Administrationsbereiches sowie im Stylesheet :file:`oxid.css`. Sie wurden notwendig durch die Umsetzung der Verbraucherrechterichtlinie. Eine Übersicht aller Änderungen finden Sie in der Template-Dokumentation :file:`/templ_docu_admin/index.html` und :file:`/templ_docu_azure/index.html` des Installationspaketes.

Änderungen in .php-Dateien
++++++++++++++++++++++++++
In den Dateien :file:`order.php`, :file:`basket.php`, :file:`category_main.php`, :file:`oxBasket.php` und :file:`oxArticle.php` wurden Änderungen vorgenommen.

Anpassungen nach Neu- oder Update-Installation
++++++++++++++++++++++++++++++++++++++++++++++
Wenn Sie Ihren OXID eShop auf die Version 4.8.6/5.1.6 aktualisieren, sind zwei Anpassungen notwendig.

Der Link im Footer des Shops muss von \"Lieferung und Kosten\" in \"Zahlung und Lieferung\" geändert werden. Gehen Sie dafür im Administrationsbereich zu :menuselection:`Kundeninformationen --> CMS-Seiten`. Ändern Sie den Titel der CMS-Seite mit dem Ident \"oxdeliveryinfo\".

Passen Sie den Inhalt der CMS-Seite \"Widerrufsrecht\" an und setzen sie einen Link zum Formular :file:`/out/pictures/wysiwigpro/Model_form_for_withdrawal_de.pdf`. Die CMS-Seite \"Widerrufsrecht\" hat den Ident\"oxrightofwithdrawal\".

Mailbenachrichtigung bei Lizenzproblemen
++++++++++++++++++++++++++++++++++++++++
Treten bei einem OXID eShop Professional oder Enterprise Edition unerwartet Probleme mit dem gespeicherten Lizenzkey auf, wird der Shopbetreiber per Mail informiert. Die Mail geht an die in den Grundeinstellungen unter Info E-Mail eingetragene Adresse. Es werden zwei Mails verschickt, eine mit Beginn des stillen Countdowns und eine zweite 24 Stunden bevor der Shop offline geht. Die Funktion wurde bereits mit Version 4.8.5/5.1.5 eingeführt und nun um die E-Mail-Benachrichtigung ergänzt.

Korrekturen
-----------
Alle mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet:

`https://bugs.oxid-esales.com/changelog_page.php?version_id=255 <https://bugs.oxid-esales.com/changelog_page.php?version_id=255>`_ \\

Weiterführende Informationen für Entwickler finden Sie auf der `OXIDforge <http://wiki.oxidforge.org/Downloads/4.8.6_5.1.6>`_ .

Änderungen gegenüber der vorhergehenden Version können im Repository der Community Edition auf `GitHub <https://github.com/OXID-eSales/oxideshop_ce/compare/v4.8.5...v4.8.6>`_ eingesehen werden.