Preisauf- und abschläge festlegen
=================================

Für Zahlungsarten können Preisauf- und -abschläge definiert werden.

So können Sie Kosten, die für eine Zahlungsart entstehen, auf die Kunden umgelegen.

Ein Beispiel dafür ist die Zahlungsarten Nachnahme, bei der Gebühren anfallen (Beispiel: :ref:`oxbaft01`).

Für Zahlungsarten wie beispielsweise Vorauskasse können Sie aber auch einen Preisnachlass gewähren, da die Ware erst nach Zahlungseingang geliefert wird. Eine Art Skonto, denn das Zahlungsziel wird bei Vorauskasse immer eingehalten.

Legen Sie den Preisaufschlag oder Preisabschlag absolut oder prozentual fest. Ein absoluter Preisaufschlag ist eine Position im Warenkorb, die zum Warenwert dazugerechnet wird.

Wenn Sie den Preisauf- oder -abschlag in Prozent angegeben haben, muss er bei der Bestellung berechnet werden. Basis dafür ist der Warenkorb.

Folgende Warenkorbpositionen können bei der Berechnung berücksichtigt werden: Warenwert aller Artikel im Warenkorb, Rabatte, Gutscheine, Versandkosten und Geschenkverpackung/Grußkarte.

Wenn Sie einen negativen Preis angeben, führt führt das zu einem Preisnachlass.

|procedure|

1. Gehen Sie zu :menuselection:`Shopeinstellungen --> Zahlungsarten`.
#. Wählen Sie die gewünschte Zahlungsart aus der Zahlungsartenliste oder erstellen Sie Sie eine neue Zahlungsart.
#. Legen Sie Auf der Registerkarte :guilabel:`Stamm` im Eingabefeld :guilabel:`Preisauf-/abschlag (€)` (:ref:`oxbaft02`, Pos. 1) einen absoluten oder prozentualen Preis fest.

   Ein positiver Wert bewirkt einen Preisaufschlag, ein negativer einen Preisabschlag.

   .. _oxbaft02:

   .. figure:: ../../media/screenshots/oxbaft02.png
      :alt: Artikelübersicht mit und ohne Warenkorb
      :width: 650
      :class: with-shadow

      Abb.: Artikelübersicht mit und ohne Warenkorb

#. Wenn Sie einen :emphasis:`prozentualen` Preisauf- oder -abschlag festlegen, dann legen Sie unter :guilabel:`Basis für Preisaufschlag/-abschlag` (:ref:`oxbaft01`, Pos. 2) fest, welche Kosten für die Berechnung des Warenkorbwerts herangezogen werden sollen.
#. Speichern Sie Ihre Einstellungen.

|result|

Im Warenkorb wird der Aufschlag für die Zahlungsart Nachnahme angezeigt, in unserem Beispiel 7,50 Euro.

.. todo: #tbd: 7034 Bild neu machen

.. _oxbaft01:

.. figure:: ../../media/screenshots/oxbaft01.png
   :alt: Bestellung mit Zuschlag für Nachnahme
   :width: 650
   :class: with-shadow

   Abb.: Bestellung mit Zuschlag für Nachnahme

.. seealso:: :doc:`Zahlungsarten - Registerkarte Stamm <../zahlungsarten/registerkarte-stamm>`

.. Intern: oxbaft, Status: