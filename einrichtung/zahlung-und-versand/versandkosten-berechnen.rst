Standard-Versandkosten berechnen
================================

.. todo: #SB: Use case klären: Für welche Zahlungsarten? Was genau ist der Benefit?
.. todo: #SB: Ab welche Version haben wir die Funktion?

Um Zahlungen mit Zahlungsdienstleistern zu optimieren, stellen Sie durch Standardversandkosten sicher, dass der Wert des Warenkorbs ungefähr dem Wert entspricht, der beim Checkout vom PayPal-Konto des Kunden eingezogen wird.


|background|

Wenn ein Kunde beispielsweise PayPal Express nutzt und einen Artikel in den Warenkorb legt, autorisiert er eine Zahlung in Höhe des Warenkorbwerts zuzüglich einer Toleranz von etwa 5 % für Versandkosten.

Im Fall von niedrigpreisigen Artikeln kann es sein, dass der Anteil der Versandkosten mehr als 5 % des Artikelpreises beträgt.

Beispiel: Der Artikelpreis ist 5 Euro, die Versandkosten betragen 4 Euro. Die Toleranz ist bei weitem überschritten.

Wenn PayPal dauerhaft finanzielle Reserven vorhalten muss, weil die realen Versandkosten dauerhaft von den Versandkosten abweichen, die PayPal schätzt und die PayPal Express autorisiert, dann kann es für PayPal schwierig werden, Ihnen weiterhin die Zahlungsart PayPal Express bereitzustellen.


|procedure|

.. todo: #SB: Wie genau gehe ich vor?

1. Legen Sie unter :menuselection:`Shopeinstellungen --> Versandarten` eine Standard-Versandart an.

   Dies ist die Versandart, welche die typischen Käufe in Ihrem OXID eShop (also etwa 80 % der Fälle) abdeckt.

#. Wählen Sie :menuselection:`Stammdaten --> Grundeinstellungen`.
#. Öffnen Sie auf der Registerkarte :guilabel:`Einstell.` den Bereich :guilabel:`Weitere Einstellungen`.
#. Markieren Sie das Kontrollkästchen :guilabel:`Versandkosten auch dann berechnen, wenn der Kunde noch nicht eingeloggt ist` (:ref:`oxbaka01`).

   .. _oxbaka01:

   .. figure:: /media/screenshots/oxbaka01.png
      :alt: Berechnen von Standard-Versandkosten aktivieren
      :width: 650
      :class: with-shadow

      Abb.: Berechnen von Standard-Versandkosten aktivieren

|result|

Um die Versandkosten und den gesamten Wert eines Warenkorb eines nicht angemeldeten Kunden zu schätzen, verwendet Ihr Zahlungsdienstleister diejenige Zahlungsart, die laut Versandkostenregel als erstes zutrifft.

Das ist in den meisten Fällen die von Ihnen definierte Standard-Versandart.

.. todo: #SB: Use case aus Kundensicht: Wie wird dadurch die Shop-Experience verbessert und damit indirekt der Nutzen des Shopbetreibers
.. todo: #SB: In welchem Fall will ich die Option NICHT aktivieren?

.. todo: EN:
1. Wählen Sie :menuselection:`Master Settings --> Core Settings`.
#. Öffnen Sie auf der Registerkarte :guilabel:`Settings.` den Bereich :guilabel:`Other settings`.
#. Markieren Sie das Kontrollkästchen :guilabel:`Calculate default Shipping costs when ser is not logged in yet`.

.. Intern: oxbaka, Status: