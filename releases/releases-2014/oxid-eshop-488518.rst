OXID eShop 4.8.8/5.1.8
**********************
Versionsbezeichnung: 5.1.8

Edition: Enterprise Edition

Versionsbezeichnung: 4.8.8

Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 28.10.2014

Verbesserungen und Anpassungen
------------------------------------
Änderungen in Templates
+++++++++++++++++++++++
In der Version 4.8.8/5.1.8 wurden kleine Änderungen in Templates des Themes \"Azure\" vorgenommen. Eine Übersicht aller Änderungen finden Sie in :file:`/templ_docu_azure/index.html`.

Sicherheitsverbesserungen
+++++++++++++++++++++++++
Die automatische Prüfung auf einen Security Token wird nun bei angemeldeten Benutzern für alle Formulare und Aktions-URLs ausgeführt. Einzige Ausnahme ist der Aufruf *fnc=tobasket* , um auch nicht angemeldeten Benutzern über einen Link Artikel in den Warenkorb legen zu können.

Passwörter wurden bisher mit der kryptographische Hashfunktion MD5 und einem zusätzlichen Salt verschlüsselt. Die Verschlüsselung wurde auf die aktuellere kryptographische Hashfunktion SHA-2 umgestellt und das Erzeugen der als Salt bezeichneten, zufällig gewählten Zeichenfolge leicht geändert. Die Kunden können sich wie gewohnt am Shop anmelden, ohne ein neues Passwort erstellen zu müssen.

Detaillierte Informationen entnehmen Sie bitte den Informationen für Entwickler auf der `OXIDforge <http://oxidforge.org/en/oxid-eshop-version-4-8-8-ce-pe-5-1-8-ee.html>`_ .

Korrekturen
-----------
Alle mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet:

`https://bugs.oxid-esales.com/changelog_page.php?version_id=261 <https://bugs.oxid-esales.com/changelog_page.php?version_id=261>`_ plus

`https://bugs.oxid-esales.com/view.php?id=3338 <https://bugs.oxid-esales.com/view.php?id=3338>`_

`https://bugs.oxid-esales.com/view.php?id=4150 <https://bugs.oxid-esales.com/view.php?id=4150>`_

`https://bugs.oxid-esales.com/view.php?id=5558 <https://bugs.oxid-esales.com/view.php?id=5558>`_

`https://bugs.oxid-esales.com/view.php?id=5628 <https://bugs.oxid-esales.com/view.php?id=5628>`_

`https://bugs.oxid-esales.com/view.php?id=5753 <https://bugs.oxid-esales.com/view.php?id=5753>`_

`https://bugs.oxid-esales.com/view.php?id=5809 <https://bugs.oxid-esales.com/view.php?id=5809>`_

`https://bugs.oxid-esales.com/view.php?id=5811 <https://bugs.oxid-esales.com/view.php?id=5811>`_

`https://bugs.oxid-esales.com/view.php?id=5835 <https://bugs.oxid-esales.com/view.php?id=5835>`_

`https://bugs.oxid-esales.com/view.php?id=5857 <https://bugs.oxid-esales.com/view.php?id=5857>`_

`https://bugs.oxid-esales.com/view.php?id=5860 <https://bugs.oxid-esales.com/view.php?id=5860>`_

`https://bugs.oxid-esales.com/view.php?id=5872 <https://bugs.oxid-esales.com/view.php?id=5872>`_

`https://bugs.oxid-esales.com/view.php?id=5887 <https://bugs.oxid-esales.com/view.php?id=5887>`_

Weiterführende Informationen für Entwickler finden Sie auf der `OXIDforge <http://oxidforge.org/en/oxid-eshop-version-4-8-8-ce-pe-5-1-8-ee.html>`_ .

Änderungen gegenüber der vorhergehenden Version können im Repository der Community Edition\auf `GitHub <https://github.com/OXID-eSales/oxideshop_ce/compare/v4.8.7...v4.8.8>`_ eingesehen werden.