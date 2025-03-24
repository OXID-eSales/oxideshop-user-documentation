Preis pro Mengeneinheit (Grundpreis) angeben
============================================

Für Artikel, die nach Gewicht, Volumen, Länge oder Fläche angeboten werden, müssen Sie den Grundpreis angeben.

Dies ist in § 2 der `Preisangabeverordnung <http://www.gesetze-im-internet.de/pangv/>`_ geregelt.

Für den Artikel ist daher nicht nur der Endpreis, sondern auch der Preis je Mengeneinheit auszuweisen.

Der Grundpreis wird automatisch berechnet und auf der Detailseite des Artikels zusammen mit dem Endpreis angezeigt (:ref:`oxbafl01`, Pos. 1).

.. _oxbafl01:

.. figure:: ../../media/screenshots/oxbafl01.png
   :alt: Grundpreis auf der Detailseite des Artikels anzeigen
   :width: 650
   :class: with-shadow

   Abb.: Grundpreis auf der Detailseite des Artikels anzeigen

Vorgehen
--------

Um den Grundpreis eines Artikels zu berechnen und anzuzeigen, tun Sie Folgendes:

1. Gehen Sie zu :menuselection:`Artikel verwalten --> Artikel`.
#. Wählen Sie den gewünschten Artikel aus der Artikelliste.
#. Wählen Sie die Registerkarte :guilabel:`Erweitert`.
#. Tragen Sie im Eingabefeld :guilabel:`Menge` den Wert ein, und wählen Sie im Feld :guilabel:`Mengeneinheit` die Einheit fest (:ref:`oxbafl02`, Pos. 1).
   |br|
   Wählen Sie die Mengeneinheit aus der Dropdown-Liste oder tragen Sie sie ein, ohne eine Mengeneinheit auszuwählen (\"-\").

   .. _oxbafl02:

   .. figure:: ../../media/screenshots/oxbafl02.png
      :alt: Grundpreis automatisch berechnen
      :width: 650
      :class: with-shadow

      Abb.: Grundpreis automatisch berechnen

#. Speichern Sie die Änderungen.

|result|

Der Grundpreis wird automatisch berechnet und auf der Detailseite des Artikels zusammen mit dem Endpreis angezeigt (:ref:`oxbafl01`, Pos. 1).

Beispiele
---------

Bei einem Artikel, der in einer 500 g-Packung angeboten wird, tragen Sie im Feld :guilabel:`Menge` den Wert 0,5 ein und wählen kg als Mengeneinheit.`

Angenommen, der Artikel hat einen Preis von 6,99 €, wäre der Grundpreis 13,98 €/kg.

Ein Artikel von 2 m² Größe kostet 39,90 €. Der Grundpreis pro m² beträgt 19,95 €.

.. todo: #SB: für welchen Anwendungsfall brauche ich die folgende Info?

Die Mengeneinheiten kg, g, l, ml, cm, mm, m, m², m³, Stück und Teil sind in der Sprachdatei :file:`lang.php` im Verzeichnis :file:`/application/translations/de` hinterlegt.

.. seealso:: :doc:`Artikel - Registerkarte Erweitert <../artikel/registerkarte-erweitert>` | `Hinweisblatt zur Angabe von Grundpreisen im Online-Shop <http://www.haendlerbund.de/hinweisblaetter/finish/1-hinweisblaetter/114-grundpreisangabe-im-online-handel>`_ (Händlerbund)

.. Intern: oxbafl, Status: