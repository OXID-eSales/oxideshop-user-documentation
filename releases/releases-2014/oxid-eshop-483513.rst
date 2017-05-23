OXID eShop 4.8.3/5.1.3
======================
Versionsbezeichnung: 5.1.3, Revision 5738f8cf8e498c85158db18cca0d9c368376955f

Edition: Enterprise Edition

Versionsbezeichnung: 4.8.3, Revision 5738f8cf8e498c85158db18cca0d9c368376955f

Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 31.01.2014

Allgemeines
-----------
Das Releases des OXID eShop 4.8.2/5.1.2 vom 28.01.2014 wurde zurückgenommen, da ein unerwartetes Verhalten des WYSIWYG-Editors auftrat. Das machte eine erneute Veröffentlichung notwendig, in der das Problem korrigiert wurde.

Neue Funktionen
---------------
Im Administrationsbereich kann unter :menuselection:`Stammdaten --> Grundeinstellungen --> Bankdaten (SEPA)` eingestellt werden, ob im Shop ausschließlich IBAN/BIC verwendet werden soll. Ist das Kontrollkästchen aktiviert, können im Bestellprozess Kontonummer und Bankleitzahl nicht mehr alternativ angegeben werden.

Verbesserungen und Anpassungen
------------------------------
In der Version 4.8.3/5.1.3 wurden einige wenige Änderungen an Sprachdateien und Templates des Administrationsbereiches und an einem Template des Themes \"Azure\" vorgenommen. Die Änderungen stehen im Zusammenhang mit der für Februar 2014 angekündigten SEPA-Umstellung.

Eine Übersicht aller Änderungen finden Sie in :file:`/templ_docu_basic/index.html` und :file:`/templ_docu_azure/index.html`. Bitte beachten Sie, dass es auch Änderungen in der Datei :file:`config.inc.php` und :file:`.htaccess` gab.

Korrekturen
-----------
Alle mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet:

`https://bugs.oxid-esales.com/changelog_page.php?version_id=241 <https://bugs.oxid-esales.com/changelog_page.php?version_id=241>`_ .

Das Patch-Release enthält auch alle Bugfixes der vorhergehenden Releases 4.6.7, 4.7.10/5.0.10 und 4.6.8:

`https://bugs.oxid-esales.com/changelog_page.php?version_id=188 <https://bugs.oxid-esales.com/changelog_page.php?version_id=188>`_

`https://bugs.oxid-esales.com/changelog_page.php?version_id=225 <https://bugs.oxid-esales.com/changelog_page.php?version_id=225>`_ plus

`https://bugs.oxid-esales.com/view.php?id=5463 <https://bugs.oxid-esales.com/view.php?id=5463>`_

`https://bugs.oxid-esales.com/view.php?id=5582 <https://bugs.oxid-esales.com/view.php?id=5582>`_

`https://bugs.oxid-esales.com/view.php?id=5568 <https://bugs.oxid-esales.com/view.php?id=5568>`_

`https://bugs.oxid-esales.com/changelog_page.php?version_id=249 <https://bugs.oxid-esales.com/changelog_page.php?version_id=249>`_

Hinweise für Entwickler: Folgende Funktionen wurden als veraltet markiert:

`oxModule::isExtended`

`oxSepaValidator::isValidIBANRegistry`

`oxSepaValidator::setIBANRegistry`

`oxSepaValidator::getIBANRegistry`

.. Intern: oxaaer (doppelt), Status: