Registerkarte Stamm: Rabatt anlegen
===================================

Nehmen Sie auf der Registerkarte :guilabel:`Stamm` die grundsätzlichen Einstellungen für Rabatte vorgenommen.

.. figure:: ../../media/screenshots/oxbahi01.png
   :alt: Rabatte - Registerkarte Stamm
   :width: 650
   :class: with-shadow

   Abb.: Rabatte - Registerkarte Stamm

Mit der Sprachumstellung am unteren linken Ende des Eingabebereichs lässt sich der Name des Rabattes auch direkt in einer weiteren Sprache bearbeiten.

Beachten Sie, dass die Einstellungen und die Sprachumstellung erst nach Anlegen des Rabattes verfügbar sind.

:guilabel:`Name`
   Name des Rabattes. Dieser wird im Warenkorb als eine Zeile in der Auflistung des Gesamtbetrages angezeigt, wenn der Rabatt global für den kompletten Warenkatalog des Shops gilt.

:guilabel:`Sortierung`
   Legen Sie mit numerischen Werten fest, in welcher Reihenfolge die Rabatte auf Artikel oder den Warenkorb angewendet werden. Der Rabatt mit der kleinsten Zahl wird zuerst berücksichtigt, der mit der größten Zahl zuletzt.

:guilabel:`Immer aktiv`
   Aktivieren Sie dieses Kontrollkästchen, damit der Rabatt dauerhaft gewährt wird. Ist das Kontrollkästchen nicht angehakt, wird für den Rabatt ein eingetragener Zeitraum berücksichtigt.

:guilabel:`Aktiv für Zeitraum` ... :guilabel:`(von)` ... :guilabel:`(bis)`
   Um Rabattaktionen vorbereiten und zeitlich steuern zu können, kann ein Zeitraum definiert werden, in dem ein Rabatt gültig ist. Anfang und Ende müssen im Format JJJJ-MM-TT HH:MM:SS angegeben werden. Datum und Zeit des Endes der Aktivierung sind nicht optional.

:guilabel:`Einkaufsmenge von` ... :guilabel:`bis` ...
   Soll der Rabatt nur dann gewährt werden, wenn eine bestimmte Menge von Artikeln im Warenkorb liegt, kann hier die minimale und maximale Einkaufsmenge vorgegeben werden. Wenn beide Werte 0 sind, gilt der Rabatt für alle Einkaufsmengen.

   Legen Sie mit Hilfe des Eingabefelds :guilabel:`Einkaufswert (€) von` oder :guilabel:`Einkaufsmenge von` auch fest, wie der Rabatt vom Preis abgezogen werden soll.

   Weitere Informationen finden Sie unter :ref:`betrieb/rabatte/rabatte:Anzeigen von Rabatten`.

:guilabel:`Einkaufswert (€) von` ... :guilabel:`bis` ...
   Geben Sie eine Spanne für den Gesamtpreis vor, auf den ein Rabatt gewährt werden soll. Sind beide Werte 0, gilt der Rabatt für jeden Einkaufswert.

   Legen Sie mit Hilfe des Eingabefelds :guilabel:`Einkaufswert (€) von` oder :guilabel:`Einkaufsmenge von` auch fest, wie der Rabatt vom Preis abgezogen werden soll.

   Weitere Informationen finden Sie unter :ref:`betrieb/rabatte/rabatte:Anzeigen von Rabatten`.

:guilabel:`Rabatt`
   Definieren Sie hier den Rabatt, der gewährt werden soll.

   Dieser kann prozentual, absolut oder als Stückzahl angegeben werden. Mit der Auswahlliste hinter dem Eingabefeld wird die Art des Rabattes ausgewählt.

   :guilabel:`abs`: Der Rabatt ist absolut, beispielsweise 5 €. |br|
   :guilabel:`%`: Der Rabatt ist prozentual, beispielsweise 10 Prozent vom Einkaufswert. |br|
   :guilabel:`itm`: Der Rabatt wird in Form eines kostenlosen Artikels (Dreingabe/Zugabe) gewährt.

:guilabel:`Artikel auswählen`
   Die Schaltfläche wird nur angezeigt, wenn der Rabatt ein kostenloser Artikel ist.

   Sie öffnet ein neues Fenster, in dem ein Artikel ausgewählt werden kann. In diesem Zuordnungsfenster werden in der linken Liste alle Artikel angezeigt.

   Die Anzeige kann auf eine Kategorie beschränkt werden, indem diese aus einer Dropdown-Liste ausgewählt wird.

   Artikel können auch nach Artikelnummer, Titel und/oder EAN gefiltert und sortiert werden. Der Artikel wird per Drag \& Drop in die rechte Liste verschoben. Es kann nur ein Artikel zugeordnet werden. Dessen Preis wird automatisch auf Null gesetzt, wenn er im Rahmen des Rabattes als Zugabe in den Warenkorb kommt.

:guilabel:`Drein/Zugabe` - :guilabel:`Menge`
   Das Eingabefeld wird nur angezeigt, wenn der Rabatt ein kostenloser Artikel ist.

   Geben Sie an, in welcher Menge der kostenlose Artikel als Rabatt gewährt wird.

   Wird beispielsweise 2 als Menge eingetragen, werden insgesamt zwei kostenlose Artikel in den Warenkorb gelegt, unabhängig davon, wie viele Artikel gekauft wurden.

   .. figure:: ../../media/screenshots/oxbahi03.png
      :alt: Artikel mit Gratisartikel im Warenkorb
      :width: 650
      :class: with-shadow

      Abb.: Artikel mit Gratisartikel im Warenkorb

      .. todo: #tbd: Bild neu

:guilabel:`Drein/Zugabe` - :guilabel:`Multiplizieren`
   Das Kontrollkästchen wird nur angezeigt, wenn der Rabatt ein kostenloser Artikel ist. Setzen Sie ein Häkchen, wenn die Menge der kostenlosen Artikel von der Anzahl der gekauften Artikel abhängen soll.

   Die Anzahl der Zugaben wird im Warenkorb berechnet. Dabei wird die Anzahl der rabattfähigen Artikel zunächst durch den Wert der Mindesteinkaufsmenge (Feld :guilabel:`Einkaufsmenge von ... bis`) geteilt und anschließend mit dem Wert multipliziert, der bei :guilabel:`Drein/Zugabe - Menge` eingetragen ist.

   Beispiel: Wurden 10 Artikel gekauft, auf die der Rabatt gewährt wird, die Mindesteinkaufsmenge ist 5 und die Menge der Zugabe 1, wird die Zugabe (10/5)*1 = 2 mal in den Warenkorb gelegt. Ist die Menge der Zugabe 2, erhöht sich die Anzahl der Zugaben auf 4.

:guilabel:`In Sprache`
   Der Rabatt lässt sich auch in weiteren aktiven Sprachen des Shops bearbeiten. Wählen Sie eine Sprache aus der Liste aus.

:guilabel:`Kopieren`
   Der Rabatt kann in eine aktive Sprache des Shops kopiert werden. Das ist Voraussetzung dafür, dass er in dieser Sprache bearbeitet werden kann. Ist der Rabatt in allen aktiven Sprachen des Shops vorhanden, werden die Schaltfläche und die Auswahlliste für die Sprache ausgeblendet.

:guilabel:`Länder zuordnen`
   Rabatte können auch länderspezifisch gelten. Ordnen Sie mit der Schaltfläche die Länder zu, aus denen Kunden bei einer Bestellung diesen Rabatt erhalten. Ohne eine solche Zuordnung ist der Rabatt für alle Länder gültig.

.. seealso:: :doc:`Zeitlich begrenzte Rabatte <zeitlich-begrenzte-rabatte>`

.. Intern: oxbahi, Status:, F1: discount_main.html