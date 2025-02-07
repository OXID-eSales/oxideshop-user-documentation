Rabatte anlegen, verwalten und plazieren
========================================

Rabatte gehören neben Gutscheinserien, Newslettern und Aktionen zu den zentralen Marketinginstrumenten in Ihrem OXID eShop

Ein Rabatt reduziert den Preis eines Artikels, sofern bestimmte Bedingungen erfüllt sind.

Günstigere Artikelpreise können Sie für bestimmte Artikel, Kategorien, Benutzer, Benutzergruppen, Einkaufswerte oder -mengen gewähren.

Durch Rabatte bieten Sie Ihren Kunden attraktive Einkaufsvorteile und stärken die Kundenbindung.

Arten von Rabatten
------------------

* Den Wert des Rabatts können Sie wie folgt festlegen:

  * prozentual zum Artikelpreis (:ref:`oxbahh01`, Pos. 2)
  * absolut
  * als Gratisartikel, der automatisch in den Warenkorb gelegt wird

* Schränken Sie die Gültigkeit ein

  * nach Kategorien oder Artikeln
  * nach Benutzern oder Benutzergruppen
  * für einen bestimmten Zeitraum
  * länderspezifisch

* Mengenrabatte oder Staffelrabatte können Sie mit Staffelpreisen direkt in den Artikeln umsetzen.

  Damit können Sie definieren, dass ein Artikel günstiger wird, sobald eine bestimmte Menge dieses Artikels gekauft wird.

  Weitere Informationen finden Sie unter :doc:`Artikel - Registerkarte Lager <../../einrichtung/artikel/registerkarte-lager>`.

.. _oxbahh01:

.. figure:: ../../media/screenshots/oxbahh01.png
   :alt: Beispiel: Zeitlich begrenzten Rabatt von 10% anlegen
   :width: 650
   :class: with-shadow

   Abb.: Beispiel: Zeitlich begrenzten Rabatt von 10% anlegen

Rabatte plazieren
-----------------

* Bestimmen Sie die Plazierung:

  * Zeigen Sie das Angebot direkt mit den ermäßigten Preisen an.
  * Weisen Sie den Rabatt erst im Warenkorb aus.

    Beispiel: Sie wollen, dass die Rabattart Zugabe im Warenkorb angezeigt wird und nicht in der Artikelübersicht oder auf der Detailseite (siehe :ref:`betrieb/rabatte/artikel-als-zugabe:Gratisartikel als Rabatt anlegen`).

  Weitere Informationen finden Sie im Schritt :ref:`Plazierung bestimmen <Rabatt-Plazierung-bestimmen>` (unter :ref:`betrieb/rabatte/rabatte:Rabatte anlegen und verwalten`).

* Aktivieren Sie in Ihrem OXID eShop bei Bedarf verschiedene Rabatte gleichzeitig, die bei entsprechenden Bedingungen im Warenkorb berücksichtigt werden.

  Dabei werden Rabatte, die für bestimmte Artikel gelten, im Warenkorb durch den jetzt gültigen rabattierten Preis und den durchgestrichenen, ursprünglichen Artikelpreis kenntlich gemacht (:ref:`oxbahh02`, Pos. 1).

  Rabatte, die für den gesamten Warenkatalog gelten, werden als jeweils eine Zeile bei der Auflistung des Gesamtbetrages für den Warenkorb angezeigt (:ref:`oxbahh02`, Pos. 2).

  .. _oxbahh02:

  .. figure:: ../../media/screenshots/oxbahh02.png
     :alt: Beispiel: Rabattierter Artikel im Warenkorb
     :width: 650
     :class: with-shadow

     Abb.: Beispiel: Rabattierter Artikel im Warenkorb

  Für Sie als Shopbetreiber wird der Rabatt in der Bestellverwaltung angezeigt (siehe :doc:`Bestellungen - Registerkarte Stamm <../bestellungen/registerkarte-stamm>`).

Rabatte anlegen und verwalten
-----------------------------

Erstellen und bearbeiten Sie Rabatte.

|procedure|

1. Wählen Sie :menuselection:`Shopeinstellungen --> Rabatte`.

#. Wenn Sie die Oxid eShop Enterprise Edition haben: Pflegen Sie Rabatte zentral und vererben Sie sie alle oder einzeln an Subshops.

   Weitere Informationen finden Sie unter :doc:`Registerkarte Mall: Rabatte an Subshops vererben <registerkarte-mall>`.

#. Legen Sie den Rabatt an.

   Sie haben folgende Möglichkeiten:

   * Optional: Begrenzen Sie Rabatte zeitlich.

     Weitere Informationenfinden Sie unter :doc:`Rabatte zeitlich begrenzen <zeitlich-begrenzte-rabatte>`.
   * Optional: Legen Sie statt eines absoluten oder relativen Preisnachlasses einen Gratisartikel als Rabatt an.

     Weitere Informationenfinden Sie unter :doc:`Gratisartikel als Rabatt anlegen <artikel-als-zugabe>`.
   * Bestimmen Sie die Plazierung.

     .. _Rabatt-Plazierung-bestimmen:

     Legen Sie im Eingabefeld :guilabel:`Einkaufswert` oder :guilabel:`Einkaufsmenge` fest, wann der Rabatt vom Preis abgezogen werden soll:

     * Um den Artikel bereits im Online-Shop mit dem rabattierten Preis anzuzeigen, geben Sie den Wert im Feld :guilabel:`Von` mit ``0`` an (:ref:`oxbahh03`, Pos. 1).

       Der Wert im Feld :guilabel:`Bis` kann ebenfalls ``0`` sein.

       .. _oxbahh03:

       .. figure:: ../../media/screenshots/oxbahh03.png
          :alt: Anzeigen des rabattierten Preises im Online-Shop
          :width: 650
          :class: with-shadow

          Abb.: Anzeigen des rabattierten Preises im Online-Shop

       In unserem Beispiel wird statt des Listenpreises von 120.000 € der um 10% rabattierte Preis von 108.000 € angezeigt (:ref:`oxbahh03`, Pos. 2).

     * Um den Rabatt erst im :emphasis:`Warenkorb` auszuweisen (:ref:`oxbahh04`, Pos. 4, 5), geben Sie den Wert im Feld :guilabel:`Von` mit ``1`` an (:ref:`oxbahh04`, Pos. 1).

       .. attention::

          Der Wert im Feld :guilabel:`Bis` darf in diesem Fall nicht ``0`` sein. (:ref:`oxbahh04`, Pos. 2).

       .. _oxbahh04:

       .. figure:: ../../media/screenshots/oxbahh04.png
          :alt: Anzeigen des rabattierten Preises im Warenkorb
          :width: 650
          :class: with-shadow

          Abb.: Anzeigen des rabattierten Preises im Warenkorb


#. Ordnen Sie die betreffenden Kategorien oder Artikel zu.

   Weitere Informationen finden Sie unter :doc:`Registerkarte Artikel: Kategorie oder Artikel zuordnen <registerkarte-artikel>`.
#. Optional: Schränken Sie den Rabatt auf bestimmte Benutzergruppen ein.

   Weitere Informationenfinden Sie unter :doc:`Registerkarte Benutzer: Rabatte auf Benutzer oder Gruppen einschränken <registerkarte-benutzer>`.


|result|

In der Liste der Rabatte symbolisiert ein kleiner grüner Kreis mit Häkchen am Anfang der Zeile einen immer aktiven Rabatt.

 .. note::

    :emphasis:`Zeitgesteuerte` Rabatte sind in der Liste :emphasis:`nicht` gesondert markiert.

    .. todo: #SB: Wird evtl. feature request: https://oxid-esales.atlassian.net/browse/OXDEV-8435?focusedCommentId=168679

Rabatte deaktivieren
--------------------

Um einen Rabatt zu deaktivieren, tun Sie Folgendes:

* Entfernen Sie die MArkierung bei :guilabel:`Immer aktiv`.
* Stellen Sie sicher, dass kein Zeitraum eingetragen ist. Ein Eintrag würde den Rabatt ansonsten für den angegebenen Zeitraum aktivieren.


.. Intern: oxbahh, Status: