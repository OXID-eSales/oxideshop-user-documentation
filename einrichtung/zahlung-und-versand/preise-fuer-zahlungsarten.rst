Preisaufschläge oder -abschläge festlegen
=========================================

Legen Sie Preisaufschläge oder -abschläge für Zahlungsarten fest, um entstehende Kosten direkt an Ihre Kundschaft weiterzugeben oder Preisvorteile anzubieten.

Beispiel: Bei der Zahlungsart :guilabel:`Nachnahme` fallen Gebühren an, die etwa vom Paketdienst erhoben werden können (:ref:`oxbaft01`). Für :guilabel:`Vorauskasse` können Sie einen Preisnachlass einräumen, da der Zahlungseingang vor Lieferung erfolgt und somit das Zahlungsziel immer eingehalten wird – vergleichbar mit einem Skonto.

Definieren Sie den Preisaufschlag oder -abschlag als absoluten Betrag oder in Prozent. Ein absoluter Wert wird direkt zum Warenwert im Warenkorb addiert. Prozentuale Werte berechnet der Shop beim Bestellvorgang auf Basis definierter Warenkorbpositionen.

Folgende Positionen können Sie zur Berechnung heranziehen – einzeln oder kombiniert:

* Warenwert der Artikel
* Rabatte
* Gutscheine
* Versandkosten
* Geschenkverpackungen und Grußkarten

.. note::
   Ein negativer Betrag reduziert den Gesamtpreis und entspricht einem Nachlass.

|procedure|

1. Wählen Sie :menuselection:`Shopeinstellungen --> Zahlungsarten`.
#. Wählen Sie eine bestehende Zahlungsart oder legen Sie eine neue an.
#. Geben Sie auf der Registerkarte :guilabel:`Stamm` im Feld :guilabel:`Preisauf-/abschlag (€)` (:ref:`oxbaft02`, Pos. 1) den gewünschten Betrag ein – positiv für einen Aufschlag, negativ für einen Abschlag.

   .. _oxbaft02:

   .. figure:: ../../media/screenshots/oxbaft02.png
      :alt: Preisaufschlag oder -abschlag festlegen
      :width: 650
      :class: with-shadow

      Abb.: Preisaufschlag oder -abschlag festlegen

#. Wenn Sie einen prozentualen Wert verwenden, legen Sie im Feld :guilabel:`Basis für Preisauf-/abschlag` (:ref:`oxbaft01`, Pos. 2) fest, welche Warenkorbpositionen berücksichtigt werden sollen.
#. Speichern Sie Ihre Einstellungen.

|result|

Im Warenkorb zeigt der Shop den Preisaufschlag für die gewählte Zahlungsart an. In unserem Beispiel berechnet der Shop bei Nachnahme einen Zuschlag von 7,50 € (:ref:`oxbaft01`, Pos. 1).

.. _oxbaft01:

.. figure:: ../../media/screenshots/oxbaft01.png
   :alt: Bestellung mit Zuschlag für Nachnahme
   :width: 650
   :class: with-shadow

   Abb.: Bestellung mit Zuschlag für Nachnahme

.. seealso:: :doc:`Zahlungsarten – Registerkarte Stamm <../zahlungsarten/registerkarte-stamm>`

.. Intern: oxbaft, Status:


