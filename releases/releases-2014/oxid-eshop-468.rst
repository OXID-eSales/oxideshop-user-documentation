OXID eShop 4.6.8
****************
Versionsbezeichnung: 4.6.8, Revision e2f1a0e0287ce7674cf00eccb02171ad67942c91

Veröffentlichungstermin: 14.01.2014

Allgemeines
-----------
Dies ist das nunmehr letzte Release des OXID eShop Version 4.6. Ursprünglich wurde das bereits für den OXID eShop 4.6.7 erklärt, aber Fixes für die Bugs #5568 und #5582 sowie die Änderungen im Zusammenhang mit der bevorstehende SEPA-Umstellung machten die aktuelle Veröffentlichung notwendig.

Verbesserungen und Anpassungen
------------------------------
In der Version 4.6.8 wurden einige wenige Änderungen an Sprachdateien und Templates der Themes \"Basic\" und \"Azure\" sowie des Administrationsbereiches vorgenommen. Diese wurden hauptsächlich wegen der für Februar 2014 angekündigten SEPA-Umstellung notwendig. Der OXID eShop 4.6.8 ist damit auf die Umstellung des bargeldlosen Zahlungsverkehrs in Europa vorbereitet. Die Zahlungsart Bankeinzug/Lastschrift wurde angepasst, so dass als Kontonummer eine gültige IBAN (International Bank Account Number) und als Bankleitzahl ein BIC (Business Identifier Code) eingetragen werden können.

Eine Übersicht aller Änderungen finden Sie in :file:`/templ_docu_basic/index.html`, :file:`/templ_docu_azure/index.html` und :file:`/templ_docu_admin/index.html`.


Korrekturen
-----------
Alle mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet: `https://bugs.oxid-esales.com/changelog_page.php?version_id=249 <https://bugs.oxid-esales.com/changelog_page.php?version_id=249>`_

.. note:: Hinweise für Entwickler

Bug #5582: Die Funktion_handleDbConnectionException` wurde implementiert, um das Verhalten des OXID eShop im Produktivmodus beeinflussen zu können, wenn die Datenbank nicht erreichbar ist.

Bug #5568: Für die Entwicklung von Modulen gelten strengere Vorgaben. Aus Sicherheitsgründen können nur noch öffentliche Methoden von außerhalb des Shop-Frameworks angesprochen werden. Es besteht kein Zugriff auf geschützte Funktionen mehr.

.. Intern: oxaaep, Status: