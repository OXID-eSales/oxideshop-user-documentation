OXID eShop 4.7.10/5.0.10
************************
Versionsbezeichnung: 5.0.10, Revision 1ba99c94c3a1efacb84e6a31a50055d867b9a6c8

Edition: Enterprise Edition

Versionsbezeichnung: 4.7.10, Revision 1ba99c94c3a1efacb84e6a31a50055d867b9a6c8

Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 09.01.2014

Verbesserungen und Anpassungen
------------------------------
In der Version 4.7.10/5.0.10 wurden einige wenige Änderungen an Sprachdateien und Templates des Themes \"Azure\" und des Administrationsbereiches vorgenommen. Diese wurden hauptsächlich wegen der für Februar 2014 angekündigten SEPA-Umstellung notwendig. Der OXID eShop 4.7.10/5.1.10 ist damit auf die Umstellung des bargeldlosen Zahlungsverkehrs in Europa vorbereitet. Die Zahlungsart Bankeinzug/Lastschrift wurde angepasst, so dass als Kontonummer eine gültige IBAN (International Bank Account Number) und als Bankleitzahl ein BIC (Business Identifier Code) eingetragen werden können.

Eine Übersicht aller Änderungen finden Sie in :file:`/templ_docu_azure/index.html` und :file:`/templ_docu_admin/index.html`.

Korrekturen
-----------
Alle mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet:

`https://bugs.oxid-esales.com/changelog_page.php?version_id=225 <https://bugs.oxid-esales.com/changelog_page.php?version_id=225>`_ plus

`https://bugs.oxid-esales.com/view.php?id=5463 <https://bugs.oxid-esales.com/view.php?id=5463>`_

`https://bugs.oxid-esales.com/view.php?id=5582 <https://bugs.oxid-esales.com/view.php?id=5582>`_ 

`https://bugs.oxid-esales.com/view.php?id=5568 <https://bugs.oxid-esales.com/view.php?id=5568>`_

Hinweise für Entwickler

Bug #5582: Die Funktion_handleDbConnectionException` wurde implementiert, um das Verhalten des OXID eShop im Produktivmodus beeinflussen zu können, wenn die Datenbank nicht erreichbar ist.

Bug #5568: Für die Entwicklung von Modulen gelten strengere Vorgaben. Aus Sicherheitsgründen können nur noch öffentliche Methoden von außerhalb des Shop-Frameworks angesprochen werden. Es besteht kein Zugriff auf geschützte Funktionen mehr.

