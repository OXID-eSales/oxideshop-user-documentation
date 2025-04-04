Anzeigereihenfolge von Artikeln in Kategorien festlegen
=======================================================

Legen Sie die Reihenfolge fest, in der Artikel in einer Kategorie angezeigt werden.

Sie können die Reihenfolge von Artikeln in Kategorien auf drei verschiedene Arten steuern:

* Automatisch sortieren – lassen Sie die Artikel anhand eines ausgewählten Felds wie Titel, Preis oder Erstellungsdatum automatisch in auf- oder absteigender Reihenfolge sortieren.
* Manuell anordnen – legen Sie die Reihenfolge der Artikel individuell fest, indem Sie die Artikel per Zuordnungsfenster sortieren.
* Sortieroptionen für Kunden anbieten – definieren Sie, nach welchen Kriterien Kundinnen und Kunden Artikellisten im Frontend selbst sortieren können (z. B. nach Preis, Bewertung oder Artikelnummer).

Artikel automatisch sortieren
-----------------------------

Wählen Sie ein Sortierkriterium, beispielsweise :guilabel:`Titel`, :guilabel:`Preis` oder :guilabel:`Angelegt am`, nach dem automatisch sortiert werden soll.

Legen Sie fest, ob die Artikel nach diesem Artikelmerkmal auf- oder absteigend sortiert werden sollen.

|procedure|

1. Wählen Sie :menuselection:`Artikel verwalten --> Kategorien`.
#. Wählen Sie in der Kategorieliste die gewünschte Kategorie.
#. Öffnen Sie auf der Registerkarte :guilabel:`Stamm` die Dropdown-Liste :guilabel:`Schnellsortierung`.
#. Wählen Sie ein Artikelmerkmal für die Schnellsortierung.
#. Wählen Sie :guilabel:`asc` oder :guilabel:`desc` für eine aufsteigende oder eine absteigende Sortierung.
#. Speichern Sie Ihre Einstellungen.

Artikel manuell anordnen
------------------------

Bringen Sie die Artikel einer Kategorie manuell in eine bestimmte Reihenfolge.

|procedure|

1. Wählen Sie :menuselection:`Artikel verwalten --> Kategorien`.
#. Wählen Sie die gewünschte Kategorie aus der Kategorieliste.
#. Stellen Sie sicher, dass auf der Registerkarte :guilabel:`Stamm` in der Dropdown-Liste :guilabel:`Schnellsortierung` die Option :guilabel:`keine Sortierung` gewählt ist.
#. Wählen Sie auf der Registerkarte :guilabel:`Sortierung` die Schaltfläche :guilabel:`Artikel sortieren`.
#. Verschieben Sie die Artikel in der gewünschten Reihenfolge in die rechte Liste des Zuordnungsfensters.
#. Wählen Sie die Schaltfläche :guilabel:`Neue Sortierung` speichern.

|result|

In der linken Liste wird die nun aktuelle Sortierung angezeigt (:ref:`oxbafq01`, Pos. 1). Die Spalte :guilabel:`Position` enthält die Werte, die die Sortierreihenfolge bestimmen.

.. _oxbafq01:

.. figure:: ../../media/screenshots/oxbafq01.png
   :alt: Artikelreihenfolge manuell festlegen
   :width: 650
   :class: with-shadow

   Abb.: Artikelreihenfolge manuell festlegen

Sortierung durch Kunden ermöglichen
-----------------------------------

Legen Sie fest, ob und nach welchen Kriterien Ihre Kunden die Artikel in Kategorien sortieren können.

|procedure|

1. Wählen Sie zu :menuselection:`Stammdaten --> Grundeinstellungen`.
#. Wählen Sie auf der Registerkarte :guilabel:`Einstell.` den Abschnitt :guilabel:`Artikel`.
#. Stellen Sie sicher, dass das Kontrollkästchen :guilabel:`Benutzer können Artikellisten sortieren` aktiviert ist (:ref:`oxbafq02`, Pos. 1).
#. Legen Sie die Felder für die Sortierung fest (:ref:`oxbafq02`, Pos. 2).

   Sie haben folgende Möglichkeiten:

   * ``oxtitle``: Titel (Name) der Artikel
   * ``oxprice``: Preis der Artikel
   * ``xvarminprice``: Der niedrigste Preis der Artikel, wenn Varianten mit verschiedenen Preisen verwendet werden.
   * ``oxartnum``: Artikelnummer
   * ``oxrating``: Die Bewertung der Artikel
   * ``oxstock``: aktueller Lagerbestand

   Jedes Feld muss in einer Zeile stehen.

   Die Sortierfelder entsprechen den Datenbankfeldern der Tabelle ``oxarticles``.

   .. _oxbafq02:

   .. figure:: ../../media/screenshots/oxbafq02.png
      :alt: Kundenseitiges Sortieren konfigurieren
      :width: 650
      :class: with-shadow

      Abb.: Kundenseitiges Sortieren konfigurieren

#. Speichern Sie Ihre Einstellungen.

|result|

In unserem Beispiel können die Kunden zusätzlich zu Titel und Preis auch nach der Artikelnummer sortieren (:ref:`oxbafq02`, Pos. 3).

Dafür haben wir in den Stammdaten den standardmäßig eingetragenen Feldern ``oxtitle``  und ``oxvarminprice``  das Feld ``oxartnum``  hinzugefügt (:ref:`oxbafq02`, Pos. 2).

.. seealso:: :doc:`Kategorien - Registerkarte Stamm <../kategorien/registerkarte-stamm>` | :doc:`Kategorien - Registerkarte Sortierung <../kategorien/registerkarte-sortierung>`

.. Intern: oxbafq, Status: