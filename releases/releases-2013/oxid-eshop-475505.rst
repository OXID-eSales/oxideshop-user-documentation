OXID eShop 4.7.5/5.0.5
**********************
Versionsbezeichnung: 5.0.5, Revision 6cda1e4d8b4c19047960cdce632a54033e6fe2ff

Edition: Enterprise Edition

Versionsbezeichnung: 4.7.5, Revision 6cda1e4d8b4c19047960cdce632a54033e6fe2ff

Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 30.04.2013

Verbesserungen und Anpassungen
------------------------------
Änderungen in Templates
+++++++++++++++++++++++
In der Version 4.7.5/5.0.5 wurden einige Sprachdateien und Templates des Administrationsbereiches auf Grund von Bugfixes leicht angepasst. Folgende Templates aus :file:`/application/views/admin/tpl` enthalten minimale Änderungen: :file:`header.tpl`, :file:`list_order.tpl` und :file:`systeminfo.tpl`. Es war auch eine kleine Korrektur in den Sprachdateien des Themes \"Azure\" notwendig.

Eine Übersicht aller Änderungen finden Sie in :file:`/templ_docu_admin/index.html` und :file:`/templ_docu_azure/index.html` des Installationspaketes.

Weitere Änderungen
++++++++++++++++++
Die Revisionsnummer wird in den Dateien :file:`pkg.ref` und :file:`pkg.info` gespeichert, die sich im Hauptverzeichnis des Shops befinden. Da sich ihr Format geändert hat, wird die Revisionsnummer im Administrationsbereich nicht mehr im oberen rechten Bereich hinter der Shopversion angezeigt. Sie ist nun unter :menuselection:`Services --> Systeminfo` zu finden. Dort wird zu Beginn der Tabelle der Inhalt von :file:`pkg.info` ausgegeben. Siehe auch: `https://bugs.oxid-esales.com/view.php?id=5043 <https://bugs.oxid-esales.com/view.php?id=5043>`_

Die Datei :file:`.htaccess` im Hauptverzeichnis des Shop wurde geändert, weil das Skript :file:`getimg.php` in das Hauptverzeichnis des Shops verschoben wurde. Siehe auch: `https://bugs.oxid-esales.com/view.php?id=5037 <https://bugs.oxid-esales.com/view.php?id=5037>`_ .

Korrekturen
-----------
Alle mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet: `https://bugs.oxid-esales.com/changelog_page.php?version_id=192 <https://bugs.oxid-esales.com/changelog_page.php?version_id=192>`_ .