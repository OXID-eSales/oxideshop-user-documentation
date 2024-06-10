Versandkosten nach Lieferland differenzieren
============================================

Für den Versand von Waren in das Ausland fallen höhere Versandkosten als für den Versand im Inland an.

Bilden Sie das durch Versandkostenregeln ab, die nur für bestimmte Länder gelten.

Der Kunde entscheidet sich beim Kauf im Online-Shop für eine Versandart. Alle Versandkostenregeln, die zu dieser Versandart gehören, werden abgearbeitet. Es wird geprüft, ob die festgelegte Bedingung (Land, in das versendet werden soll) erfüllt ist. Nur wenn die Bedingung zutrifft, wird die Versandkostenregel bei der Berechnung der Versandkosten angewandt.

Vorgehen
--------

1. Ordnen Sie in den Versandkostenregeln die gültigen Länder zu.

   .. hint:: Damit die Definition von Versand und Zahlung stringent ist, sollte die Länderzuordnung mit der in der zugehörigen Zahlungsart und der Versandart übereinstimmen.

      Ist kein Land zugewiesen, gilt die Versandkostenregel immer für alle Länder.

   a. Gehen Sie zu :menuselection:`Shopeinstellungen --> Versandkostenregeln`.
   #. Wählen Sie die Versandkostenregel aus der Liste der Versandkostenregeln.
   #. Betätigen Sie die Schaltfläche :guilabel:`Länder zuordnen` auf der Registerkarte :guilabel:`Stamm`.
   #. Verschieben Sie die Länder per Drag \& Drop in die rechte Liste des Zuordnungsfensters.
   #. Schließen Sie das Zuordnungsfenster.

2. Ordnen Sie die Versandkostenregel einer Versandart zu.

   .. hint::
      Der Versandart müssen mindestens eine Versandkostenregel und eine Zahlungsart zugeordnet worden sein.

      Länder sollten zugewiesen sein, damit die Definition von Versand und Zahlung stringent ist. Ohne Länderzuordnung gilt die Versandart für alle Länder.

   a. Gehen Sie zu :menuselection:`Shopeinstellungen --> Versandarten`.
   #. Wählen Sie die Versandart aus der Liste der Versandarten.
   #. Betätigen Sie die Schaltfläche :guilabel:`Versandkostenregeln zuordnen` auf der Registerkarte :guilabel:`Stamm`.
   #. Verschieben Sie die Versandkostenregel per Drag \& Drop in die rechte Liste des Zuordnungsfensters.
   #. Schließen Sie das Zuordnungsfenster.

Beispiel
--------
Zwei Versandkostenregeln dienen als Beispiel für eine Lieferung mit höheren Versandkosten, wenn Artikel ins Ausland geliefert werden.

Dafür erstellen Sie zwei Versandkostenregeln, denen Sie unterschiedliche Länder zugeordnen. Die eine ist für den Versand von Artikeln innerhalb von Deutschlands zum Preis von 3,90 € (:ref:`oxbafx01`), die andere für die Lieferung nach Österreich und in die Schweiz für 6,90 €.

Sie definieren die Versandkostenregeln so, dass die Berechnung nur einmal pro Warenkorb erfolgt. Länder müssen zugewiesen sein. Für die eine Versandkostenregel ist das Deutschland, für die andere sind das Österreich und die Schweiz.

.. _oxbafx01:

.. figure:: ../../media/screenshots/oxbafx01.png
   :alt: Beispiel: Versandkostenregel für Deutschland
   :width: 650
   :class: with-shadow

   Abb.: Beispiel: Versandkostenregel für Deutschland

Die Versandkostenregeln müssen einer Versandart zugeordnet sein. Wird diese Versandart beim Kauf eines Artikels ausgewählt, werden alle zugehörigen Versandkostenregeln geprüft. Sollen die Artikel nach Deutschland geliefert werden, greift die erste Versandkostenregel.

Wurden Artikel eingekauft, die nach Österreich geliefert werden, gilt die zweite Versandkostenregel.

.. seealso:: :doc:`Versandkostenregeln - Registerkarte Stamm <../versandkostenregeln/registerkarte-stamm>` | :doc:`Versandarten - Registerkarte Stamm <../versandarten/registerkarte-stamm>`

.. Intern: oxbafx, Status: