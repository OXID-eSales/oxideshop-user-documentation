Bilder
======

Jeder Artikel kann bis zu zwölf Artikelbilder haben, die in der Detailansicht des Artikels angezeigt werden. Artikel verfügen über Zoombilder, die ebenfalls auf der Detailseite aufrufbar sind. Kleinere Artikelbilder zeigen den Artikel in den Artikellisten, in Produktboxen und im Warenkorb. Alle benötigten Bildarten werden automatisch generiert.

Informationen zur Generierung der Bilder und zur Verzeichnisstruktur der Artikelbilder ab OXID eShop 4.5.1 finden Sie im englischsprachigen Tutorial `Image handling changes <https://oxidforge.org/en/image-handling-changes-since-version-4-5-1.html>`_ auf der OXIDforge.

Bildgenerierung und -qualität
-----------------------------
Die erforderlichen Einstellungen für die Bildgenerierung und für die Bildgrößen werden für alle Artikel im Administrationsbereich vorgenommen. Gehen Sie zu :menuselection:`Stammdaten --> Grundeinstellungen`, Registerkarte :guilabel:`Einstell.` Klicken Sie auf :guilabel:`Bilder`, um die Einstellungen anzuzeigen. Das ist zum einen die installierte Version der GDLib, einer Software auf dem Server, die für die dynamische Erzeugung von Grafiken zuständig ist. Deren aktuelle Version ist die Version 2. Zum anderen ist das automatische Generieren von Icons aktiviert. Lassen Sie beide Einstellungen unverändert.

In der Registerkarte :guilabel:`System` gibt es ebenfalls einen kleinen Abschnitt :guilabel:`Bilder`. Wichtig für die Bildgenerierung ist die Vorgabe für die Bildqualität. Die Standardeinstellung ist 75 und stellt einen guten Kompromiss zwischen Bildqualität und Dateigröße dar. Bei einem deutlich kleineren Wert sind die Artikelbilder stark komprimiert, haben daher eine kleine Dateigröße, aber eine schlechte Bildqualität (Unschärfen und Kompressionsartefakte). Ist der Wert größer als 75, steigt die Bildqualität, aber auch die Größe der Datei (längere Ladezeiten).

Die Option :guilabel:`E-Mails mitsamt Bildern versenden`, hat nichts mit der Bildgenerierung zu tun. Ist diese Einstellung aktiv, werden Artikelbilder in E-Mails mitgesendet. Die E-Mail, die als Bestellbestätigung verschickt wird, enthält dann Artikelbilder. E-Mails können so schnell groß werden, was zu Problemen beim Versand und beim Empfang der Mail führen kann. Standardmäßig werden E-Mails ohne Artikelbilder versendet. Die Artikelbilder werden beim Lesen der E-Mail durch das Mail-Programm des Kunden nachgeladen.

Bildgrößen
----------
Die Größe der Bilder für Artikel, Kategorien und für Hersteller- und Markenlogos ist abhängig vom Design des Shops. Die Einstellungen sind daher beim aktiven Theme unter :menuselection:`Erweiterungen --> Themes` hinterlegt. Rufen Sie die Registerkarte :guilabel:`Einstell.` des Themes \"Azure\" auf und klicken Sie auf :guilabel:`Bilder`.

:guilabel:`Größe des Icons in Pixeln (Breite*Höhe)`
   Icons sind die kleinsten Artikelbilder und werden im Warenkorb und in Produktboxen (Beispiel: Top of the Shop) verwendet. Standardgröße: 87 Pixel breit und 87 Pixel hoch.

:guilabel:`Größe des Thumbnails in Pixeln (Breite*Höhe)`
   Thumbnails sind Vorschaubilder und werden in Artikellisten, wie Kategorie-Übersichten und Suchergebnisse, und in Aktionen (Beispiel: Frisch eingetroffen!) angezeigt. Standardgröße: 185 Pixel breit und 150 Pixel hoch.

:guilabel:`Größe des Kategoriebildes in Pixeln (Breite*Höhe)`
   Bild für die Anzeige der Kategorie-Übersicht. Standardgröße: 784 Pixel breit und 150 Pixel hoch.

:guilabel:`Größe der Zoom-Bilder (Zoom 1-4) in Pixeln (Breite*Höhe)`
   Vergrößerte Anzeige eines Artikelbildes, die sich auf der Detailseite aufrufen lässt. Standardgröße: 665 Pixel breit und 665 Pixel hoch.

:guilabel:`Größe der Artikelbilder (Bild 1-12) in Pixeln (Breite*Höhe)`
   Artikelbild, welches auf der Detailseite angezeigt wird. Die Größe von bis zu 12 Artikelbilder kann definiert werden. Dadurch sind Artikelbilder mit unterschiedlichen Größen möglich. Für jedes Artikelbild gibt es eine Zeile, an derem Anfang oxpic und eine Zahl steht. oxpic1 steht für das erste Artikelbild, oxpic2 für das zweite Artikelbild usw. Standardgröße: 380 Pixel breit und 340 Pixel hoch.

.. hint::Die Möglichkeit unterschiedlicher Bildgrößen sollte nur mit Umsicht verwendet werden, denn verschieden große Artikelbilder könnten eventuell zu einer eher unprofessionellen Präsentation der Artikel beitragen.

:guilabel:`Größe des Hersteller-/Markenlogos in Pixeln (Breite*Höhe)`
   Logo, das in der Marken-Übersicht auf der Startseite angezeigt wird. Standardgröße: 100 Pixel breit und 100 Pixel hoch.

:guilabel:`Größe des Kategoriebildes einer Unterkategorie in Pixeln (Breite*Höhe)`
   Bild für die Anzeige von Unterkategorien in der Kategorie-Übersicht. Standardgröße: 168 Pixel breit und 100 Pixel hoch.

:guilabel:`Größe des Kategoriebildes für die Startseite in Pixeln (Breite*Höhe)`
   Bild der Kategorie, die auf der Startseite beworben wird. Standardgröße: 370 Pixel breit und 107 Pixel hoch.

.. Intern: oxbaaz, Status: