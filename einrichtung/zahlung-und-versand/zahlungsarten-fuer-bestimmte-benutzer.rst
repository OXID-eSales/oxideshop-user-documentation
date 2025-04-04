Zahlungsarten für bestimmte Benutzer festlegen
==============================================

Treffen Sie Shopbetreiber eine grundsätzliche Entscheidung darüber, welche Zahlungsarten Sie Ihren Kunden anbieten möchten.

Legen Sie fest, bei welchen Kunden es akzeptabel ist, die Ware vor dem Zahlungseingang zu verschicken, und bei welchen Kunden diese Vorleistung nicht sinnvoll ist.

Die Zahlung auf Rechnung ist bei Kunden sehr beliebt, da sie die Ware vor der Bezahlung prüfen oder testen können. Für den Shopbetreiber entsteht dadurch ein Risiko – denn nicht jeder Kunde zahlt pünktlich oder überhaupt.

Im OXID eShop haben Sie zwei Möglichkeiten, Zahlungsarten nur für bestimmte Benutzer anzubieten:

* Bonitätsindex bei Zahlungsarten hinterlegen
* Zahlungsarten Benutzergruppen zuordnen

Bonitätsindex bei Zahlungsarten hinterlegen
-------------------------------------------

Eine davon ist der Bonitätsindex, den Sie bei den Zahlungsarten hinterlegen können.

Diese Einstellung steuert, dass nur Kunden diese Zahlungsart im Bestellprozess angezeigt bekommen, deren Bonität größer gleich dem Bonitätsindex der Zahlungsart ist.

Diese Option ist mit hohem Aufwand verbunden, da Sie die Bonität für jeden Benutzer individuell pflegen müssen.

1. Definieren Sie für die Zahlungsart die vorausgesetzte Bonität.

   a. Gehen Sie zu :menuselection:`Shopeinstellungen --> Zahlungsarten`.
   #. Wählen Sie die gewünschte Zahlungsart aus der Liste der Zahlungsarten.
   #. Vergeben Sie auf der Registerkarte :guilabel:`Stamm` einen Bonitätsindex.
   #. Speichern Sie die Eingabe.

2. Legen Sie für jeden Benutzer einzeln die Bonität fest.

   a. Gehen Sie zu :menuselection:`Benutzer verwalten --> Benutzer`.
   #. Wählen Sie den gewünschten Benutzer aus der Liste der Benutzer.
   #. Geben Sie einen Wert in das Feld :guilabel:`Bonität` auf der Registerkarte :guilabel:`Erweitert` ein.
   #. Speichern Sie die Eingabe.

Zahlungsarten Benutzergruppen zuordnen
--------------------------------------

Die zweite Möglichkeit für kundenbezogene Zahlungsarten im Bestellprozess wird durch die Zuordnung von Benutzergruppen zu den Zahlungsarten erreicht.

Damit können Sie beispielsweise festlegen, dass nur der Benutzergruppe Händler die Zahlung auf Rechnung eingeräumt ist.

|procedure|

1. Gehen Sie zu :menuselection:`Shopeinstellungen --> Zahlungsarten`.
#. Wählen Sie die gewünschte Zahlungsart aus der Liste der Zahlungsarten.
#. Betätigen Sie die Schaltfläche :guilabel:`Benutzergruppen zuordnen` auf der Registerkarte :guilabel:`Stamm`.
#. Verschieben Sie die Benutzergruppe per Drag \& Drop in die rechte Liste des Zuordnungsfensters.
#. Schließen Sie das Zuordnungsfenster.

.. seealso:: :doc:`Zahlungsarten - Registerkarte Stamm <../zahlungsarten/registerkarte-stamm>` | :doc:`Benutzer - Registerkarte Erweitert <../../betrieb/benutzer/registerkarte-erweitert>`

.. Intern: oxbafu, Status: