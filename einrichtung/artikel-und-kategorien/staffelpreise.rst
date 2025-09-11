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

.. important::

   Abb.: Staffelpreise festlegen

   Stellen Sie sicher, dass das Feld :guilabel:`bis` der höchsten Staffel eine ausreichend große Menge enthält (z. B. 999999).

   So verhindern Sie, dass bei Überschreitung der maximalen Staffelmenge der Originalpreis angewendet wird.

Staffelpreise in Kombination mit Rabatten verwenden
---------------------------------------------------

Staffelpreise ähneln Rabatten.

Die Kombination von Staffelpreisen mit Rabatten hängt von der Art des Rabatts ab. Produkt- und kategoriespezifische Rabatte prüfen den Mindestbestellwert, ab welchem ein Rabatt gilt, gegen den Originalpreis, während allgemeine Rabatte die staffelbereinigte Gesamtbestellsumme berücksichtigen. Die staffelbereinigte Summe bezeichnet die Gesamtbestellsumme nach Anwendung der Staffelpreise, aber vor Anwendung zusätzlicher Rabatte.

Produkt- und kategorie-spezifische Rabatte
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Wenn Sie Rabatte für Produkte mit Staffelpreisen konfigurieren, wird der im Feld :guilabel:`Einkaufswert` festgelegte Mindestbestellwert mit dem Originalpreis (dem ursprünglichen Preis des Produkts ohne Mengenrabatt) verglichen, nicht mit dem Staffelpreis.

|example|

* Sie haben ein Produkt mit einem Originalpreis von 10,00 EUR.
* Das Produkt hat einen Staffelpreis für Mengen von 10 bis 99 Stück in Höhe von 9,00 EUR.
* Sie fügen einen Rabatt von 50 % hinzu, der bei einer Preissumme von 100,00 EUR (dem im Feld :guilabel:`Einkaufswert` festgelegten Mindestbestellwert, ab welchem ein Rabatt gilt), ausgelöst wird.

Wenn Sie zehn Artikel in den Warenkorb legen, beträgt die ursprüngliche Preissumme 100,00 EUR, wodurch der 50 %-Rabatt ausgelöst wird. Da die Menge von zehn Artikeln den Staffelpreis von 9,00 EUR aktiviert, ergibt sich eine Gesamtbestellsumme von 45,00 EUR (nach Anwendung des Rabatts auf die staffelbereinigte Summe).

Sie können auch ein weiteres Produkt in Ihren Warenkorb legen, was zu elf Mal demselben Produkt führt. Mit dem Mengenrabatt erreichen Sie EUR 99,00. Allerdings beträgt die ursprüngliche Preissumme – nicht der Staffelpreis – EUR 110,00, weshalb der 50%-Rabatt angewendet wird. Sie zahlen EUR 49,50.

Dieses Verhalten gilt für produktspezifische und kategoriespezifische Rabatte. Allgemeine Rabatte vergleichen den im Feld :guilabel:`Einkaufswert` festgelegten Mindestbestellwert mit der Gesamtsumme der Bestellung, die unter Einbeziehung der Mengenrabatte berechnet wird.

**Erläuterung des Rechenwegs (produkt- oder kategoriespezifischer Rabatt mit 10 Artikeln):**

Das System priorisiert die Prüfung des im Feld :guilabel:`Einkaufswert` festgelegten Mindestbestellwerts, ab welchem ein Rabatt gilt, auf Basis der ursprünglichen Preissumme, um die Rabattbedingung auszulösen. Anschließend wird der Staffelpreis auf die Menge angewendet, und der Rabatt wirkt sich auf die staffelbereinigte Summe aus. Der detaillierte Ablauf ist wie folgt:

.. list-table::
   :header-rows: 1
   :widths: 10 50 25 15

   * - Schritt
     - Beschreibung
     - Berechnung
     - Ergebnis
   * - 1
     - Ursprüngliche Preissumme ermitteln (für Rabattbedingung)
     - 10 × 10,00 EUR
     - 100,00 EUR
   * - 2
     - Rabattbedingung prüfen und Rabattfaktor anwenden (da Summe ≥ 100,00 EUR)
     - Rabatt triggern: 50 % (Faktor 0,5)
     - Rabatt aktiviert
   * - 3
     - Staffelpreis anwenden (Menge 10 passt zu 10–99)
     - 10 × 9,00 EUR
     - 90,00 EUR (staffelbereinigte Summe)
   * - 4
     - Rabatt auf staffelbereinigte Summe anwenden
     - 90,00 EUR × 0,5
     - 45,00 EUR (Gesamtsumme)

Fügen Sie einen weiteren Artikel hinzu, so dass insgesamt elf gleiche Produkte im Warenkorb sind. Mit dem Staffelpreis erreichen Sie eine Zwischensumme von 99,00 EUR. Die ursprüngliche Preissumme (ohne Staffelpreis) beträgt jedoch 110,00 EUR, weshalb der 50 %-Rabatt angewendet wird. Sie zahlen 49,50 EUR.

**Erläuterung des Rechenwegs (produkt- oder kategoriespezifischer Rabatt mit 11 Artikeln):**

Ähnlich wie oben wird die Rabattbedingung auf der ursprünglichen Preissumme geprüft, der Staffelpreis separat angewendet und der Rabatt dann auf die staffelbereinigte Summe angewendet:

.. list-table::
   :header-rows: 1
   :widths: 10 50 25 15

   * - Schritt
     - Beschreibung
     - Berechnung
     - Ergebnis
   * - 1
     - Ursprüngliche Preissumme ermitteln (für Rabattbedingung)
     - 11 × 10,00 EUR
     - 110,00 EUR
   * - 2
     - Rabattbedingung prüfen und Rabattfaktor anwenden (da Summe ≥ 100,00 EUR)
     - Rabatt auslösen: 50 % (Faktor 0,5)
     - Rabatt aktiviert
   * - 3
     - Staffelpreis anwenden (Menge 11 passt zu 10–99)
     - 11 × 9,00 EUR
     - 99,00 EUR (staffelbereinigte Summe)
   * - 4
     - Rabatt auf staffelbereinigte Summe anwenden
     - 99,00 EUR × 0,5
     - 49,50 EUR (Gesamtsumme)


Allgemeine Rabatte
^^^^^^^^^^^^^^^^^^

Allgemeine Rabatte vergleichen den im Feld :guilabel:`Einkaufswert` festgelegten Mindestbestellwert, ab welchem ein Rabatt gilt, mit der Gesamtbestellsumme, die unter Berücksichtigung der Staffelpreise berechnet wird.

|example|

Dasselbe Szenario wie zuvor, aber diesmal mit einem allgemeinen Rabatt. Wenn Sie zehn Artikel in den Warenkorb legen, beträgt die Gesamtbestellsumme aufgrund des Staffelpreises (ab einer Menge von zehn) 90,00 EUR. Der 50 %-Rabatt wird nicht angewendet, da die Gesamtbestellsumme unter 100,00 EUR liegt.

**Erläuterung des Rechenwegs (allgemeiner Rabatt mit 10 Artikeln):**

Bei allgemeinen Rabatten erfolgt die Prüfung der Bedingung nach Anwendung der Staffelpreise, was zu einer anderen Logik führt:

.. list-table::
   :header-rows: 1
   :widths: 10 50 25 15

   * - Schritt
     - Beschreibung
     - Berechnung
     - Ergebnis
   * - 1
     - Staffelpreis anwenden (Menge 10 passt zu 10–99)
     - 10 × 9,00 EUR
     - 90,00 EUR (Gesamtsumme)
   * - 2
     - Rabattbedingung prüfen (auf staffelbereinigter Summe)
     - 90,00 EUR < 100,00 EUR
     - Kein Rabatt
   * - 3
     - Finale Summe
     - Keine weitere Anpassung
     - 90,00 EUR (Gesamtsumme)

Fügen Sie nun ein weiteres Produkt in den Warenkorb hinzu, z. B. ein Produkt mit einem Preis von 15,00 EUR. Die Gesamtbestellsumme beträgt nun 105,00 EUR. Der im Feld :guilabel:`Einkaufswert` festgelegte Mindestbestellwert wird erreicht, und der 50 %-Rabatt wird angewendet.

**Erläuterung des Rechenwegs (allgemeiner Rabatt mit 10 Artikeln + Zusatzprodukt):**

Die Staffelpreise werden zuerst auf die relevanten Produkte angewendet, dann die Gesamtsumme geprüft und der Rabatt auf die gesamte Summe appliziert:

.. list-table::
   :header-rows: 1
   :widths: 10 50 25 15

   * - Schritt
     - Beschreibung
     - Berechnung
     - Ergebnis
   * - 1
     - Staffelpreis für Hauptprodukt anwenden
     - 10 × 9,00 EUR
     - 90,00 EUR
   * - 2
     - Zusatzprodukt addieren
     - 90,00 EUR + 15,00 EUR
     - 105,00 EUR (Gesamtsumme)
   * - 3
     - Rabattbedingung prüfen und anwenden (da Summe ≥ 100,00 EUR)
     - 105,00 EUR × 0,5
     - 52,50 EUR (Gesamtsumme)


.. hint:: Rabatte aus Gutscheinserien werden stets auf Basis der Gesamtbestellsumme berechnet, da sie nur die Option :guilabel:`Min. Bestellsumme` verwenden und keinen Mindestbestellwert (Feld :guilabel:`Einkaufswert`), der mit Staffelpreisen in Konflikt geraten könnte.

  Weitere Informationen finden Sie unter :doc:`Gutscheinserien <../../betrieb/gutscheinserien/gutscheinserien>`.

.. seealso:: :doc:`Artikel - Registerkarte Lager <../artikel/registerkarte-lager>`

.. Intern: oxbafm, Status: