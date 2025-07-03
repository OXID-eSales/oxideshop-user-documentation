:orphan:
System
======

Legen Sie Konfigurationsoptionen im OXID eShop fest, die für den Betrieb und die Anpassung Ihres Online-Shops relevant sind.

Konfigurieren Sie Bestellungen, Variantenmanagement, Bildverwaltung und Einstellungen im Administrationsbereich.

.. todo: #tbd: adjust redirect anlegen: OXID-eSales/documentation-redirect-handler at b-7.x


|procedure|

1. Wählen Sie :mensuselection:`Stanndaen --> Grundeinstellungen`.
#. Wählen Sie die Registerkarte :guilael:`System`.




Bestellungen
------------



* Bestellungen aus dem Ausland auch dann erlauben, wenn keine Versandkosten für das Land vorhanden sind.

  Diese Einstellung beeinflusst das Verhalten des OXID eShops, wenn für ein Land, in das Benutzer bestellen wollen, keine Versandkosten definiert sind:
  * Wenn die Einstellung aktiv ist, erhalten diese Benutzer im Bestellprozess eine Meldung: Die Versandkosten werden ihnen nachträglich mitgeteilt, wenn Sie damit einverstanden ist. Sie können mit der Bestellung fortfahren.
  * Wenn die Einstellung ausgeschaltet ist, können Benutzer aus Ländern, für die keine Versandkosten definiert sind, nicht bestellen.

* Einige Navigationselemente während des Bestellprozesses ausblenden.

  Wenn Sie diese Einstellung aktivieren, werden die meisten Navigationselemente im Bestellprozess ausgeblendet. Dadurch werden die Benutzer beim Bestellen nicht unnötig abgelenkt.

* IP-Adressen speichern (Achtung: Dies kann gegen Datenschutzbestimmungen verstoßen).
* Benutzer müssen sich registrieren, um bestellen zu können.

Varianten
---------

.. todo: #SB: Was sind die Anwendungsfälle für diese Aktionen?
        Nur einige Punkte sind woanders erwähnt

* Varianten im Administrationsbereich in Zuordnungs-Listen anzeigen

  Im eShop gibt es oft Listen, in denen Sie Artikel zuordnen können, z. B. wenn Sie Artikel zu Rabatten zuordnen. Wenn die Einstellung aktiv ist, werden in diesen Listen auch Varianten angezeigt.

* Varianten-"Vater" ist kaufbar

  Hier können Sie einstellen, ob der Vater-Artikel gekauft werden kann:

  * Wenn die Einstellung aktiv ist, kann auch der Vater-Artikel gekauft werden.
  * Wenn die Einstellung nicht aktiv ist, können nur die Varianten gekauft werden.

* Varianten erben Staffelpreise vom "Vater"

  einrichtung/artikel-und-kategorien/staffelpreise.rst

  Diese Einstellung beeinflusst das Verhalten des eShops, wenn beim Vater-Artikel Staffelpreise eingerichtet sind: Wenn die Einstellung aktiv ist, werden die Staffelpreise auch bei den Varianten verwendet.

* Varianten-Bewertungen beim "Vater"-Artikel anzeigen

  Diese Einstellung beeinflusst das Verhalten, wenn Varianten bewertet werden: Wenn die Einstellung aktiv ist, dann werden die Bewertungen der Varianten auch beim Vater-Artikel angezeigt.

* Multidimensionale Varianten einschalten

  einrichtung/artikel/registerkarte-varianten.rst

  ist standardmäßig aktiv, in welchem Fall deaktiviere ich das? Was wäre der Vorteil?

Bilder
------

.. todo: #SB: Was sind die Anwendungsfälle für diese Aktionen?
    Nur einige Punkte sind woanders erwähnt

* Bildqualität von 0 (schlechteste Qualität, kleine Dateigröße) bis 100 (beste Qualität, große Dateigröße) einstellbar.

  Empfehlenswerte Einstellungen sind ca. 40-80:

  Unterhalb von ca. 40 werden deutliche Kompressionsartefakte sichtbar, und die Bilder wirken unscharf.

  Oberhalb von ca. 80 kann man kaum eine Verbesserung der Bildqualität feststellen, während die Dateigröße enorm zunimmt.

  Die Standardeinstellung ist 75.

* Bilder automatisch ins WebP-Format konvertieren

  konfiguration/bilder.rst

  Empfohlen: Aktivieren Sie die WebP-Konvertierung, damit die Seiten Ihres OXID eShops schneller geladen werden.

  Prüfen Sie jedoch, ob die Qualität Ihrer Bilder durch die im Vergleich mit dem JPG-Format stärkere Kompression beeinträchtigt wird.

  Deaktivieren Sie die WebP-Konvertierung gegebenenfalls wieder.

* E-Mails mitsamt Bildern versenden: E-Mails mitsamt Bildern

  #SB: in welchem FAll will ich das? Wenn die Einstellung aktiv ist, werden die Bilder, die in E-Mails verwendet werden, zusammen mit der E-Mail versendet.

  Wenn die Einstellung nicht aktiv ist, lädt das E-Mail Programm die Bilder herunter, wenn Benutzer die E-Mail öffnen.

Administrationsbereich
----------------------

.. todo: #SB: Was sind die Anwendungsfälle für diese Aktionen?


* Profile für den Administrationsbereich je nach Bildschirmauflösung (z.B. 1024x768, 1280x1024, 1600x1200).

  .. todo: #SB: Wozu sind diese Zurodnungen?
    Standard => 10
    1024x768 => 10
    1280x1024 => 17
    1600x1200 => 22

* Zeitverschiebung des Servers in Stunden einstellen.

  Es kann sein, dass sich der Server in einer anderen Zeitzone befindet. Mit dieser Einstellung können Sie die Zeitverschiebung korrigieren: Geben Sie die Anzahl der Stunden, die zur Serverzeit addiert/abgezogen werden sollen ein, z. B. +2 oder -2

* Option "Passwort merken" beim Login anzeigen.

  #SB: Standardm. aktiv; in welchem FAll wll ich das nicht?

* Prozentsatz gleicher Attribute, damit Artikel als ähnlich gelten.

  #SB: Sollte relevant sein unter :ref:`einrichtung/attribute/attribute:Ähnliche Produkte anzeigen`, aber da kommt es nicht vor.

* Artikelbewertungen moderieren: Veröffentlichung erst nach Freigabe durch einen Administrator

  #SB: Sollte relevant sein unter einrichtung/artikel/registerkarte-bewertung.rst, aber da kommt es nicht vor.

* Diese Änderungen im Administrationsbereich nicht mitloggen.

  #SB: Was gebe ich in das Text-Eingabefeld ein? In welchem Fall?

Weitere Einstellungen
---------------------

* Zusätzliches Util-Modul aktivieren

  Bitte tragen Sie Ihre .php-Datei ein, mit der beim Shopstart eShop Funktionen überschrieben werden sollen.


