Staffelpreise definieren
========================

Gewähren Sie für ausgewählte Artikel einen Mengenrabatt durch Staffelpreise.

Ab bestimmten Mengen greifen automatisch niedrigere Preise.

Für jede Staffel legen Sie entweder einen festen Preis oder einen prozentualen Rabatt fest.

Mit mehreren Mengenstaffeln definieren Sie unterschiedliche Preisstufen für den Artikel.

Im OXID eShop werden die Staffelpreise auf der Artikeldetailseite angezeigt (:ref:`oxbafm01`, Pos. 2), sobald der Kunde die Schaltfläche :guilabel:`Mengenstaffelpreise` wählt (:ref:`oxbafm01`, Pos. 1).

Der im Warenkorb angezeigte Preis richtet sich nach der beim Kauf angegebenen Menge.

.. _oxbafm01:

.. figure:: ../../media/screenshots/oxbafm01.png
   :alt: Staffelpreise anzeigen
   :width: 650
   :class: with-shadow

   Abb.: Staffelpreise anzeigen

|procedure|

Legen Sie Staffelpreise in der Artikelverwaltung fest.

1. Wählen Sie :menuselection:`Artikel verwalten --> Artikel`.
#. Wählen Sie den gewünschten Artikel aus der Artikelliste.
#. Legen Sie auf der Registerkarte :guilabel:`Lager` unter :guilabel:`Staffelpreise` eine Mengenstaffel sowie den dazugehörigen Preis fest (:ref:`oxbafm02`, Pos. 1).

   Beispiel: Für Mengen zwischen 5 und 10 ist der Preis 33,99 € statt des regulären Preises von 35,99 €, den Sie unter :guilabel:`Stamm` festgelegt haben.

#. Speichern Sie Ihre Eingaben und fügen Sie weitere Mengenstaffeln nach demselben Muster hinzu.

   Beispiel: Für alle Bestellmengen über 10 ist der Preis 30 €.

   Stellen Sie sicher, dass bei der Staffel mit der höchsten Artikelanzahl im Feld :guilabel:`bis` ein ausreichend hoher Wert eingetragen ist, beispielsweise 999999.

   Andernfalls gilt bei Überschreitung der höchsten Staffelmenge der reguläre Artikelpreis.

.. _oxbafm02:

.. figure:: ../../media/screenshots/oxbafm02.png
   :alt: Staffelpreise festlegen
   :width: 650
   :class: with-shadow

   Abb.: Staffelpreise festlegen


.. seealso:: :doc:`Artikel - Registerkarte Lager <../artikel/registerkarte-lager>`

.. Intern: oxbafm, Status: