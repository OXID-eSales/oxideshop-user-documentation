Gratisartikel als Rabatt anlegen
================================

Neben dem absoluten und relativen Preisnachlass bietet der OXID eShop noch eine dritte Rabattmöglichkeit: den Gratisartikel.

Bei jedem Kauf, der die Bedingungen des Rabattes erfüllt, wird ein dafür vorgesehener Artikel als kostenlose Zugabe in den Warenkorb gelegt.

Damit lassen sich beispielsweise Rabattaktionen für bestimmte Einkaufswerte oder -mengen umsetzen.

Der Preis des Artikels, der als Zugabe in den Warenkorb gelegt wird, wird automatisch auf Null gesetzt. Es ist nicht notwendig, dafür den bisherigen Preis in der Artikelverwaltung zu ändern.

|procedure|

1. Wählen Sie :menuselection:`Shopeinstellungen --> Rabatte`.
#. Legen Sie einen neuen Rabatt an, vergeben Sie einen aussagekräftigen Namen und wählen Sie aus der Dropdown-Liste :guilabel:`Rabatt` den Eintrag :guilabel:`itm`.
#. Wählen Sie :guilabel:`Speichern`.
#. Wählen Sie die Schaltfläche :guilabel:`Artikel auswählen` auf der Registerkarte :guilabel:`Stamm`.
#. Verschieben Sie den Artikel, der als Gratisartikel dienen soll, per Drag \& Drop in die rechte Liste des Zuordnungsfensters und schließen Sie das Zuordnungsfenster.
#. Optional: Legen Sie im Feld :guilabel:`Menge` fest, wie oft der Artikel in den Warenkorb gelegt wird.
#. Optional: Setzen Sie ein Häkchen bei :guilabel:`Multiplizieren`, wenn die Anzahl des Gratisartikels abhängig von der Anzahl der gekauften Artikel sein soll.
#. Wählen Sie :guilabel:`Speichern`.


#. Legen Sie fest, wo der Rabatt angezeigt werden soll: in der Artikelübersicht oder Detailansicht oder erst im Warenkorb.

   Typischerweise wollen Sie, dass der Gratisartikel erst im Warenkorb erscheint.

   Um das umzusetzen, folgen Sie im Schritt :ref:`Plazierung bestimmen <Rabatt-Plazierung-bestimmen>` (unter :ref:`betrieb/rabatte/rabatte:Anlegen und Verwalten von Rabatten`).

#. Stellen Sie sicher, dass der Rabatt aktiv ist.
#. Speichern Sie die Einstellungen.

|result|

Die Anzahl der kostenfreien Zugaben wird im Warenkorb berechnet. Der oder die Gratisartikel werden angezeigt.

.. figure:: ../../media/screenshots/oxbahi03.png
   :alt: Beispiel Artikel mit einem einzigen Gratisartikel im Warenkorb
   :width: 650
   :class: with-shadow

   Abb.: Beispiel Artikel mit einem einzigen Gratisartikel im Warenkorb

Dabei wird die Anzahl der rabattfähigen Artikel zunächst durch den Wert der Mindesteinkaufsmenge geteilt und anschließend mit dem Wert multipliziert, der bei :guilabel:`Menge` eingetragen ist.

Beispiel: Wurden 10 Artikel gekauft, auf die der Rabatt gewährt wird, die Mindesteinkaufsmenge ist 3 und die Menge der Zugabe 1, wird die Zugabe (10/3)*1 = 3 mal in den Warenkorb gelegt.

Ist die Menge der Zugabe 2, erhöht sich die Anzahl der Zugaben auf 6.


.. Intern: oxbahq, Status: