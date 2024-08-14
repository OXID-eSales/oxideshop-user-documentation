Attribute
=========

Artikel haben standardmäßig eine Reihe von Eigenschaften, mit denen sie charakterisiert werden können. Dazu gehören beispielsweise die Standard-Attribute Gewicht, Abmessungen oder Menge.

Mit benutzerdefinierten Attributen können Sie als Shopbetreiber eigene Artikeleigenschaften definieren und diese dem jeweiligen Artikel mit einem entsprechenden Wert zuweisen.

Attribute anzeigen
------------------
.. todo: Folgendes geht zur Zeit nicht im APEX-Theme: OXDEV-8565

Zeigen Sie Attribute auf der Detailseite oder im Bestellprozess an.

|procedure|

* Um Attribute in der Detailansicht des Produkts unter :guilabel:`Spezifikation` einzublenden, stellen Sie sicher, dass den Attributen Werte zugewiesen sind.
* Um Attribute beim Artikel im Warenkorb und beim Bestellabschluss anzuzeigen, tun Sie Folgendes:

  a. Wählen Sie unter :menuselection:`Artikel verwalten --> Attribute` das Attribut.
  #. Stellen Sie sicher, dass das Kontrollkästchen :guilabel:`Wert des Attributs für Artikel im Bestellprozess anzeigen` markiert ist.


Filtern mit Attribut-Werten ermöglichen
---------------------------------------
.. todo: Folgendes geht zur Zeit nicht im APEX-Theme: OXDEV-8571; klären: kann ich mehrere Filter anlegen?

Um das Filtern von Produkten zu ermöglichen, blenden Sie in der Kategorieübersicht des Shops eine Dropdown-Liste aller Werte des Attributes ein.

|procedure|

1. Wählen Sie unter :menuselection:`Artikel verwalten --> Attribute` das Attribut.
#. Wählen Sie auf der Registerkarte :guilabel:`Kategorien` die Schaltfläche :guilabel:`Kategorien zuordnen`.

Ähnliche Produkte anzeigen
--------------------------

Nutzen Sie Attribute, um ähnliche Artikel zu erkennen und auf der Detailseite zu präsentieren (:ref:`oxbaff01`).

.. _oxbaff01:

.. figure:: ../../media/screenshots/oxbaff01.png
   :alt: Ähnliche Produkte anzeigen
   :width: 300
   :class: with-shadow

   Abb.: Ähnliche Produkte anzeigen

|procedure|

1. Legen Sie die Anzahl ähnlicher Artikel fest, die bei einem Artikel angezeigt werden.

   Wählen Sie dazu im Administrationsbereich unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Artikel` das Eingabefeld :guilabel:`Anzahl ähnlicher Artikel, die bei einem Artikel angezeigt werden`.

#. Stellen Sie unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Artikel` auf der Registerkarte :guilabel:`Perform.` sicher, dass das Kontrollkästchen :guilabel:`Ähnliche Artikel laden` markiert ist.
#. Tun Sie unter :menuselection:`Artikel verwalten --> Attribute` Folgendes:

   a. Legen Sie benutzerdefinierte Attribute an, um möglichst viele charakteristische Merkmale Ihrer Produkte abzubilden.

      Hintergrund: Je größer die Schnittmenge gemeinsamer Attribute, desto "ähnlicher" sind die Produkte.

      Beispiel: Koffer und Fahrzeuge werden als ähnliche Produkte angezeigt, wenn sie lediglich das Attribut :technicalname:`Gewicht` gemeinsam haben.

      Damit bei einem Fahrzeug nur andere :emphasis:`Fahrzeuge` als ähnliche Produkte erscheinen, müssen Sie weitere Attribute zuordnen.

      Die größte Ähnlichkeit haben Produkte, die ein spezifisches Merkmal teilen, beispielsweise bei Fahrzeugen die Beschleunigung.

      .. note::
         Die spezifischen :emphasis:`Werte`, die Sie den Attributen pro Produkt zuordnen, beeinflussen :emphasis:`nicht` die Ähnlichkeit.

         Beispiel: Ihre Produkte haben nur das Attribut :technicalname:`Gewicht` gemeinsam. Fahrzeuge wiegen zwischen 1600 kg und 2500 kg, Regenschirme zwischen 1 kg und 1,5 kg. Ein Fahrzeug mit 2000 kg ist einem Regenschirm mit 1 kg genau so ähnlich wie einem anderen Fahrzeug.

   #. Ordnen Sie den benutzerdefinierten Attributen jeweils die betreffenden Produkte zu.

      Wählen Sie dazu das Attribut und wählen Sie :guilabel:`Produkte zuordnen`.

#. Ordnen Sie den betreffenden Produkten möglichst viele charakterisierende Merkmale (Attribute) zu.

   * Um einem Produkt ein Standard-Attribut zuzuordnen, tun Sie Folgendes:

     a. Wählen Sie unter :menuselection:`Artikel verwalten --> Artikel` das Produkt.
     #. Wählen Sie :guilabel:`Erweitert`.
     #. Legen Sie Gewicht, Maße oder Menge fest.

   * Um ein benutzerdefiniertes Attribut zuzuweisen, tun Sie Folgendes:

     a. Wählen Sie unter :menuselection:`Artikel verwalten --> Artikel` das Produkt.
     #. Wählen Sie :guilabel:`Auswahl` (:ref:`oxbaff02`, Pos. 1).
     #. Wählen Sie :guilabel:`Attribute zuordnen` (:ref:`oxbaff02`, Pos. 2).
     #. Ordnen Sie dem Artikel das Attribut zu.
     #. Klicken Sie auf den Namen des Attributs.

        Ein Eingabefeld für das Eingeben des Attribut-Werts erscheint (:ref:`oxbaff02`, Pos. 3).

     #. Geben Sie den Wert ein und speichern Sie Ihre Eingabe.


     .. _oxbaff02:

     .. figure:: ../../media/screenshots/oxbaff02.png
        :alt: Benutzerdefiniertes Attribut zuweisen und Wert festlegen
        :width: 650
        :class: with-shadow

        Abb.: Benutzerdefiniertes Attribut zuweisen und Wert festlegen


-----------------------------------------------------------------------------------------

Registerkarte Stamm
-------------------
**Inhalte**: Attribut eines Artikels, Sortierung der Attribute, Attribut im Bestellprozess, kaufrelevante Informationen, Button-Lösung, Attribut zu Artikeln zuordnen, ähnliche Artikel |br|
:doc:`Artikel lesen <registerkarte-stamm>` |link|

Registerkarte Kategorien
------------------------
**Inhalte**: Attribut zu Kategorien zuordnen, Kategorien nach Attributen filtern, Sortierung der Attribute |br|
:doc:`Artikel lesen <registerkarte-kategorien>` |link|

Registerkarte Mall
------------------
Nur in der Enterprise Edition vorhanden |br|
**Inhalte**: Attribute vererben, Attribute verknüpfen, Elternshop, Subshop, Supershop, Multishop, Mall, Enterprise Edition |br|
:doc:`Artikel lesen <registerkarte-mall>` |link|

.. seealso:: :doc:`Artikel <../artikel/artikel>` | :doc:`Artikel - Registerkarte Auswahl <../artikel/registerkarte-auswahl>`

.. Intern: oxbaff, Status: