Registerkarte Stamm
===================

Konfigurieren Sie auf der Registerkarte :guilabel:`Stamm` die Versandart.

Ordnen Sie der Versandart beispielsweise Versandkostenregeln und Länder zu. Legen Sie eine Tracking-URL fest, damit das System einen Tracking-Link an Ihren Kunden senden kann.

.. image:: ../../media/screenshots/oxbade01.png
   :alt: Versandarten - Registerkarte Stamm
   :height: 339
   :width: 650

:guilabel:`Name`
   Tragen Sie die Bezeichnung der Versandart ein. Diese wird dem Kunden im Bestellschritt 3 angezeigt.

   Sind mehrere Versandarten gültig, muss eine davon aus einer Dropdown-Liste ausgewählt werden.

:guilabel:`Immer aktiv`
   Damit die Versandart aktiv ist und verwendet werden kann, markieren Sie das Kontrollkästchen.

:guilabel:`Aktiv für Zeitraum`
   Legen Sie einen Zeitraum fest, in dem die Versandart aktiv sein soll.

   Das Eingabeformat ist :code:`YYY-MM-DD HH:MM:SS`.

   Damit der Zeitraum berücksichtigt wird, stellen Sie sicher, dass :guilabel:`Immer aktiv` nicht markiert ist.

:guilabel:`Sortierung`
   Legen Sie die Reihenfolge der Versandarten in der Dropdown-Liste fest.

   Die Versandart mit der kleinsten Zahl steht als erste zur Auswahl und ist damit vorausgewählt.

.. _tracking-url-shipping-method:

:guilabel:`Tracking-URL`
   Legen Sie eine Tracking-URL fest.

   Beispiel (:ref:`oxbade02`, Pos. 1): :code:`https://www.dhl.com/de-de/home/tracking/tracking-express.html?tracking-id=##ID##`

   Den Platzhalter :code:`##ID##` ersetzt das System durch die jeweilige Paket-ID der Bestellung (je nach Versanddienstleister Tracking Code, Paketscheinnummer, Paketreferenz, Sendungsnummer usw.).

   Die Paket-ID geben Sie ein, wenn Sie die jeweilige Bestellung bearbeiten.
   |br|
   Weitere Informationen finden Sie unter :ref:`Tracking-Code <tracking-url-orders>`.

   .. _oxbade02:

   .. figure:: ../../media/screenshots/oxbade02.png
      :alt: Tracking-URL für eine Versandart festlegen
      :width: 650
      :class: with-shadow

      Abb.: Tracking-URL für eine Versandart festlegen

   Ergebnis: Die Tracking-URL und die konkrete Paket-ID einer Bestellung werden zu einem Tracking-Link zusammengefügt. Der Tracking-Link wird dem Kunden zur Sendungsverfolgung mit der Versandbestätigungs-E-Mail zugeschickt.

   Der Besteller kann den Tracking-Link auch in der Kundenbestellhistorie im Frontend unter :menuselection:`Mein Konto --> Bestellhistorie` anzeigen.

   Wenn Sie für eine Versandart keine eigene Tracking-URL festlegen, verwendet das System die Tracking-URL, die Sie unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Weitere Einstellungen` festgelegt haben.

   .. todo: #tbd 7.x: create Ref hier hin sobald Doku existiert für :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Weitere Einstellungen` / :menuselection:`Master Settings --> Core Settings --> Settings --> Other Settings`, :guilabel:`Standard shipping provider tracking URL`

:guilabel:`In Sprache`
   Wenn Sie die Versandart in einer anderen aktiven Sprache des Shops bearbeiten möchten, wählen Sie die gewünschte Sprache aus der Dropdown-Liste aus.

:guilabel:`Kopieren`
   Kopieren Sie eine Versandart, um sie in einer weiteren aktiven Sprache bearbeiten zu können.

   Wählen Sie die Sprache aus der Dropdown-Liste aus und drücken Sie die Schaltfläche :guilabel:`Kopieren`. Ist keine weitere aktive Sprache im Shop vorhanden, wird diese Schaltfläche nicht angezeigt.

:guilabel:`Versandkostenregeln zuordnen`
   Ordnen Sie der Versandart mindestens eine Versandkostenregel zu.

   Über die Schaltfläche :guilabel:`Versandkostenregeln zuordnen` öffnen Sie ein neues Fenster. In diesem Zuordnungsfenster werden in der linken Liste alle Versandkostenregeln angezeigt.

   Filtern Sie die Versandkostenregeln nach Titel, Kosten und/oder Typ (absoluter oder prozentualer Preis) und sortieren Sie sie.

   Verschieben Sie die Versandkostenregeln per Drag \& Drop in die rechte Liste. Die Zuordnung ist damit abgeschlossen.

:guilabel:`Länder zuordnen`
   Um eindeutige Zahlungs- und Versandbedingungen zu haben, ordnen Sie der Versandart Länder zu.

   Sind die Länder zugeordnet und ein Kunde bestellt aus einem Land, dem keine Versandart zugeordnet ist, so erhält der Kunde die folgende Meldung: \"Derzeit ist keine Versandart für dieses Land definiert. Wir werden versuchen, Liefermöglichkeiten zu finden und Sie über die Versandkosten informieren.\". Die Zahlungsarten werden ihm nicht angezeigt.

   Ohne Länderzuordnung gilt die Versandart für alle Länder.

   Öffnen Sie mit der Schaltfläche :guilabel:`Länder zuordnen` ein neues Fenster: In der linken Liste werden alle aktiven Länder angezeigt.

   Sortieren und filtern Sie die Länder nach Titel und/oder Länderkürzel (ISO Alpha 2).

   Ziehen Sie die gewünschten Länder mit der Maus in die Liste auf der rechten Seite. Eine Mehrfachauswahl ist bei gedrückter Strg-Taste möglich. Damit ist die Zuordnung zur Versandart abgeschlossen.


.. Intern: oxbade, Status:, F1: deliveryset_main.html