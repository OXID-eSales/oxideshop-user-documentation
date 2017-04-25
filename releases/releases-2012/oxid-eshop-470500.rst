OXID eShop 4.7.0/5.0.0
**********************
Versionsbezeichnung: 5.0.0, Revision 51243

Edition: Enterprise Edition

Versionsbezeichnung: 4.7.0, Revision 51243

Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 08.11.2012

Allgemeines
-----------
In dieser Shopversion wurden zwei Haupt-Features für die Enterprise Edition entwickelt und umgesetzt: Caching und Master/Slave. Die Features tragen wesentlich zur Verbesserung der Performance und zur Reduktion von Lastspitzen in Hochlast-Szenarien bei. Sie erweitern damit signifikant das Potential des OXID eShop. Dies wird durch die Versionsbezeichnung 5.0.0 zum Ausdruck gebracht. Professional und Community Edition wurden mit der Versionsbezeichnung 4.7.0 veröffentlicht. Sie enthalten alle wichtigen Änderungen am OXID Framework und am Core sowie sämtliche Korrekturen.

Zukünftig sollen alle drei Shop-Editionen wieder zusammengeführt werden. Die nächsten Releases sollen neue Funktionen enthalten, die hauptsächlich für OXID eShop, die kleineren E-Commerce betreiben, hilfreich sind. Selbstverständlich wird dabei die Open Source-Strategie weiter konsequent umgesetzt und der OXID eShop auf einer gemeinsamen Code-Basis entwickelt.

Update-Installation
+++++++++++++++++++
Das Update auf OXID eShop Version 4.7.0 (Community und Professional Edition) und Version 5.0.0 (Enterprise Edition) unterscheidet sich grundlegend vom Standard-Update und kann nur auf einen OXID eShop Version 4.6.5 bzw. 4.6.6 angewandt werden. Haben Sie eine vorhergehende Shopversion im Einsatz, muss diese zuerst auf 4.6.5 bzw. 4.6.6 aktualisiert werden.

Die Anleitung `Auf 4.7.0/5.0.0 aktualisieren <de/support-services/dokumentation-und-hilfe/oxid-eshop/installation/oxid-eshop-aktualisieren/auf-470500-aktualisieren.html>`_ beschreibt das Update des OXID eShop.

Hinweis: Wir empfehlen dringend, das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, auszuführen. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

Neue Funktionen
-----------------

Caching (nur Enterprise Edition)
++++++++++++++++++++++++++++++++++
Für die Enterprise Edition wurde ein neues Caching-System implementiert. Es wird durch drei Hauptkomponenten umgesetzt: durch den in den OXID eShop integrierten Cache Manager, unterstützt durch den Reverse Proxy Varnish und/oder durch Memcached. Das Zusammenwirken der Komponenten bewirkt, dass – wenn immer möglich – zwischengespeicherte Inhalte genutzt und an die anfragenden Web-Clients geschickt werden. Damit werden die Datenbankzugriffe reduziert und die Antwortzeiten des OXID eShop verkürzt.

Anleitung zur Konfiguration von Varnish und Memcached sowie zu den Einstellungen für das Caching finden Kunden mit einer Enterprise Edition und ausgewählte Partner im Abschnitt `Enterprise Edition <de/support-services/dokumentation-und-hilfe/oxid-eshop/enterprise-edition.html>`_ unserer Online-Dokumentation. Dieser Abschnitt der Online-Dokumentation ist passwortgeschützt. Über ein bereitgestelltes Formular können Sie Zugangsdaten anfordern.

Master/Slave (nur Enterprise Edition)
+++++++++++++++++++++++++++++++++++++
Die Enterprise Edition kann bei aktiviertem Master/Slave mit mehreren Datenbanken betrieben werden. Dabei ist eine Datenbank die Master-Datenbank, die hauptsächlich Schreibzugriffe verarbeitet. Die Slave-Datenbanken enthalten gespiegelte Daten und bedienen die Lesezugriffe. Ein Load-Balancer verteilt die Datenbankzugriffe nach dieser grundsätzlichen Unterscheidung auf die Master-Datenbank und auf die Slave-Datenbanken.

Kunden mit einer Enterprise Edition und ausgewählte Partner finden die Anleitung zur Konfiguration von Master/Slave ebenfalls im Abschnitt `Enterprise Edition <de/support-services/dokumentation-und-hilfe/oxid-eshop/enterprise-edition.html>`_ unserer Online-Dokumentation.

Widgets
+++++++
Mit den Widgets wurde ein neuer Komponententyp für den Seitenaufbau des OXID eShop eingeführt. Es sind logische Elemente der Benutzeroberfläche (GUI), die in jedem beliebigen Template verwendet werden können. Die Aufteilung der Seiten in kleine Einheiten ist eine wichtige Voraussetzung für das Caching. Weitere Informationen zu den Widgets finden Sie im Tutorial `Widgets in 4.7 + 5.0 <http://wiki.oxidforge.org/Tutorials/widgets_from_4.7_5.0>`_ in der OXIDforge.

EU Cookie-Richtlinie
++++++++++++++++++++
In einer 2009 verabschiedeten Richtlinie hat die Europäische Union gefordert, Besucher einer Website über die Verwendung von Cookies zu informieren. Diese kleinen Textdateien enthalten Informationen über die Einstellungen des Benutzers für die Website, zum Beispiel Login-Informationen, Spracheinstellung oder bei einem Online-Shop den Inhalt des Warenkorbs.

Der OXID eShop weist Benutzer beim ersten Besuch darauf hin, dass Cookies verwendet werden. Der Benutzer kann entscheiden, ob er die Cookies akzeptieren, keine Cookies verwenden oder die Seite verlassen möchte. Die Funktion kann im Administrationsbereich unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Weitere Einstellungen` aktiviert werden.

Benutzerdefinierte Konfigurationsdatei
++++++++++++++++++++++++++++++++++++++
Eigene Konfigurationseinstellungen können in der Datei :file:`cust_config.inc.php` definiert werden, die beim Start nach der :file:`config.inc.php` geladen wird. Die benutzerdefinierte Konfigurationsdatei muss sich im Hauptverzeichnis des OXID eShop befinden.

Datenbanktabellen mit Zeitstempel
+++++++++++++++++++++++++++++++++
Alle Datenbanktabellen erhielten ein zusätzliches Datenbankfeld \"oxtimestamp\". Beim Erstellen und Ändern von Datensätzen wird die jeweilige Zeit in das Datenbankfeld eingetragen. Damit sind vor kurzem erstellte und geänderte Datensätze schnell zu finden, was die Synchronisation von Daten mit angeschlossenen Systemen erleichtert.

Verbesserungen und Anpassungen
--------------------------------
Überarbeiteter Bootstrap-Prozess
++++++++++++++++++++++++++++++++
Um den OXID eShop noch schneller zu machen, wurde der Bootstrap-Prozess überarbeitet. Der sogenannte Bootstrap-Prozess ist ein Script, welches alle Methoden inkludiert, definiert und initialisiert, damit das Framework des OXID eShop korrekt arbeitet. Das Framework startet nun in einer effizienteren Weise, indem ausschließlich dessen unmittelbar benötigte Teile geladen werden.

Detaillierte Informationen zum überarbeiteten Bootstrap-Prozess finden Sie im Tutorial `Bootstrap process refactored in 4.7 5.0 <http://wiki.oxidforge.org/Tutorials/bootstrap_process_refactored_in_4.7_5.0>`_ in der OXIDforge.

Theme \"Basic\" und Template-Änderungen
+++++++++++++++++++++++++++++++++++++++
Das Theme \"Basic\" wird nicht mehr unterstützt. OXID eShop 4.7.0/5.0.0 enthält ausschließlich das Theme \"Azure\". Obwohl das Theme \"Basic\" nicht länger gewartet wird, ist dessen Funktionalität noch vorhanden und kann nach einem Update noch genutzt werden. Eine Anleitung zur Anpassung der Templates finden Sie im Tutorial `Use basic theme from version 4.7 and 5.0 on <http://wiki.oxidforge.org/Tutorials/use_basic_theme_from_version_4.7_and_5.0_on>`_ in der OXIDforge.

Templates wurden im Zusammenhang mit der sogenannten \"Button-Lösung\", die nachfolgend beschrieben ist, geändert. Das Theme \"Azure\" enthält bereits alle notwendigen Verbesserungen, damit der OXID eShop die Vorgaben des deutschen Gesetzgebers erfüllt. Es gab auch noch weitere kleinere Änderungen in den Templates. Die als \"deprecated\" gekennzeichneten Bestandteile wurden entfernt.

Button-Lösung und Attribute
+++++++++++++++++++++++++++
Wegen der vom Deutschen Bundestag beschlossenen und am 01. August 2012 in Kraft getretenen sogenannten \"Button-Lösung\" wurden im OXID eShop Vorgaben zur Information von Kunden im Bestellabschluss umgesetzt. Im letzten Bestellschritt werden die Details zur Bestellung kompakt am Ende der Bestellübersicht ausgegeben. Sie zeigen alle kaufrelevanten Informationen eines Artikels, inklusive der Werte bestimmter Attribute. Direkt unter diesen Informationen befindet sich der Button :guilabel:`Zahlungspflichtig bestellen`.

Ob ein Attribut im Bestellprozess als Zusatzinformation beim Artikel angezeigt werden soll, kann direkt unter :menuselection:`Artikel verwalten --> Attribute`, Registerkarte :guilabel:`Stamm` eingestellt werden. Aktivieren Sie dafür das Kontrollkästchen :guilabel:`Wert des Attributs für Artikel im Bestellprozess anzeigen`.

Neue Datei- und Verzeichnisstruktur
+++++++++++++++++++++++++++++++++++
Die Architektur des OXID eShop unterliegt ständigen Erweiterungen. Die Struktur von Verzeichnissen und Dateien wurde mit diesem Major Release geändert, um die Architektur klarer zu verdeutlichen. Es erfolgte eine generelle Trennung von Framework und System-Komponenten von der eigentlichen Anwendung. Das Verzeichnis :file:`/core` enthält die Komponenten des Frameworks für Datenbank-, Datei- und Session-Handling usw. Im Verzeichnis :file:`/application` befinden sich alle Dateien, die den OXID eShop als Anwendung repräsentieren. Das Verzeichnis für die Anwendung wurde zudem in Unterordner aufgeteilt, die das der Architektur zugrunde liegende MVC-Konzept (Model View Controller) abbilden. Darüber hinaus erhielten Komponenten und die neuen Widgets eigene Ordner.

*Bisherige Verzeichnisstruktur*

``/eshop

\\/core

\\/views

\\/modules

\\/out

\\/tmp``

*Neue Verzeichnisstruktur*

``/eshop

\\/application

\\\\\/models\\\\\\\\\

\\\\\/controllers

\\\\\/components

\\\\\\\\/widgets

\\\\\/views

\\\\\/translations

\\/core

\\/modules

\\/out

\\/tmp``

*Dateien und neue Speicherorte*


* Models: Dateien, zuständig für Business Logic, wurden vom Verzeichnis :file:`/core` nach :file:`/application/models` verschoben. Andere Dateien verblieben dort als Teil des Frameworks.
* Controllers: Alle Dateien aus dem Verzeichnis :file:`/views` wurde nach :file:`/application/controllers` verschoben mit Ausnahme folgender Dateien: :file:`oxview.php`, :file:`oxviewconfig.php`, :file:`oxshopcontrol.php` in das Verzeichnis :file:`/core` und :file:`oxcmp_*.php` in das Verzeichnis :file:`/application/components`.
* Controllers für Administrationsbereich wurden vom Verzeichnis :file:`/admin` nach :file:`/application/controllers/admin` verschoben.
* Templates befinden sich jetzt im Verzeichnis :file:`/application/views`.
* Die generischen Sprachdateien wurden vom Verzeichnis :file:`/out/{local}` nach :file:`/application/translations/{local}` verschoben.

Datei für Transliteration
+++++++++++++++++++++++++
Die Liste der Zeichen, die in der URL durch andere Zeichen zu ersetzen sind (Transliteration), wurde aus der :file:`lang.php` in die neue Datei :file:`translit_lang.php` verschoben.

Sprachabhängige Überprüfung der Shopversion
+++++++++++++++++++++++++++++++++++++++++++
Im Administrationsbereich wird unter :menuselection:`Stammdaten` --> :menuselection:`Grundeinstellungen` --> :guilabel:`Lizenz` der Update-Status geprüft. Dabei wurde bisher immer ein Ergebnis in deutscher Sprache zurückgegeben. Nun wird berücksichtigt, mit welcher Sprache die Anmeldung am Administrationsbereich erfolgte. Unterstützt werden die beiden Standardsprachen des OXID eShop Deutsch und Englisch (Default).

Modul-Handling
++++++++++++++
Beim Aktivieren und Deaktivieren von Modulen können jetzt Ereignisse ausgeführt werden. Diese sind in der Metadata-Datei zu definieren. Derzeit werden die Ereignisse \"onActivate\" und \"onDeactivate\" unterstützt. Weitere Ereignisse sind geplant.

:code:`'events' =\>array(

\\'onActivate' =\>'myModuleEvents::onActivate',

\\'onDeactivate' =\>'myModuleEvents::onDeactivate' ),`

Die Klasse \"myModuleEvents\" wird ebenfalls in der Metadata-Datei, im Array \"files\" angegeben. Alle Module, die Ereignisse verwenden, müssen die Metadata-Version 1.1 haben.

Mit der geänderten Datei- und Verzeichnisstruktur hat sich auch die der Module geändert.

* Dateien müssen mit Dateinamen und Pfad ab dem Verzeichnis des Moduls angegeben werden (oxtplblocks:OXFILE).
* Beispiel
* : :file:`/views/blocks/checkoutUserForm.tpl` anstatt nur mit dem Dateinamen :file:`checkoutUserForm.tpl`. Besteht das Modul nur aus einer Datei und hat kein eigenes Verzeichnis, muss Dateiname und Pfad :file:`/modules/{file_name}` lauten. Dateinamen ohne Pfad werden noch für einige Zeit unterstützt.
* Sprachdateien für das Frontend wurden vom Verzeichnis :file:`/out/lang/{local}` des Moduls nach :file:`/translations/{local}` verschoben. Die frühere Struktur wird noch für einige Zeit unterstützt.
* Sprachdateien für den Administrationsbereich wurden vom Verzeichnis :file:`/out/admin/{local}` des Moduls nach :file:`/views/admin/{local}` verschoben. Die frühere Struktur wird noch für einige Zeit unterstützt.

Die Moduleinstellungen können jetzt geändert werden, ohne dass dafür das Module aktiviert werden muss.

Nicht mehr unterstützt
++++++++++++++++++++++

* Alle in vorhergehenden Shop-Versionen als
* \"
* deprecated
* \"
* gekennzeichneten Funktionen, Variablen und Codestellen wurden entfernt. Siehe dazu die Übersicht
*  `Removed deprecated source <http://wiki.oxidforge.org/Tutorials/Removed_deprecated_source>`_ 
* in der OXIDforge.
* Das Theme
* \"
* Basic
* \"
* wird nicht mehr gewartet und nicht veröffentlicht.
* Die Zend Platform wird nicht länger unterstützt, da dieses Produkt von Zend eingestellt wurde. Die Unterstützung für den Zend Server bleibt bestehen.

Korrekturen
-------------
Korrekturen 4.7.0/5.0.0 Final: `https://bugs.oxid-esales.com/changelog_page.php?version_id=164 <https://bugs.oxid-esales.com/changelog_page.php?version_id=164>`_ 

Korrekturen 4.7.0/5.0.0 RC 2: `https://bugs.oxid-esales.com/changelog_page.php?version_id=162 <https://bugs.oxid-esales.com/changelog_page.php?version_id=162>`_ 

Korrekturen 4.7.0/5.0.0 RC 1: `https://bugs.oxid-esales.com/changelog_page.php?version_id=159 <https://bugs.oxid-esales.com/changelog_page.php?version_id=159>`_ 

Korrekturen 4.7.0/5.0.0 Beta 3: `https://bugs.oxid-esales.com/changelog_page.php?version_id=156 <https://bugs.oxid-esales.com/changelog_page.php?version_id=156>`_ 

Korrekturen 4.7.0/5.0.0 Beta 2: `https://bugs.oxid-esales.com/changelog_page.php?version_id=146 <https://bugs.oxid-esales.com/changelog_page.php?version_id=146>`_ 

Korrekturen 4.7.0/5.0.0 Beta 1: `https://bugs.oxid-esales.com/changelog_page.php?version_id=132

 <https://bugs.oxid-esales.com/changelog_page.php?version_id=132>`_

Weiterführende Informationen für Entwickler finden Sie auf der `OXIDforge <http://oxidforge.org/en/oxid-eshop-version-4-7-0-ce-pe-5-0-0-ee.html>`_ .