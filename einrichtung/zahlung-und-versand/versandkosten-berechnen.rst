Versandkosten in der Warenkorbübersicht anzeigen
================================================

.. todo: #SB: Ab welcher Version haben wir die Funktion? -- seit immer drin

Zeigen Sie die Versandkosten bereits in der Warenkorbübersicht an (:ref:`oxbaka02`, Pos. 1).

Tun Sie das jedoch :emphasis:`nur dann`, wenn es technisch möglich ist, die Versandkosten korrekt zu bestimmen, ohne dass sich der Kunde in Ihrem OXID eShop angemeldet hat.

Beispiel: Sie haben für alle Produkte und Lieferländer eine Versandkostenpauschale. In solchen Fällen kennen Sie die Versandkosten, ohne beispielsweise die Lieferadresse des Kunden zu wissen.

|procedure|

.. attention::

   **Preisangabenverordnung**

   Stellen Sie sicher, dass Sie nicht gegen die Preisangabenverordnung oder andere rechtliche Rahmenbedingungen verstoßen.

   Stellen Sie deshalb sicher, dass Sie die tatsächlichen Versandkosten anzeigen, wenn Sie die Funktion nutzen.

   Wenn das nicht möglich ist, bevor sich der Kunde im Checkout angemeldet und eine Versandart gewählt hat, dann vermeiden Sie es, die Funktion zu nutzen und die Versandkosten in der Warenkorbübersicht anzuzeigen.

   Zeigen Sie stattdessen beispielsweise einen Link zu einer Seite mit einer Versandkostenübersicht an (:ref:`oxbaka03`, Pos. 1), damit sich der Kunde vorab informieren kann. Passen Sie dazu das Template an.

   Im Demo-Shop ab OXID eShop Version 7 lenkt der Link :guilabel:`Versandkosten` (:ref:`oxbaka03`, Pos. 1) auf der Produkt-Detailseite auf die Seite :guilabel:`Zahlung und Lieferung`. Diese Seite wiederum bearbeiten Sie unter :menuselection:`Kundeninformation --> CMS-Seiten`. Der Titel ist :technicalname:`Zahlung und Lieferung`, Ident ist :technicalname:`oxdeliveryinfo`).

   .. _oxbaka03:

   .. figure:: /media/screenshots/oxbaka03.png
      :alt: Link zur Versandkostenübersicht
      :width: 650
      :class: with-shadow

      Abb.: Link zur Versandkostenübersicht

1. Legen Sie unter :menuselection:`Shopeinstellungen --> Versandarten` eine Standard-Versandart oder mehrere Versandarten mit identischen Versandkosten für den Versand an.
#. Legen Sie die Versandkostenregeln an und ordnen Sie die Versandarten zu.
#. Wählen Sie :menuselection:`Stammdaten --> Grundeinstellungen`.
#. Öffnen Sie auf der Registerkarte :guilabel:`Einstell.` den Bereich :guilabel:`Weitere Einstellungen`.
#. Markieren Sie das Kontrollkästchen :guilabel:`Versandkosten auch dann berechnen, wenn der Kunde noch nicht eingeloggt ist` (:ref:`oxbaka01`, Pos. 1).

   .. _oxbaka01:

   .. figure:: /media/screenshots/oxbaka01.png
      :alt: Anzeigen von Standard-Versandkosten aktivieren
      :width: 650
      :class: with-shadow

      Abb.: Anzeigen von Standard-Versandkosten aktivieren

|result|

Die Versandkosten werden angezeigt (:ref:`oxbaka02`, Pos. 1).

.. note::

   **Mehrere Versandarten**

   Technisch ist es so, dass die Versandkosten der :emphasis:`ersten` Versandart, die entsprechend Ihrer Versandkostenregeln anwendbar ist, angezeigt werden.

   Weil Sie die Versandarten so konfiguriert haben, dass die Versandkosten immer gleich sind, ist es möglich, dass der Kunde im Checkout nach der Anmeldung eine andere Versandart wählt. Es wird in jedem Fall der korrekte Endpreis wie im Checkout angezeigt.

.. _oxbaka02:

.. figure:: /media/screenshots/oxbaka02.png
   :alt: Versandkosten in der Warenkorbübersicht anzeigen
   :width: 650
   :class: with-shadow

   Abb.: Versandkosten in der Warenkorbübersicht anzeigen



.. todo: EN:
    1. Wählen Sie :menuselection:`Master Settings --> Core Settings`.
    #. Öffnen Sie auf der Registerkarte :guilabel:`Settings.` den Bereich :guilabel:`Other settings`.
    #. Markieren Sie das Kontrollkästchen :guilabel:`Calculate default Shipping costs when ser is not logged in yet`.

.. Intern: oxbaka, Status: