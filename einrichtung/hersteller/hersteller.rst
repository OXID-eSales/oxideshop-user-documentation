Produkte nach Marken präsentieren
=================================

Präsentieren Sie die Marken (Hersteller) Ihres OXID eShops im Frontend.

So können Sie Artikel unabhängig von den Kategorien im Shop nach Marken präsentieren.

Wie sieht das aus?

Im Frontend erscheinen die Marken Ihres OXID eShops in einem Slider (:ref:`oxbagb01`, Pos. 1).

.. _oxbagb01:

.. figure:: ../../media/screenshots/oxbagb01.png
   :alt: Marken-Slider
   :width: 650
   :class: with-shadow

   Abb.: Marken-Slider

Über den Slider (:ref:`oxbagb01`, Pos. 2) gelangen Ihre Kunden zu einer Übersicht aller Artikel einer Marke (:ref:`oxbagb02`, Pos. 1).

.. _oxbagb02:

.. figure:: ../../media/screenshots/oxbagb02.png
   :alt: Artikelübersicht nach Marken
   :width: 650
   :class: with-shadow

   Abb.: Artikelübersicht nach Marken

Über die Übersicht aller Artikel einer Marke (:ref:`oxbagb02`, Pos. 4) gelangen Ihre Kunden zu einer Marken-Übersicht (:ref:`oxbagb03`, Pos. 1).

.. _oxbagb03:

.. figure:: ../../media/screenshots/oxbagb03.png
   :alt: Marken-Übersicht
   :width: 650
   :class: with-shadow

   Abb.: Marken-Übersicht


|procedure|

Um die Hersteller als Marken im Frontend anzuzeigen, tun Sie Folgendes:

1. Wählen Sie :menuselection:`Stammdaten --> Hersteller`.
#. Wählen Sie :guilabel:`Neuen Hersteller anlegen`.
#. Tun Sie auf der Registerkarte :guilabel:`Stamm`  (:ref:`oxbagb04`) Folgendes:

   a. Geben Sie im Feld :guilabel:`Titel` den Namen der Marke ein.
   #. Geben Sie im Feld :guilabel:`Kurzbeschreibung` den Slogan (Tagline/Claim) ein, der in der Artikelübersicht nach Marke angezeigt werden soll (:ref:`oxbagb02`, Pos. 3).
   #. Ordnen Sie die Produkte des betreffenden Herstellers zu.
   #. Stellen Sie sicher, dass die Marke aktiv ist und speichern Sie Ihre Eingaben.

   .. note::

      Die Hersteller sind standardmäßig alphabetisch nach Titel sortiert.

      Werte im Feld :guilabel:`Sortierung` wirken sich also standardmäßig nicht aus.

      Um die Hersteller bei Bedarf anders zu sortieren, implementieren Sie eine Lösung, welche die ``oxManufacturerList`` nach ``oxsort`` sortiert statt standardmäßig nach ``oxtitle``.

      .. todo: #SB/#HR: Funktion in Klärung: OXDEV-9113

   .. _oxbagb04:

   .. figure:: ../../media/screenshots/oxbagb04.png
      :alt: Hersteller (Marke) anlegen
      :width: 650
      :class: with-shadow

      Abb.: Hersteller (Marke) anlegen

#. Wenn Sie die OXID eShop Enterprise Edition haben, verwalten Sie auf der Registerkarte :guilabel:`Mall` die Verknüpfungen eines Herstellers zu Subshops und Supershops.

   Weitere Informationen finden Sie unter :doc:`Registerkarte Mall <registerkarte-mall>`.

#. Optimieren Sie auf der Registerkarte :guilabel:`SEO` die Auffindbarkeit Ihrer Marken, indem Sie passende Keywords, Meta-Beschreibungen und URLs hinterlegen.

   Weitere Informationen finden Sie unter :doc:`Registerkarte SEO <registerkarte-seo>`.

#. Tun Sie auf der Registerkarte :guilabel:`Bilder` Folgendes:

   a. Ordnen Sie der Marke ein Icon zu, das im Slider (:ref:`oxbagb01`, Pos. 1), in der Markenübersicht (:ref:`oxbagb02`, Pos. 2) und in der Artikelübersicht (:ref:`oxbagb03`, Pos. 2) angezeigt wird.

      Legen Sie die Größe des Hersteller-/Markenlogos in Pixeln (Breite*Höhe) in den Einstellungen des Themes fest.

   #. Laden Sie bei Bedarf weitere Bilder hoch.

      * Alternatives Icon: Nutzen Sie bei Bedarf ein invertiertes Logo, wenn Sie einen Marken-Slider mit invertierten Farben implementieren.

      Die folgenden Bild-Typen sind nicht standardmäßig im APEX-Theme implementiert. Sie können sie aber einsetzen, indem Sie das APEX-Theme anpassen:

      * Bild: Ergänzen Sie eine Abbildung auf der Produktdetailseite
      * Thumbnail
      * Icon für Werbeaktionen

#. Aktivieren Sie die Funktion.

   a. Wählen Sie :menuselection:`Stammdaten --> Grundeinstellungen`.
   #. Wählen Sie die Registerkarte :guilabel:`Perform.`.
   #. Aktivieren Sie das Kontrollkästchen :guilabel:`Herstellerliste laden und anzeigen`.

.. todo: #SB: Wozu dient unter Stammdaten-> Hersteller  der Link "Artikelanzahl in den Herstellern zurücksetzen"?
    "Wird ein Hersteller aus der Liste gewählt, werden dessen Informationen in den Eingabebereich geladen. In der Fußzeile finden Sie die Funktionen: :guilabel:`Neuen Hersteller anlegen`, :guilabel:`Artikelanzahl in den Herstellern zurücksetzen` und :guilabel:`Hilfe starten`.
   SB: Keine Idee, was es soll: solange Ignorieren: SB meldet sich

.. Intern: oxbagb, Status: