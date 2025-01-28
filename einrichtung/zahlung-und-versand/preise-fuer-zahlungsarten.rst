Preisaufschläge oder -abschläge festlegen
=========================================

Definieren Sie Preisaufschlag oder -abschläge für Zahlungsarten.

So können Sie die für eine Zahlungsart entstehenden Kosten direkt auf die Kunden umlegen.

Ein Beispiel dafür ist die Zahlungsart Nachnahme, bei der Gebühren anfallen, die von externen Dienstleistern wie dem Paketdienst erhoben werden können (Beispiel: :ref:`oxbaft01`).

Für Zahlungsarten wie beispielsweise Vorauskasse können Sie aber auch einen Preisnachlass gewähren, da die Ware erst nach Zahlungseingang geliefert wird. Eine Art Skonto, denn das Zahlungsziel wird bei Vorauskasse immer eingehalten.

Legen Sie den Preisaufschlag oder Preisabschlag absolut oder prozentual fest. Ein absoluter Preisaufschlag wird dem Warenwert im Warenkorb hinzugefügt.

Wenn Sie den Preisaufschlag oder -abschlag in Prozent angegeben haben, muss er bei der Bestellung berechnet werden. Die Berechnungsgrundlage dafür ist der Warenkorb.

Folgende Warenkorbpositionen können bei der Berechnung einbezogen werden (einzeln oder kombiniert): Warenwert aller Artikel, Rabatte, Gutscheine, Versandkosten und Geschenkverpackungen/Grußkarten.

Wenn Sie einen negativen Preis angeben, führt das zu einem Preisnachlass.

|procedure|

1. Wählen Sie :menuselection:`Shopeinstellungen --> Zahlungsarten`.
#. Wählen Sie die gewünschte Zahlungsart aus der Zahlungsartenliste oder erstellen Sie eine neue Zahlungsart.
#. Legen Sie auf der Registerkarte :guilabel:`Stamm` im Eingabefeld :guilabel:`Preisauf-/abschlag (€)` (:ref:`oxbaft02`, Pos. 1) einen absoluten oder prozentualen Preis fest.

   Ein positiver Wert bewirkt einen Preisaufschlag, ein negativer einen Preisabschlag.

   .. _oxbaft02:

   .. figure:: ../../media/screenshots/oxbaft02.png
      :alt: Preisaufschlag oder -abschlag festlegen
      :width: 650
      :class: with-shadow

      Abb.: Preisaufschlag oder -abschlag festlegen

#. Wenn Sie einen :emphasis:`prozentualen` Preisaufschlag oder -abschlag festlegen, dann legen Sie unter :guilabel:`Basis für Preisaufschlag/-abschlag` (:ref:`oxbaft01`, Pos. 2) fest, welche Kosten für die Berechnung des Warenkorbwerts herangezogen werden sollen.
#. Speichern Sie Ihre Einstellungen.

|result|

Im Warenkorb wird der Aufschlag für die Zahlungsart Nachnahme angezeigt, in unserem Beispiel 7,50 Euro (:ref:`oxbaft01`, Pos. 1).

.. _oxbaft01:

.. figure:: ../../media/screenshots/oxbaft01.png
   :alt: Bestellung mit Zuschlag für Nachnahme
   :width: 650
   :class: with-shadow

   Abb.: Bestellung mit Zuschlag für Nachnahme

.. seealso:: :doc:`Zahlungsarten - Registerkarte Stamm <../zahlungsarten/registerkarte-stamm>`

.. Intern: oxbaft, Status: