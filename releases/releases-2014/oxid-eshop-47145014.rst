OXID eShop 4.7.14/5.0.14
************************
Versionsbezeichnung: 5.0.14

Edition: Enterprise Edition

Versionsbezeichnung: 4.7.14

Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 28.10.2014

Verbesserungen und Anpassungen
----------------------------------

Änderungen in Templates
+++++++++++++++++++++++
In der Version 4.7.14/5.0.14 wurden kleine Änderungen in den Sprachdateien und Templates des Administrationsbereiches und des Themes \"Azure\" vorgenommen. Die Version des Themes \"Azure\" ist jetzt 1.3.2 und wurde in der Datei :file:`theme.php` angepasst.

Eine Übersicht aller Änderungen finden Sie in :file:`/templ_docu_admin/index.html` und :file:`/templ_docu_azure/index.html`.

Sicherheitsverbesserungen
+++++++++++++++++++++++++
Die automatische Prüfung auf einen Security Token wird nun bei angemeldeten Benutzern für alle Formulare und Aktions-URLs ausgeführt. Einzige Ausnahme ist der Aufruf *fnc=tobasket* , um auch nicht angemeldeten Benutzern über einen Link Artikel in den Warenkorb legen zu können.

Passwörter wurden bisher mit der kryptographische Hashfunktion MD5 und einem zusätzlichen Salt verschlüsselt. Die Verschlüsselung wurde auf die aktuellere kryptographische Hashfunktion SHA-2 umgestellt und das Erzeugen der als Salt bezeichneten, zufällig gewählten Zeichenfolge leicht geändert. Die Kunden können sich wie gewohnt am Shop anmelden, ohne ein neues Passwort erstellen zu müssen.

Detaillierte Informationen entnehmen Sie bitte den Informationen für Entwickler auf der `OXIDforge <http://oxidforge.org/en/oxid-eshop-version-4-7-14-ce-pe-5-0-14-ee.html>`_ .

Korrekturen
-----------
Alle mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet: `https://bugs.oxid-esales.com/changelog_page.php?version_id=260 <https://bugs.oxid-esales.com/changelog_page.php?version_id=260>`_ .`Weiterführende Informationen für Entwickler finden Sie auf der `OXIDforge <http://oxidforge.org/en/oxid-eshop-version-4-7-14-ce-pe-5-0-14-ee.html>`_ .