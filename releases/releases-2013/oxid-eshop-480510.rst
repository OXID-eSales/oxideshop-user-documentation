OXID eShop 4.8.0/5.1.0
======================

Versionsbezeichnung: 5.1.0, Revision 333c29d26a16face3ac1a14f38ad4c8efc80fefc |br|
Edition: Enterprise Edition

Versionsbezeichnung: 4.8.0, Revision 333c29d26a16face3ac1a14f38ad4c8efc80fefc |br|
Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 29.10.2013

----------

Allgemeines
-----------

OXID eShop mit PayPal und Mobile Theme
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Das Standalone-Modul PayPal 3.1.0 und das Mobile Theme 1.2.0 sind in der Standardauslieferung des OXID eShop 4.8.0/5.1.0 enthalten.

Das Standalone-Modul PayPal integriert die schnelle und sichere Zahlung mit PayPal in den OXID eShop. Das ermöglicht dem Kunden das Bezahlen der Bestellung mit den Zahlungs- und Adressinformationen aus seinem PayPal-Konto, ohne diese im Shop selbst eingeben zu müssen. Shopbetreiber hingegen sind gegen Zahlungsausfälle geschützt, da die Zahlungsanforderung in Echtzeit geprüft und bestätigt wird. Details zur OXID eFire Extension PayPal finden Sie auf der Seite `Die neue OXID eFire Extension PayPal <https://www.oxid-esales.com/de/produkte-archiv/erweiterungen/efire-ext/oxid-efire-extension-paypal.html>`_.

OXID eShop Mobile Theme und das dazu gehörige Modul OXID eShop Theme Switch ermöglichen die Anzeige des OXID eShop auf einem mobilen Gerät, wie Smartphone oder Tablet. Details zum Mobile Theme entnehmen Sie bitte der Seite `OXID eShop mobile theme <https://www.oxid-esales.com/de/products/facts/oxid-eshop-mobile-theme/produktinformationen.html>`_.

Wenn Sie die Zahlungsart PayPal oder die Anzeige Ihres Shops auf mobilen Endgeräten nutzen möchten, müssen die Erweiterungen lediglich im Administrationsbereich unter :menuselection:`Stammdaten --> Erweiterungen` aktiviert werden. Durch ein Update auf Version 4.8.0/5.1.0 werden die Erweiterungen nicht installiert, können aber kostenfrei im `OXID eXchange <http://exchange.oxid-esales.com/startseite/>`_ heruntergeladen und nachgerüstet werden.

Ende für PHP 5.2
^^^^^^^^^^^^^^^^
Bereits im Dezember 2010 kündigte das PHP-Entwicklungsteam an, dass die Veröffentlichung von PHP 5.2.16 das Ende des PHP 5.2-Supports markiert. Details dazu finden Sie im News Archive von php.net: `http://www.php.net/archive/2010.php#id2010-12-16-1 <http://www.php.net/archive/2010.php#id2010-12-16-1>`_ .

OXID eShop 4.8.0/5.1.0 unterstützt daher die PHP-Version 5.2 nicht mehr. Er wird nicht in einer PHP 5.2-Umgebung getestet und die Wartung hinsichtlich dieser PHP-Version ist eingestellt. Für die OXID eShop Enterprise und Professional Edition liegen Installationspakete vor, die für PHP 5.3 und PHP 5.4 verschlüsselt sind. Der Quellcode aller Editionen ist momentan noch kompatibel zu PHP 5.2, sodass der OXID eShop auch in einer solchen Umgebung lauffähig sein sollte. Dies wurde nicht explizit getestet und kann daher nicht garantiert werden. Ein Anspruch auf Support besteht in diesem Falle nicht.

Bereits im nächsten Major Release sollen beispielsweise Sprach-Features aus PHP 5.3 genutzt werden. Wir empfehlen eine sofortige Umstellung auf PHP 5.3 und höher. Achten Sie bitte darauf, dass die PHP-Version Ihres Server zur installierten Shopversion passt. Module, die im Shop verwendet werden, müssen ebenfalls mit der PHP-Version kompatibel sein. Siehe auch den englischsprachigen Blogpost vom 08.10.2013:  `http://blog.oxid-esales.com/2013/10/php-52-will-not-be-supported-from-oxid-eshop-versions-48-and-51-on <http://blog.oxid-esales.com/2013/10/php-52-will-not-be-supported-from-oxid-eshop-versions-48-and-51-on>`_.

----------

Neue Funktionen
---------------

Shop mit SEPA-Unterstützung
^^^^^^^^^^^^^^^^^^^^^^^^^^^
SEPA steht für Single Euro Payments Area (Einheitlicher Euro-Zahlungsverkehrsraum) und ist ein Projekt zur Vereinheitlichung des bargeldlosen Zahlungsverkehrs in Europa. Zum 01.02.2014 enden nationale Überweisungs- und Lastschriftverfahren in den Euro-Ländern. Hintergrundinformationen finden Sie beispielsweise auf der Webseite der Europäischen Zentralbank: `http://www.ecb.europa.eu/paym/sepa/html/index.en.html <http://www.ecb.europa.eu/paym/sepa/html/index.en.html>`_.

OXID eShop 4.8.0/5.1.0 ist auf die Umstellung des bargeldlosen Zahlungsverkehrs in Europa vorbereitet. Die Zahlungsart Bankeinzug/Lastschrift wurde angepasst, so dass als Kontonummer eine gültige IBAN (International Bank Account Number) und als Bankleitzahl ein BIC (Business Identifier Code) eingetragen werden können.

Diagnosewerkzeug im Administrationsbereich
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Das Diagnosewerkzeug, welches aus dem Administrationsbereich heraus aufgerufen werden kann, ermittelt Informationen über den Shop und den Server. Angaben über den Shop, dessen Edition und Version sowie die Anzahl von Subshops, Kategorien und Artikeln werden immer angezeigt. Optional können die Module des Shops aufgelistet und die Systemgesundheit, die PHP-Konfiguration und Serverinformationen abgefragt werden.

In das Diagnosewerkzeug ist das bekannte Prüfskript :file:`oxchkversion.php` integriert, welches die Konsistenz des Shops untersucht. Dabei werden alle .php-Dateien und Templates geprüft, indem ihre MD5-Checksumme über einen Webservice mit den in einer Datenbank gespeicherten Werten verglichen wird.

Neue Widgets
^^^^^^^^^^^^
OXID eShop 4.7.0/5.0.0 führte Widgets als einen neuen Komponententyp für den Seitenaufbau ein. Widgets sind logische Elemente der Benutzeroberfläche (GUI), die in jedem beliebigen Template verwendet werden können.

Mit diesem Shop-Release ergänzen 'oxwArticleBox', 'oxwArticleDetails', 'oxwRating' und 'oxwReview' die bereits vorhandenen Widgets. Weitere Informationen finden Sie im Tutorial `Widgets from 4.8 5.1 <http://oxidforge.org/en/widgets-from-4-8-5-1.html>`_ in der OXIDforge.

----------

Verbesserungen und Anpassungen
------------------------------

Änderungen in Templates
^^^^^^^^^^^^^^^^^^^^^^^
Es gab Änderungen in Templates und Sprachdateien des Administrationsbereiches und des Themes \"Azure\". Die bereits erwähnten Widgets, das Diagnosewerkzeug oder die Verwendung von Argumenten in Sprachkonstanten hatten beispielsweise neue, umgestellte oder erweiterte Templates zur Folge.

Eine Übersicht aller Änderungen finden Sie in der Template-Dokumentation :file:`/templ_docu_admin/index.html` und :file:`/templ_docu_azure/index.html` des Installationspaketes.

Sprachdateien
^^^^^^^^^^^^^
Die Sprachdateien wurden überarbeitet. Dabei wurden Duplikate bei den Sprachkonstanten entfernt, Übersetzungen geändert und teilweise musste auch die Schreibweise von Sprachkonstanten korrigiert werden. Auf das so genannte Mapping von Sprachkonstanten wird fortan verzichtet, um die Transparenz bei der Verwendung von Sprachkonstanten und übersetzten Texten zu verbessern. Die Funktion für das Mapping ist noch vorhanden und kann bei Bedarf weiter verwendet werden.

Die Anzahl der Sprachkonstanten konnte um rund 20 Prozent reduziert werden. Alle Sprachkonstanten, die in den Templates des Themes \"Azure\" verwendet werden, wurden nach :file:`/application/translations/{locale}/lang.php` verschoben. Die ursprüngliche Datei :file:`/application/views/azure/{locale}/lang.php` ist noch vorhanden und kann, wenn benötigt, verwendet werden.

Mit zwei neuen Funktionen können den Sprachkonstanten Satzzeichen angehangen oder Argumente übergeben werden. Damit lassen sich Texte beispielsweise mit einem Doppelpunkt abschließen. Das Satzzeichen wird selbst als Sprachkonstante definiert. Ein der Sprachkonstante übergebenes Argument wird anstatt eines Platzhalters im Text ausgegeben. Eine kurze Beschreibung mit Anwendungsbeispielen finden Sie in den englischsprachigen Release Notes `OXID eShop version 4.8.0 (CE + PE) & 5.1.0 (EE) <http://oxidforge.org/en/oxid-eshop-version-4-8-0-ce-pe-5-1-0-ee.html>`_ der OXIDforge.

Für die Aktualisierung der Templates und Sprachdateien wurde ein Script bereitgestellt. Beachten Sie bitte die Hinweise in der Readme-Datei, wenn Sie das Script verwenden möchten. Es ist in die Update-Prozedur des OXID eShop integriert, kann aber auch separat aus GitHub heruntergeladen werden: `https://github.com/OXIDprojects/languageFixer <https://github.com/OXIDprojects/languageFixer>`_.

PDF-Rechnung
^^^^^^^^^^^^
Das in Community und Professional Edition verwendete Modul zur Ausgabe einer PDF-Rechnung wurde angepasst. Dabei wurden auch die Sprachkonstanten aus den Sprachdateien des Shops in die des Moduls verschoben.

Position des Währungszeichens
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Das Währungszeichen kann nun anstatt nach dem Preis auch vor diesem stehen. Beispiel: \"$17.00\" anstatt \"17.00 $\".

In den Templates wurde dies mit einem Smarty-Plugin umgesetzt.

``[{oxprice price=$oArticle-\>getPrice() currency=$currency }]``

Ob das Währungszeichen vor oder nach dem Preis steht, wird im Administrationsbereich bei :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Weitere Einstellungen` definiert. Schließt die Zeile für eine Währung mit @Front ab, wird das Währungszeichen dem Preis vorangestellt. Beispiel: ``USD@ 1.2994@ .@ @ $@ 2 @Front``

Eigene Datei für Shop-Logo
^^^^^^^^^^^^^^^^^^^^^^^^^^
Standardmäßig wird die Datei :file:`logo.png` aus dem Verzeichnis :file:`/out/azure/img` für das Shop-Logo verwendet. Nun kann auch eine eigene Datei in der :file:`config.inc.php` angegeben werden. Speichern Sie Ihr Shop-Logo im genannten Verzeichnis und ergänzen Sie die Konfigurationsdatei mit einer Zeile in folgender Syntax: ``$this-\>sShopLogo = 'your_own_image.jpg';``

Meldungen für Nachnahme und internationalen Versand
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Wie von Trusted Shops empfohlen, werden Meldungen im Bestellprozess ausgegeben, die auf mögliche zusätzliche Gebühren bei der Auswahl von Nachnahme als Zahlungsart und bei Versand ins Ausland entstehen können. Diese Meldungen können im Administrationsbereich unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Bestellungen` abgeschaltet werden. Die Meldungstexte sind in den CMS-Seiten mit den IDs 'oxtscodmessage' und 'oxtsinternationalfees' editierbar.

Integriertes Trustbage
^^^^^^^^^^^^^^^^^^^^^^
Wurde Ihr Shop von Trusted Shops zertifiziert, können Sie den Kunden Ihre Vertrauenswürdigkeit noch deutlicher kommunizieren. Mit dem Trustbage wird das Trusted Shops Gütesiegel immer im unteren rechten Eck des Browserfensters angezeigt. Bewegt der Kunde die Maus über das Siegel, öffnet sich die sogenannte Trustcard, ein Zusatzfenster mit weiteren Informationen von Ihrer Zertifikatsseite bei Trusted Shops. Beispiel: Bei `Edeka24 <http://www.edeka24.de/>`_, einem OXID eShop, ist das Trustbage bereits im Einsatz.

----------

Korrekturen
-----------
Korrekturen 4.8.0/5.1.0 Final: `https://bugs.oxid-esales.com/changelog_page.php?version_id=227 <https://bugs.oxid-esales.com/changelog_page.php?version_id=227>`_ |br|
Korrekturen 4.8.0/5.1.0 RC 2: `https://bugs.oxid-esales.com/changelog_page.php?version_id=221 <https://bugs.oxid-esales.com/changelog_page.php?version_id=221>`_ |br|
Korrekturen 4.8.0/5.1.0 RC 1: `https://bugs.oxid-esales.com/changelog_page.php?version_id=213 <https://bugs.oxid-esales.com/changelog_page.php?version_id=213>`_ |br|
Korrekturen 4.8.0/5.1.0 Beta 1: `https://bugs.oxid-esales.com/changelog_page.php?version_id=166 <https://bugs.oxid-esales.com/changelog_page.php?version_id=166>`_

----------

Weiterführende Informationen für Entwickler finden Sie auf der OXIDforge: `http://oxidforge.org/en/oxid-eshop-version-4-8-0-ce-pe-5-1-0-ee.html <http://oxidforge.org/en/oxid-eshop-version-4-8-0-ce-pe-5-1-0-ee.html>`_.

.. Intern: oxaaej, Status: