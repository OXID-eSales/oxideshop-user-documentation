Hauptkategorie festlegen
========================

Ordnen Sie einen Artikel mehr als einer Kategorie zu.

Legen Sie jedoch in diesem Fall eine Kategorie als Hauptkategorie fest.

|background|

Das Festlegen einer Hauptkategorie ist aus folgenden Gründen notwendig:

* Ihr OXID eShop kann in bestimmten Situationen entscheiden, in welcher Kategorie der Artikel angezeigt wird.

  Ruft der Kunde beispielsweise einen Artikel über die shop-eigene Suche oder über die Tags auf, wird dieser Artikel in der definierten Hauptkategorie angezeigt.

* Sie vermeiden sogenannten Duplicate Content.

  Ein Artikel, der in mehreren Kategorien vorkommt, hat mehrere URLs. Diese zeigen auf dessen Detailseite und würden so identischen Inhalt präsentieren. Suchmaschinen wie Google, Bing und Yahoo! wollen ihren Nutzern Suchergebnisse jedoch ohne Redundanzen auflisten.

  Die Lösung sind Canonical Tags oder Canonical Links, die bei inhaltlich identischen Seiten auf die Originalseite verweisen. Im OXID eShop ist das die Detailseite des Artikels mit der Hauptkategorie in der URL.

  Die Canonical Tags werden im OXID eShop grundsätzlich gesetzt – auch wenn ein Artikel nur einer Kategorie zugeordnet ist.

  Wenn Sie keine Hauptkategorie festgelegt haben, wird diejenige Kategorie verwendet, welcher der Artikel als Erstes zugeordnet wurde.


|procedure|

Um die Hauptkategorie eines Artikels festzulegen, tun Sie Folgendes.

1. Wählen Sie :menuselection:`Artikel verwalten --> Artikel`.
#. Wählen Sie den gewünschten Artikel aus der Artikelliste.
#. Wählen Sie auf der Registerkarte :guilabel:`Erweitert` die Schaltfläche :guilabel:`Kategorien zuordnen`.
#. Markieren Sie die als Hauptkategorie vorgesehene Kategorie.
#. Wählen Sie die Schaltfläche :guilabel:`Als Hauptkat. setzen` (:ref:`oxbafp01`, Pos. 1: in unserem Beispiel ordnen wir den Regenschirm dem Zubehör als Hauptkategorie zu).
#. Schließen Sie das Zuordnungsfenster.

.. _oxbafp01:

.. figure:: ../../media/screenshots/oxbafp01.png
   :alt: Hauptkategorie festlegen
   :width: 650
   :class: with-shadow

   Abb.: Hauptkategorie festlegen

|result|

In unserem Beispiel enthält der Canonical Link im Seitenquelltext der Detailseite des Regenschirms die Zuordnung zur Kategorie Zubehör:

``<link rel="canonical" href="http://localhost.local/Ersatzteile/Zubehoer/Royal.html">``

.. todo: EN: <link rel="canonical" href="http://localhost.local/en/Spare-parts/Accessories/Royal.html">

.. seealso:: :doc:`Artikel - Registerkarte Erweitert <../artikel/registerkarte-erweitert>` | `Canonical Link <http://de.wikipedia.org/wiki/Canonical_Link>`_ (Wikipedia)


.. Intern: oxbafp, Status: