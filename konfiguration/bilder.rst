Bilder
======

Ordnen Sie Artikeln bis zu zwölf Artikelbilder zu, die in der Detailansicht des Artikels angezeigt werden.

Artikel haben Zoombilder, die ebenfalls auf der Detailseite aufrufbar sind. Legen Sie global oder auf Kategorienebene oder für individuelle Produkte fest, welche Art von Zoom Sie nutzen wollen.

Kleinere Artikelbilder zeigen den Artikel in den Artikellisten, in Produktboxen und im Warenkorb. Alle benötigten Bildarten werden automatisch generiert. Legen Sie die gewünschten Bildgrößen und die Bildqualität fest.

Legen Sie fest, ob Bestellbestätigungen mit Bildern gesendet werden sollen.

Bildgenerierung und -qualität festlegen
---------------------------------------
Die erforderlichen Einstellungen für die Bildgenerierung und für die Bildgrößen werden für alle Artikel im Administrationsbereich vorgenommen.

Grundeinstellungen anzeigen
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Prüfen Sie bei Bedarf die Version der Software, die für das dynamische Erzeugen von Bildern zuständig ist.

|procedure|

1. Wählen Sie unter :menuselection:`Stammdaten --> Grundeinstellungen` die Registerkarte :guilabel:`Einstell.`
#. Klicken Sie auf :guilabel:`Bilder`, um die Einstellungen anzuzeigen.

   * Prüfen Sie Version der GDLib, der Software auf dem Server, die Grafiken dynamisch erzeugt.
   * Prüfen Sie, ob das automatische Generieren von Icons aktiviert ist.

   Lassen Sie beide Einstellungen unverändert.

Bildqualität festlegen
^^^^^^^^^^^^^^^^^^^^^^

Erhöhen Sie bei Bedarf die Geschwindigkeit, mit der Seiten im Browser geladen werden.

|procedure|

1. Wählen Sie unter :menuselection:`Stammdaten --> Grundeinstellungen` die Registerkarte :guilabel:`System.`.
#. Wählen Sie den Abschnitt :guilabel:`Bilder`.

   Sie haben folgende Möglichkeiten:

   * :guilabel:`Bildqualität`: Legen Sie die Bildqualität beim Generieren der Bilder fest.

     Die Standardeinstellung ist 75 und ist ein guter Kompromiss zwischen Bildqualität und Dateigröße.

     Bei einem deutlich kleineren Wert sind die Artikelbilder stark komprimiert, haben daher eine kleine Dateigröße, aber eine schlechte Bildqualität (Unschärfen und Kompressionsartefakte).

     Ist der Wert größer als 75, steigt die Bildqualität, aber auch die Größe der Datei (längere Ladezeiten).

* :guilabel:`Bilder automatisch ins WebP-Format konvertieren`: Erhöhen Sie die Browser-Geschwindigkeit.

  Konvertieren Sie dazu die Bilder automatisch ins Bildformat WebP.

Bestellbestätigungen mit Bildern senden
---------------------------------------

Entscheiden Sie, ob Bestellbestätigungen Bilder enthalten sollen.

|background|

E-Mails mit Artikelbildern können schnell groß werden, was zu Problemen beim Versand und beim Empfang der Mail führen kann.

Standardmäßig werden E-Mails ohne Artikelbilder versendet.

Die Artikelbilder werden beim Lesen der E-Mail durch das Mail-Programm des Kunden nachgeladen.

|procedure|

1. Wählen Sie unter :menuselection:`Stammdaten --> Grundeinstellungen` die Registerkarte :guilabel:`System.`.
#. Wählen Sie den Abschnitt :guilabel:`Bilder`.
#. Um Artikelbilder in Bestellbestätigung zu senden, aktivieren Sie das Kontrollkästchen :guilabel:`E-Mails mitsamt Bildern versenden`.


Bildgrößen festlegen
--------------------
Die Größe der Bilder für Artikel, Kategorien und für Hersteller- und Markenlogos ist abhängig vom Design Ihres OXID eShops.

Die Einstellungen sind daher beim aktiven Theme hinterlegt.

|procedure|

1. Wählen Sie unter :menuselection:`Erweiterungen --> Themes` das Theme.
#. Wählen Sie die Registerkarte :guilabel:`Einstell.`, und wählen Sie :guilabel:`Bilder`.

   Sie haben folgende Möglichkeiten, die Bildgrößen anzupassen:

   * :guilabel:`Größe des Icons in Pixeln (Breite*Höhe)`

     Icons sind die kleinsten Artikelbilder und werden im Warenkorb und in Produktboxen (Beispiel: Top of the Shop) verwendet.

     Standardgröße: 87 Pixel breit und 87 Pixel hoch.

   * :guilabel:`Größe des Thumbnails in Pixeln (Breite*Höhe)`

     Thumbnails sind Vorschaubilder und werden in Artikellisten, wie Kategorie-Übersichten und Suchergebnisse, und in Aktionen (Beispiel: Frisch eingetroffen!) angezeigt.

     Standardgröße: 185 Pixel breit und 150 Pixel hoch.

   * :guilabel:`Größe des Kategoriebildes in Pixeln (Breite*Höhe)`

     Bild für die Anzeige der Kategorie-Übersicht.

     Standardgröße: 784 Pixel breit und 150 Pixel hoch.

   * :guilabel:`Größe der Zoom-Bilder (Zoom 1-4) in Pixeln (Breite*Höhe)`

     Vergrößerte Anzeige eines Artikelbildes, die sich auf der Detailseite aufrufen lässt.

     Standardgröße: 665 Pixel breit und 665 Pixel hoch.

   * :guilabel:`Größe der Artikelbilder (Bild 1-12) in Pixeln (Breite*Höhe)`

     Artikelbild, welches auf der Detailseite angezeigt wird.

     Die Größe von bis zu 12 Artikelbilder kann definiert werden.

     Dadurch sind Artikelbilder mit unterschiedlichen Größen möglich.

     Für jedes Artikelbild gibt es eine Zeile, an deren Anfang ``oxpic`` und eine Zahl steht. ``oxpic1`` steht für das erste Artikelbild, ``oxpic2`` für das zweite Artikelbild usw.

     Standardgröße: 380 Pixel breit und 340 Pixel hoch.

     .. hint:: Verwendden Sie die Möglichkeit unterschiedlicher Bildgrößen mit Umsicht

        Verschieden große Artikelbilder könnten eventuell zu einer eher unprofessionell wirkenden Präsentation der Artikel führen.

   * :guilabel:`Größe des Hersteller-/Markenlogos in Pixeln (Breite*Höhe)`

     Logo, das in der Marken-Übersicht auf der Startseite angezeigt wird.

     Standardgröße: 100 Pixel breit und 100 Pixel hoch.

   * :guilabel:`Größe des Kategoriebildes einer Unterkategorie in Pixeln (Breite*Höhe)`

     Bild für die Anzeige von Unterkategorien in der Kategorie-Übersicht.

     Standardgröße: 168 Pixel breit und 100 Pixel hoch.

   * :guilabel:`Größe des Kategoriebildes für die Startseite in Pixeln (Breite*Höhe)`

     Bild der Kategorie, die auf der Startseite beworben wird.

     Standardgröße: 370 Pixel breit und 107 Pixel hoch.

Zoom wählen
-----------

Beeinflussen Sie je nach Anwendung und Produkt die Kaufbereitschaft positiv, indem Sie beim APEX-Theme mit einer von drei Arten, Bilder zu vergrößern, unterschiedliche psychologische Bedürfnisse der Kunden ansprechen.

* Hover-Zoom: Diese Funktion bietet eine interaktive Möglichkeit, Produktbilder im Detail zu betrachten.

  Wenn der Mauszeiger über das Bild fährt, wird es vergrößert, und die Vergrößerung folgt der Mausbewegung.

  Der Hover-Zoom bietet sich an für Shops mit einer breiten Produktpalette, in denen Kunden häufig zwischen verschiedenen Produkten wechseln. Die interaktive Natur des Hover-Zooms kann das Nutzererlebnis verbessern und die Verweildauer erhöhen.

  Der Hover-Zoom fördert Neugier und Engagement, was zu schnelleren, emotional getriebenen Kaufentscheidungen führen kann.

* Modal-Zoom: Beim Klick auf das Produktbild wird dieses in einem größeren Modal-Fenster geöffnet, in dem weitere Details sichtbar werden.

  Zusätzlich kann der Nutzer innerhalb des Modals nochmals in das Bild hineinzoomen, um besonders feine Details zu erkennen.

  Dies bietet eine umfassende Möglichkeit, Produkte genau unter die Lupe zu nehmen.

  Der Modal-Zoom vermittelt Vertrauen und Sicherheit, unterstützt rationale Entscheidungen und stärkt das Vertrauen in die Produktqualität.

* Lupen-Zoom: Hier wird eine Lupenfunktion aktiviert, wenn der Mauszeiger über das Bild fährt (:ref:`oxbaaz01`).

  Ein separater Bereich zeigt eine stark vergrößerte Ansicht des Bildausschnitts direkt unter dem Mauszeiger.

  Dies ermöglicht eine präzise Betrachtung spezifischer Produktdetails, ohne das gesamte Bild zu vergrößern.

  Der Lupen-Zoom betont Präzision und Qualität, was besonders bei Kunden gut ankommt, die auf Details und Spezifikationen achten, und kann so das Vertrauen in spezifische Produkteigenschaften stärken.

  .. _oxbaaz01:

  .. figure:: ../media/screenshots/oxbaaz01.png
     :alt: Beispiel Lupen-Zoom
     :width: 650
     :class: with-shadow

     Abb.: Beispiel Lupen-Zoom

Sie können die gewünschte Art des Zooms global für Ihren eShop festlegen. Zusätzlich zu diesem Standard-Zoom können Sie die drei Zoom-Optionen auch für jedes Produkt individuell einstellen.

Zoom global festlegen
^^^^^^^^^^^^^^^^^^^^^

Wählen Sie die Art des Zooms global für Ihren eShop.

|procedure|

1. Wählen Sie unter :menuselection:`Erweiterungen --> Themes` das APEX-Theme.
#. Expandieren Sie auf der Registerkarte :guilabel:`Einstell.` den Bereich :guilabel:`Produktdetailseite`.
#. Wählen Sie unter :guilabel:`Zoom type for product detail page` die gewünschte Art des Zooms.
#. Speichern Sie Ihre Einstellungen.


Zoom für individuelle Produkte festlegen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Weisen Sie Sie bei Bedarf einzelnen Produkten eine individuelle Zoom-Option zu.

Zusätzlich zur Einstellung einer Standard-Bild-Zoom-Option in den Theme-Einstellungen können Sie damit die drei Zoom-Optionen individuell für jedes Produkt anwenden.

Damit haben Sie eine größere Flexibilität für verschiedene Produkte.

|procedure|

1. Wählen Sie unter :menuselection:`Artikel verwalten --> Artikel` das Produkt und wählen Sie die Registerkarte :guilabel:`Einstell.`.
#. Legen Sie den gewünschten Zoom fest, indem Sie im Eingabefeld :guilabel:`Alternatives Template` (:ref:`oxbaaz02`, Pos. 1) den Pfad des entsprechenden Templates eingeben.

   * Hover-Zoom: ``custom/hover_zoom.html.twig``
   * Modal-Zoom: ``custom/modal_zoom.html.twig``
   * Lupen-Zoom: ``custom/magnifier_lens.html.twig``

   .. _oxbaaz02:

   .. figure:: ../media/screenshots/oxbaaz02.png
      :alt: Alternatives Template für ein Produkt festlegen
      :width: 650
      :class: with-shadow

      Abb.: Alternatives Template für ein Produkt festlegen

#. Speichern Sie Ihre Einstellungen.
#. Optional: Um die Einheitlichkeit der Darstellung zu gewährleisten, wiederholen Sie die Schritte für alle Produkte einer Kategorie.

   Hintergrund: Es ist nicht möglich, die Zoom-Templates auf Kategorieebene anzuwenden.



.. Intern: oxbaaz, Status: