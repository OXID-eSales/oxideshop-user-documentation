Gewichtsabhängige Versandkosten festlegen
=========================================

Berücksichtigen Sie für die Berechnung der Versandkosten das Gewicht der Artikel.

Dafür erstellen Sie Versandkostenregeln, deren Bedingung das Gewicht von Artikeln ist.

Im Bestellprozess entscheidet sich der Kunde für eine Versandart. Alle Versandkostenregeln, die zu dieser Versandart gehören, werden abgearbeitet.

Es wird geprüft, ob die festgelegte Bedingung (Gewicht) hinsichtlich des Gesamtgewichts der Artikel im Warenkorb erfüllt ist. Nur wenn die Bedingung zutrifft, wird die Versandkostenregel bei der Berechnung der Versandkosten angewandt.

Vorgehen
--------

1. Legen Sie das Gewicht eines Artikels fest.

   a. Gehen Sie zu :menuselection:`Artikel verwalten --> Artikel`.
   #. Wählen Sie den gewünschten Artikel aus der Artikelliste.
   #. Geben Sie auf der Registerkarte :guilabel:`Erweitert` das Gewicht ein.

      Wenn Sie das Gewicht eines Artikels festlegen, wird das Gewicht auf der Detailseite des Artikels unterhalb des Artikelpreises ausgewiesen.

   #. Speichern Sie Ihre Einstellungen.

#. Legen Sie in den Versandkostenregeln das Gewicht als Bedingung fest.

   a. Gehen Sie zu :menuselection:`Shopeinstellungen --> Versandkostenregeln`.
   #. Wählen Sie die Versandkostenregel aus der Liste der Versandkostenregeln.

      Auf der Registerkarte :guilabel:`Stamm` finden Sie die Dropdown-Liste :guilabel:`Bedingung`.

   #. Wählen Sie die Bedingung Gewicht und tragen Sie Werte für :guilabel:`=\>` und :guilabel:`\<=` ein.
   #. Komplettieren Sie alle weiteren Einstellungen der Versandkostenregel.
   #. Speichern Sie Ihre Einstellungen.

3. Ordnen Sie die Versandkostenregel einer Versandart zu

   a. Gehen Sie zu :menuselection:`Shopeinstellungen --> Versandarten`.
   #. Wählen Sie die Versandart aus der Liste der Versandarten.
   #. Betätigen Sie die Schaltfläche :guilabel:`Versandkostenregeln zuordnen` auf der Registerkarte :guilabel:`Stamm`.
   #. Verschieben Sie die Versandkostenregel per Drag \& Drop in die rechte Liste des Zuordnungsfensters.
   #. Schließen Sie das Zuordnungsfenster.

Beispiel
--------

In unserem Beispiel nehmen wir einen Artikel mit einem Gewicht von 2 kg an.

|procedure|

1. Tragen Sie in der Artikelverwaltung beim Artikel auf der Registerkarte :guilabel:`Erweitert` ein Gewicht von 2 Kilogramm ein (:ref:`oxbafv01`).

   .. _oxbafv01:

   .. figure:: ../../media/screenshots/oxbafv01.png
      :alt: Beispiel: Artikel mit 2 kg Gewicht
      :width: 650
      :class: with-shadow

      Abb.: Beispiel: Artikel mit 2 kg Gewicht

#. Erstellen Sie zwei Versandkostenregeln, deren Bedingung das Gewicht ist:

   * Die erste ist für Artikel im Warenkorb unter 3 Kilogramm Gesamtgewicht, die für 3,90 € verschickt werden.
   * Die zweite ist für Artikel mit mehr Gewicht und Versandkosten in Höhe von 5,50 € (:ref:`oxbafv02`).

   Die Versandkostenregeln definieren Sie so, dass die Berechnung nur einmal pro Warenkorb erfolgt.

   Länder können, aber müssen nicht zugewiesen sein.

   .. _oxbafv02:

   .. figure:: ../../media/screenshots/oxbafv02.png
      :alt: Beispiel: Versandkostenregel für Gesamtgewicht ab 3 kg
      :width: 650
      :class: with-shadow

      Abb.: Beispiel: Versandkostenregel für Gesamtgewicht ab 3 kg

#. Ordnen Sie die Versandkostenregeln einer Versandart zu.

|result|

Wird diese Versandart beim Kauf eines Artikels ausgewählt, werden alle zugehörigen Versandkostenregeln geprüft.

* Liegt der Artikel mit dem Gewicht von 2 Kilogramm einmal im Warenkorb, greift die erste Versandkostenregel.
* Sind zwei oder mehrere Artikel mit einem Gewicht von jeweils 2 Kilogramm im Warenkorb, greift die zweite Versandkostenregel.

.. seealso:: :doc:`Artikel - Registerkarte Erweitert <../artikel/registerkarte-erweitert>` | :doc:`Versandkostenregeln - Registerkarte Stamm <../versandkostenregeln/registerkarte-stamm>` | :doc:`Versandarten - Registerkarte Stamm <../versandarten/registerkarte-stamm>`


.. Intern: oxbafv, Status: