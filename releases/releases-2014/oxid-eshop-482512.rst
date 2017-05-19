OXID eShop 4.8.2/5.1.2
**********************
Versionsbezeichnung: 5.1.2, Revision d7f91f476f7f27ca7fcceae24df3f133e1e5b3f1

Edition: Enterprise Edition

Versionsbezeichnung: 4.8.2, Revision d7f91f476f7f27ca7fcceae24df3f133e1e5b3f1

Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 28.01.2014

Allgemeines
-----------
Das Release musste wenige Stunden nach Veröffentlichung zurückgenommen werden, da ein unerwartetes Verhalten des WYSIWYG-Editors auftrat. Bitte aktualisieren Sie auf OXID eShop Version 4.8.3/5.1.3.

Neue Funktionen
---------------
Im Administrationsbereich kann unter :menuselection:`Stammdaten --> Grundeinstellungen --> Bankdaten (SEPA)` eingestellt werden, ob im Shop ausschließlich IBAN/BIC verwendet werden soll. Ist das Kontrollkästchen aktiviert, können im Bestellprozess Kontonummer und Bankleitzahl nicht mehr alternativ angegeben werden.

Verbesserungen und Anpassungen
------------------------------
In der Version 4.8.2/5.1.2 wurden einige wenige Änderungen an Sprachdateien und Templates des Administrationsbereiches und an einem Template des Themes \"Azure\" vorgenommen. Die Änderungen stehen im Zusammenhang mit der für Februar 2014 angekündigten SEPA-Umstellung.

Eine Übersicht aller Änderungen finden Sie in :file:`/templ_docu_basic/index.html` und :file:`/templ_docu_azure/index.html`.

Korrekturen
-----------
Alle mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet:

`https://bugs.oxid-esales.com/changelog_page.php?version_id=241 <https://bugs.oxid-esales.com/changelog_page.php?version_id=241>`_ .

Hinweise für Entwickler: Folgende Funktionen wurden als veraltet markiert:

oxModule::isExtended

oxSepaValidator::isValidIBANRegistry

oxSepaValidator::setIBANRegistry

oxSepaValidator::getIBANRegistry

.. Intern: oxaaeq, Status: