Preis pro Mengeneinheit (Grundpreis) angeben
============================================

Für Artikel, die nach Gewicht, Volumen, Länge oder Fläche angeboten werden, müssen Sie den Grundpreis angeben.

Dies ist im Paragraph 2 der `Preisangabeverordnung <http://www.gesetze-im-internet.de/pangv/>`_ geregelt.

Beim Artikel ist daher nicht nur der Endpreis, sondern auch der Preis je Mengeneinheit auszuweisen.

Der Grundpreis wird berechnet und auf der Detailseite des Artikels zusamen mit dem Endpreis angezeigt (:ref:`oxbafl01`).

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
#. Geben Sie in die finden Sie die Eingabefelder :guilabel:`Menge` und :guilabel:`Mengeneinheit` die Menge des Artikels ein und legen Sie die Mengeneinheit fest.
   |br|
   Wählen Sie die Mengeneinheit aus der Dropdown-Liste oder tragen Sie diese ein, ohne eine Mengeneinheit auszuwählen (\"-\").
#. Speichern Sie die Änderungen.

Beispiel
--------

Bei einem Artikel, der in einer 500 g-Packung angeboten wird, tragen Sie 0,5 bei Menge ein und wählen kg als Mengeneinheit.

Angenommen, der Artikel hat einen Preis von 6,99 €, wäre der Grundpreis 13,98 €/kg.

.. todo: #SB: für welchen Anwendungsfall brauche ich die folgende Info?

Die Mengeneinheiten kg, g, l, ml, cm, mm, m, m², m³, Stück und Teil sind in der Sprachdatei :file:`lang.php` im Verzeichnis :file:`/application/translations/de` hinterlegt.

.. seealso:: :doc:`Artikel - Registerkarte Erweitert <../artikel/registerkarte-erweitert>` | `Hinweisblatt zur Angabe von Grundpreisen im Online-Shop <http://www.haendlerbund.de/hinweisblaetter/finish/1-hinweisblaetter/114-grundpreisangabe-im-online-handel>`_ (Händlerbund)

.. Intern: oxbafl, Status: