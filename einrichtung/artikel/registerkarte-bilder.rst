Registerkarte Bilder
====================

Verwalten Sie Artikelbilder direkt über die Registerkarte :guilabel:`Bilder`.

Präsentieren Sie Ihre Produkte ansprechend, indem Sie bis zu zwölf Artikelbilder in verschiedenen Ansichten und Perspektiven bereitstellen. Die Bilder erscheinen in der Detailansicht des Artikels. Zusätzlich stehen Zoombilder zur Verfügung. Kleinere Bildversionen – Thumbnails und Icons – nutzt der Shop in Artikellisten, Produktboxen und im Warenkorb.

Definieren Sie die Standardgrößen der Bilder in den Theme-Einstellungen. Eine ausführliche Anleitung dazu finden Sie im Abschnitt „Konfiguration“ unter :doc:`Bilder <../../konfiguration/bilder>` .

.. figure:: ../../media/screenshots/oxbacp01.png
   :alt: Artikel – Registerkarte Bilder
   :width: 650
   :class: with-shadow

   Abb.: Artikel – Registerkarte Bilder

|procedure|

1. Öffnen Sie im Adminbereich die gewünschte Produktdetailseite.
#. Wechseln Sie zur Registerkarte :guilabel:`Bilder`.
#. Laden Sie bis zu sieben Bilder direkt über das Interface hoch. Wenn Sie mehr als sieben Bilder verwenden möchten, laden Sie diese per FTP hoch oder erweitern Sie das Template des Administrationsbereichs.

   :guilabel:`Artikelbilder (max. 2 MB, max. 1500 x 1500 px)`
      Halten Sie sich beim Hochladen an die Standardgrenzen: maximal 2 MB pro Datei und maximal 1500 × 1500 Pixel. Höhere Werte können beim Generieren von Thumbnails oder Icons zu Speicherproblemen führen. Passen Sie gegebenenfalls die Werte ``upload_max_filesize`` und ``memory_limit`` in der :file:`php.ini` an.

   :guilabel:`#1` – :guilabel:`#7`
      Nutzen Sie die Felder :guilabel:`#1` bis :guilabel:`#7`, um Bilder vom lokalen System auszuwählen. Klicken Sie auf :guilabel:`Durchsuchen...`, wählen Sie ein Bild, und bestätigen Sie mit :guilabel:`Öffnen`. Speichern Sie anschließend, um den Upload durchzuführen. Das System erzeugt automatisch ein Thumbnail und ein Icon.

   :guilabel:`Thumbnail/Icon manuell hochladen`
      Überschreiben Sie das automatisch erzeugte Thumbnail oder Icon durch eigene Dateien. Diese erscheinen ebenfalls in der Vorschau auf der linken Seite.

   :guilabel:`Thumbnail (max. 2 MB, max. 1500*1500 px)`
      Laden Sie hier ein alternatives Thumbnail hoch, falls das automatisch generierte Bild nicht Ihren Anforderungen entspricht.

   :guilabel:`Icon (max. 2 MB, max. 1500*1500 px)`
      Verwenden Sie hier ein eigenes Iconbild, wenn Sie nicht das automatisch erzeugte Icon verwenden möchten.

#. Nutzen Sie die Vorschaufunktion, um die hochgeladenen Bilder zu überprüfen.
#. Entfernen Sie nicht mehr benötigte Bilder über das Papierkorb-Symbol. Das System löscht die Dateien sowohl aus dem Shop als auch vom Webserver.

|result|

Nach dem Speichern zeigt der Shop das neue Artikelbild in der Detailansicht, das zugehörige Thumbnail in der Artikelliste und das Icon im Warenkorb an.


.. seealso:: :doc:`Artikel – Registerkarte Erweitert <../artikel/registerkarte-erweitert>` | :doc:`Bilder <../../konfiguration/bilder>`

.. Intern: oxbacp, Status:, F1: article_pictures.html

