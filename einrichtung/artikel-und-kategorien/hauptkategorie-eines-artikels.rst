Hauptkategorie eines Artikels
=============================
Ein Artikel kann beliebig vielen Kategorien zugeordnet werden. In diesem Fall muss eine Kategorie als Hauptkategorie festgelegt werden. Das ist notwendig, damit der Shop in bestimmten Situationen entscheiden kann, in welcher Kategorie der Artikel angezeigt werden soll. Ruft der Kunde beispielsweise einen Artikel über die shopeigene Suche oder über die Tags auf, wird dieser in der definierten Hauptkategorie angezeigt.

Es spielt auch der sogenannte Duplicate Content eine Rolle. Ein Artikel, der in mehreren Kategorien vorkommt, hat mehrere URLs. Diese zeigen auf dessen Detailseite und würden so identischen Inhalt präsentieren. Suchmaschinen wie Google, Bing und Yahoo! wollen ihren Nutzern Suchergebnisse ohne Redundanzen auflisten. Die Lösung sind Canonical Tags oder Canonical Links, die bei inhaltlich gleichen Seiten auf die originale Seite verweisen. Im OXID eShop ist das die Detailseite des Artikels mit der Hauptkategorie in der URL.

Die Canonical Tags werden im OXID eShop prinzipiell, also auch für nur eine Kategorie, gesetzt. Wurde keine Hauptkategorie festgelegt, wird die Kategorie verwendet, welcher der Artikel als Erstes zugeordnet wurde.

Beispiel aus dem Seitenquelltext eines Artikels in einem Demoshop:

``\<link rel=\"canonical\"href=\"http://demoshop.oxid-esales.com/pe/Kiteboarding/Trapeze/Trapez-ION-MADTRIXX.html\"\>``

Die Hauptkategorie eines Artikels wird festgelegt.

* Gehen Sie zu :menuselection:`Artikel verwalten --> Artikel`.
* Wählen Sie den gewünschten Artikel aus der Artikelliste.
* Betätigen Sie die Schaltfläche :guilabel:`Kategorien zuordnen` auf der Registerkarte :guilabel:`Erweitert`.
* Legen Sie eine Hauptkategorie fest, wenn der Artikel in mehreren Kategorien vorkommt.
* Markieren Sie dafür die vorgesehene Kategorie in der rechten Liste.
* Betätigen Sie die Schaltfläche :guilabel:`Als Hauptkat. setzen`.
* Schließen Sie das Zuordnungsfenster.

.. image:: ../../media/screenshots-de/oxbalu01.png
   :alt: Als Hauptkategorie setzen
   :class: with-shadow
   :height: 314
   :width: 400

.. seealso:: :doc:`Artikel - Registerkarte Erweitert <../artikel/registerkarte-erweitert>` | `Canonical Link <http://de.wikipedia.org/wiki/Canonical_Link>`_ (Wikipedia)

.. Intern: oxbalu, Status: