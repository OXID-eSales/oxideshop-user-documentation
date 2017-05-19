OXID eShop 4.6.0
****************
Versionsbezeichnung: 4.6.0, Revision 44406

Veröffentlichungstermin: 26.04.2012

Neue Funktionen
---------------

Download-Artikel
++++++++++++++++
Der OXID eShop 4.6.0 stellt einen neuen Artikeltyp als Standard bereit: Download-Artikel. Mit Download-Artikeln kann der Shopbetreiber beispielsweise Software, Fotos, Musikdateien oder Dokumentvorlagen anbieten. Legt der Kunde einen Download-Artikel in den Warenkorb, erwirbt er alle dazugehörigen Dateien. Nach Abschluss des Bestellvorgangs finden sich alle Downloads unter :guilabel:`Konto --> Meine Downloads`.

Die Verwendung von Download-Artikeln im Shop muss global aktiviert werden. Im Administrationsbereich können unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Download-Artikel` die Standardeinstellungen vorgenommen werden. Das sind - neben dem Aktivieren der Funktion - der Pfad zu den herunterladbaren Dateien und Festlegungen zur Anzahl der Downloads oder zur Verfallszeit der Links.

Für jeden Download-Artikel und für jede einzelne Datei können die Werte abweichend von den Standardeinstellungen festgelegt werden. Das erlaubt eine sehr filigrane Definition der Bedingungen für den Download.

Unterstützung von RDFa und GoodRelations
++++++++++++++++++++++++++++++++++++++++
Mit Rich Snippets, basierend auf dem Resource Description Framework (RDFa) und der für den E-Commerce optimierten Beschreibungssprache GoodReleations, werden Informationen aus dem OXID eShop gut aufbereitet für Suchmaschinen bereitgestellt. Suchmaschinen können Angaben zu Firma, Zahlungsarten, Versandarten und zu den Artikeldetails effizienter verarbeiten und verwerten. Als Ergebnis könnten Onlineshops mit RDFa-Unterstützung ein verbessertes Ranking bei den Suchmaschinen erreichen.

RDFa ist ausschließlich im Theme \"Azure\" verfügbar. Damit der Shop die RDFa-Integration verwenden kann, muss die Funktion unter :menuselection:`Stammdaten --> Grundeinstellungen --> RDFa` aktiviert werden. Auf dieser Registerkarte werden auch die firmenbezogenen Daten, Zahlungsarten, Versandarten und Artikeldetails zugewiesen sowie spezielle Shopdaten definiert. Dazu zählen Informationen, welche CMS-Seiten zu Firma, Zahlungs- und Versandarten Auskunft geben, und detaillierte Angaben zu den im Shop verkauften Artikeln.

Bei den Zahlungsarten und den Versandarten wird in der Registerkarte RDFa eine logische Verknüpfung mit den in GoodReleations vordefinierten Werten für Zahlung und Versand hergestellt.

Modul-Handling
++++++++++++++
Module, die im Shop installiert wurden, lassen sich jetzt im Administrationsbereich verwalten. Unter :menuselection:`Erweiterungen --> Module` findet sich eine Liste aller Module, die den Shop funktional erweitern.

Der Shop ermittelt diese Liste aller Module automatisch. Voraussetzung dafür ist, dass jedes Modul in einem separaten Unterverzeichnis unter :file:`/modules` gespeichert ist. Eine im Aufbau standardisierte Metadatei sorgt dafür, dass im Administrationsbereich Details und Einstellungen der Module angezeigt werden. Per Drag \& Drop kann die Reihenfolge geändert werden, in welcher der Shop die Module laden soll. Module lassen sich komfortabel aktivieren und deaktivieren.

Zeitgesteuerte Aktualisierung von Artikelpreisen
++++++++++++++++++++++++++++++++++++++++++++++++
Preise können zu einem festgelegten Zeitpunkt geändert werden. Unter :menuselection:`Artikel verwalten` --> :menuselection:`Artikel`\> :guilabel:`Erweitert` lassen sich Datum und Zeitpunkt festlegen, ab dem die definierten Standardpreise aktualisiert werden sollen.

Verbesserungen und Anpassungen
------------------------------

Steigerung der Performance
++++++++++++++++++++++++++
Die Performance des OXID eShop in Hochlastszenarien konnte deutlich erhöht werden. Eine Performancesteigerung von bis zu 30 Prozent wurde durch die Reduzierung von SQL-Abfragen pro Seitenaufruf, Feintuning vom Caching und durch Optimierungen im PHP-Code erreicht.

Für den Shopbetrieb kann jetzt unter :menuselection:`Stammdaten --> Grundeinstellungen --> Perform.` der SEO Cache aktiviert werden. SEO Abfragen werden dadurch im :file:`/tmp`-Verzeichnis zwischengespeichert. Dies verbessert die Performance, benötigt aber ausreichenden Speicherplatz.

Bestellstatus NOT_FINISHED
++++++++++++++++++++++++++
Der Bestellstatus NOT_FINISHED wurde hinzugefügt. Er wird zu Beginn der Bestellung gesetzt. Erst wenn die Bestellung erfolgreich abgeschlossen wird, ändert sich der Bestellstatus auf OK.

Überarbeitetes Layout bei Bestellungen
++++++++++++++++++++++++++++++++++++++
Das Layout der Registerkarte :guilabel:`Stamm` wurde umgestellt, so dass alle Bezahl- und Versandinformationen übersichtlich zusammengefasst wurden.

Facebook-Funktion \"Live Stream\" entfernt
++++++++++++++++++++++++++++++++++++++++++
Nach einer Umfrage im Community Forum wurde die Facebook-Funktion \"Live Stream\", mit der Besucher des Shops in Echtzeit über Produkte diskutieren sollten, entfernt. Die Funktion ist unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Facebook` nicht mehr verfügbar.

Korrekturen
-----------
Korrekturen 4.6.0 Final: `https://bugs.oxid-esales.com/changelog_page.php?version_id=129 <https://bugs.oxid-esales.com/changelog_page.php?version_id=129>`_ 

Korrekturen 4.6.0 RC 2: `https://bugs.oxid-esales.com/changelog_page.php?version_id=126 <https://bugs.oxid-esales.com/changelog_page.php?version_id=126>`_ 

Korrekturen 4.6.0 RC 1: `https://bugs.oxid-esales.com/changelog_page.php?version_id=123 <https://bugs.oxid-esales.com/changelog_page.php?version_id=123>`_ 

Korrekturen 4.6.0 Beta 3: `https://bugs.oxid-esales.com/changelog_page.php?version_id=110 <https://bugs.oxid-esales.com/changelog_page.php?version_id=110>`_ 

Korrekturen 4.6.0 Beta 2: `https://bugs.oxid-esales.com/changelog_page.php?version_id=95 <https://bugs.oxid-esales.com/changelog_page.php?version_id=95>`_ 

Korrekturen 4.6.0 Beta 1: `https://bugs.oxid-esales.com/changelog_page.php?version_id=106 <https://bugs.oxid-esales.com/changelog_page.php?version_id=106>`_

Auch alle Korrekturen aus den Patches von 4.5 wurden in die Version 4.6.0 übernommen.

Weiterführende Informationen für Entwickler finden Sie auf der `OXIDforge <http://oxidforge.org/en/oxid-eshop-version-4-6-0.html>`_ .

.. Intern: oxaaab, Status: