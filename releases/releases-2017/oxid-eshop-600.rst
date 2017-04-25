OXID eShop 6.0.0
****************
Versionsbezeichnung: 5.2.0

Edition: Enterprise Edition

Versionsbezeichnung: 4.9.0

Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 30.09.2014

Veröffentlichungstermin RC 2: 18.09.2014

Veröffentlichungstermin RC 1: 16.09.2014

Veröffentlichungstermin Beta 1: 19.08.2014\

Allgemeines
-----------
Der OXID eShop 4.9.0/5.2.0 wird mit der OXID eFire Extension PayPal (Standalone-Modul) in Version 3.2.0 und dem Mobile Theme Version 1.3.0 ausgeliefert. Er läuft unter PHP 5.3 und PHP 5.4. Die Shopversion enthält einige Sicherheitsverbesserungen, so dass wir ein baldmöglichstes Update empfehlen.

Installation
++++++++++++
Für die Installation, folgen Sie bitte den Anleitungen in der Dokumentation und Hilfe:

`OXID eShop neu installieren <de/support-services/dokumentation-und-hilfe/oxid-eshop/installation/oxid-eshop-neu-installieren/server-und-systemvoraussetzungen.html>`_ 

 `OXID eShop aktualisieren <de/support-services/dokumentation-und-hilfe/oxid-eshop/installation/oxid-eshop-aktualisieren/update-vorbereiten.html>`_

Hinweis: Wir empfehlen dringend, das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, auszuführen. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

Neue Funktionen
---------------

Bis zu 1.500 Subshops möglich (Enterprise Edition)
++++++++++++++++++++++++++++++++++++++++++++++++++
Die Mandantenfähigkeit wurde komplett überarbeitet. Bisher unterstützte der OXID eShop Enterprise Edition etwa 200 Subshops. Ab der Version 5.2.0 sind bis zu 1.500 Subshops möglich.

Für die signifikante Steigerung der Anzahl von Mandanten waren Änderungen an der Kernfunktionalität, der Datenbank und der Templates notwendig. Die Präsentation des Warenkataloges in den einzelnen Subshops wird nicht mehr länger durch die Datenbankfelder *OXSHOPINCL*  und *OXSHOPEXCL*  gehandhabt. Alle Datenbanktabellen, die für die Abbildung von Subshops notwendig sind, erhielten sogenannte Mapping-Tabellen. *Beispiel* : Tabelle für die Artikel *oxarticles*  und deren Mapping-Tabelle *oxarticles2shop* .

Prüfung auf Metadaten von Modulen
+++++++++++++++++++++++++++++++++
Im Administrationsbereich des OXID eShop wird bisher geprüft, ob alle zu einem Modul gehörenden Dateien vorhanden sind. Jetzt wird auch festgestellt, ob die Dateimetadata.phpvorhanden ist. Fehlt diese, bietet der Shop wie bisher an, alle Modulinformationen und gespeicherten Einstellungen zu löschen.

Script zum Generieren von Metadaten
+++++++++++++++++++++++++++++++++++
Mit OXID eShop 4.9.0/5.2.0 wird das Vorhandensein von Metadaten bei Modulen zwingend vorausgesetzt. Um Modulhersteller bei der Anpassung ihrer Module an neue Shopversionen zu unterstützen, wird ein Script bereitgestellt, welches die Dateimetadata.phperstellt. Dabei werden die Einstellungen umgesetzt, die in der Tabelle *oxconfig*  der Datenbank nach der Aktivierung des Moduls gespeichert wurden.

Das Script kann vor oder nach dem Update des Shops ausgeführt werden.

Weitere Informationen und die Möglichkeit zum Download finden Sie auf GitHub:

 `https://github.com/OXIDprojects/metadataGenerator <https://github.com/OXIDprojects/metadataGenerator>`_ .

Prüfung der USt-ID-Nummer jetzt auch in CE und PE
+++++++++++++++++++++++++++++++++++++++++++++++++
Auch in der Community und Professional Edition wird die USt-ID-Nummer jetzt online geprüft, sobald eine Firma im Shop bestellt. Firma, Land und USt-Identifikationsnummer müssen für die Prüfung angegeben worden sein.

Verbesserungen und Anpassungen
------------------------------

Änderungen in der Datenbank
+++++++++++++++++++++++++++
Die Tabellenfelder *OXSHOPINCL*  und *OXSHOPEXCL*  wurden aus den Datenbanktabellen entfernt. Sie waren in einer Enterprise Edition bisher für die Zuordnung beispielsweise von Artikeln, Kategorien oder Versandarten zu den einzelnen Subshops notwendig. Mit der neuen Multishop-Lösung werden sie nicht mehr benötigt, ebensowenig, wie die für die Verarbeitung zuständigen Methoden.

Die Länge der Tabellenfelder *OXEAN*  und *OXDISTEAN*  der Tabelle *oxarticles*  wurde geändert. Der Tabelle *oxcountry*  wurde das Tabellenfeld *OXVATINPREFIX*  hinzugefügt, welches das Prefix der Umsatzsteuer-Identnummer aufnimmt.

Detaillierte Informationen entnehmen Sie bitte den Informationen für Entwickler auf der `OXIDforge <http://oxidforge.org/en/oxid-eshop-version-4-9-0-ce-pe-5-2-0-ee.html>`_ .

Änderungen in .php-Dateien
++++++++++++++++++++++++++
Mit den Standards PSR-1 und PSR-2 wurden neue Programmierrichtlinien bereits teilweise im OXID eShop umgesetzt. Aus diesem Grund werden Sie bei einem Update sehr viele .php-Dateien geändert vorfinden. Wir bitten, die dadurch entstehenden Unannehmlichkeiten zu entschuldigen. Die neuen Programmierrichtlinien werden in Kürze von uns veröffentlicht und als OXID Software Development Kit Teil 2 bereitgestellt.

Klassen, die für Funktionen von OXID eFire notwendig waren, wurden entfernt.

Änderungen in Templates
+++++++++++++++++++++++
Es gab Änderungen in Templates und Sprachdateien des Themes \"Azure\" und des Administrationsbereiches. Dabei wurde u.a. in den Templates für die Hauptseiten des eShop das Erstellen des Seitentitels umgestellt. Der Seitentitel wird nicht mehr selbst im Template zusammengesetzt, sondern über eine Methode ermittelt. Für mehr Informationen beachten Sie bitte die Informationen für Entwickler auf der `OXIDforge <http://oxidforge.org/en/oxid-eshop-version-4-9-0-ce-pe-5-2-0-ee.html>`_ .

Templates, die für OXID eFire notwendig waren, wurden entfernt.

Eine Übersicht aller Änderungen finden Sie in der Template-Dokumentation/templ_docu_admin/index.htmlund/templ_docu_azure/index.htmldes Installationspaketes.

Optimierte Performance
++++++++++++++++++++++
Vor allem in der Enterprise Edition konnte die Performance weiter gesteigert werden. Dazu führten die Implementierung der neuen Multishop-Lösung, Änderungen im Caching mit Varnish sowie das Entfernen einiger verbliebenen Verweise auf die Dateioxeec_class_file_paths.php. Kunden, die eine Enterprise Edition mit Hochlastoption einsetzen, finden eine aktualisierte Konfigurationsdateidefault.vlcim Abschnitt \"Caching\" der EE-Dokumentation.

Auch die Schnelligkeit der Community und Professional Edition profitiert von einigen Änderungen. Ein Performance- und Qualitätsbericht wird mit konkreten Maß- und Kennzahlen in Kürze veröffentlicht werden.

Sicherheitsverbesserungen
+++++++++++++++++++++++++
Die Möglichkeit, Benutzergruppen dynamisch via URL-Parameter \"dgr\" zuzuordnen, wurde entfernt.

Die automatische Prüfung auf einen Security Token wird nun bei angemeldeten Benutzern für alle Formulare und Aktions-URLs ausgeführt. Einzige Ausnahme ist der Aufruf *fnc=tobasket* , um auch nicht angemeldeten Benutzern über einen Link Artikel in den Warenkorb legen zu können.

Kunden können sich nicht mehr länger mit ihrer Kundennummer an den Shop anmelden. Damit wird die Sicherheit verbessert, denn einem potentiellen Angreifer würde es leichter fallen, mit einem Script eine Nummer herauszufinden als eine Zeichenfolge.

Passwörter wurden bisher mit der kryptographische Hashfunktion MD5 und einem zusätzlichen Salt verschlüsselt. Die Verschlüsselung wurde auf die aktuellere kryptographische Hashfunktion SHA-2 umgestellt und das Erzeugen der als Salt bezeichneten, zufällig gewählten Zeichenfolge leicht geändert. Die Kunden können sich wie gewohnt am Shop anmelden, ohne ein neues Passwort erstellen zu müssen.

Detaillierte Informationen entnehmen Sie bitte den Informationen für Entwickler auf der `OXIDforge <http://oxidforge.org/en/oxid-eshop-version-4-9-0-ce-pe-5-2-0-ee.html>`_ .

Zeichensatz UTF-8 ist Standard
++++++++++++++++++++++++++++++
War der Zeichensatz UTF-8 bisher bei der Neu-Installation optional, ist er nunmehr standardmäßig vorausgewählt.

Verbindung des Shops zu OXID Servern
++++++++++++++++++++++++++++++++++++
Mit der OptionVerbindung mit den OXID Servern erlaubenkönnen wie bisher zusätzliche Produktinformationen im Administrationsbereich angezeigt werden (eCommerce Services). Auch über Updates für den Shop und die installierten Module soll zukünftig bei aktivierter Option informiert werden. Für die Professional und die Enterprise Edition soll dann auch die verwendete Lizenz online geprüft werden.

Bitte beachten Sie, dass in keinem Fall geschäftsrelevante Daten (Benutzer, Umsatz etc.) übermittelt werden.

Sendungsverfolgung für bevorzugten Versanddienstleister
+++++++++++++++++++++++++++++++++++++++++++++++++++++++
Damit Kunden den Versand ihrer bestellten Ware verfolgen können, kann die Tracking-URL des Versanddienstleisters im Administrationsbereich unterStammdaten-\>Grundeinstellungen-\>Einstell.-\>Weitere Einstellungeneingetragen werden. Bisher konnte ausschließlich die Sendungsverfolgung von DPD (Dynamic Parcel Distribution) genutzt werden. Die neue Funktion wurde vom Partner ProudCommerce realisiert und als `GitHub Contribution <https://github.com/OXID-eSales/oxideshop_ce/pull/94>`_ eingereicht.

Geänderte Prüfung der E-Mail-Adresse
++++++++++++++++++++++++++++++++++++
Die Prüfung einer durch den Kunden angegebenen E-Mail-Adresse wurde vereinfacht. Erlaubt sind standardmäßig längere Namen für die Top-Level-Domänen und das Pluszeichen. Geprüft wird darauf, ob die E-Mail-Adresse aus drei Teilen besteht, die durch die Zeichen '@' and '.' getrennt sind. Für die Prüfung ist die Klasse\"oxMailValidator\"unter Verwendung des Konfigurationsparameters\"sEmailValidationRule\"zuständig. Bei Bedarf können eigene Rollen für die Prüfung definiert oder die Klasse erweitert werden.

Feld zur Passworteingabe in den Moduleinstellungen
++++++++++++++++++++++++++++++++++++++++++++++++++
Manche Module, beispielsweise die OXID eFire Extension PayPal, benötigen die Eingabe und Speicherung von Passwörtern. Damit nicht jeder Benutzer ein gesetztes Passwort in den Moduleinstellungen sehen kann, wurden Felder für die Passworteingabe und -bestätigung implementiert. Wie üblich, werden bei der Eingabe des Passwortes nur Sternchen anstelle der tatsächlichen Zeichen angezeigt.

Alle übrigen Moduleinstellungen können stets ohne erneute Passworteingabe geändert werden.

Export für Datenträgeraustauschverfahren (DTAUS) entfernt
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++
In der Community und der Professional Edition konnten Bestellungen mit der Zahlungsart\"Bankeinzug/Lastschrift\"für eine Verarbeitung bei Banken und Geldinstituten exportiert werden. Mit dieser Veröffentlichung wurde die Möglichkeit zum Erstellen von Lastschrifteinzugssätzen für die elektronische Verarbeitung im Datenträgeraustauschverfahren (DTAUS) entfernt. Dieses Verfahren wird seit August 2014 von den Banken nicht mehr unterstützt.

Korrekturen
-------------
Korrekturen 4.9.0/5.2.0: `http://bugs.oxid-esales.com/changelog_page.php?version_id=265 <http://bugs.oxid-esales.com/changelog_page.php?version_id=265>`_

Korrekturen 4.9.0/5.2.0 RC 2: `https://bugs.oxid-esales.com/changelog_page.php?version_id=264 <https://bugs.oxid-esales.com/changelog_page.php?version_id=264>`_ 

Korrekturen 4.9.0/5.2.0 RC 1: `https://bugs.oxid-esales.com/changelog_page.php?version_id=262 <https://bugs.oxid-esales.com/changelog_page.php?version_id=262>`_ 

Korrekturen 4.9.0/5.2.0 Beta 1: `https://bugs.oxid-esales.com/changelog_page.php?version_id=228 <https://bugs.oxid-esales.com/changelog_page.php?version_id=228>`_ 

`<https://bugs.oxid-esales.com/changelog_page.php?version_id=132>`_

Weiterführende Informationen für Entwickler finden Sie auf der `OXIDforge <http://oxidforge.org/en/oxid-eshop-version-4-9-0-ce-pe-5-2-0-ee.html>`_ .