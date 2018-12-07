Versandkosten für Artikel aus bestimmten Kategorien
===================================================

In einem Online-Shop gibt es in der Regel einen Warenkatalog aus ganz verschiedenen Artikeln. Der Versand kann so eingerichtet werden, dass Artikel aus bestimmten Kategorien günstig verschickt werden. Werden zusätzlich Artikel aus anderen Kategorien in den Warenkorb gelegt, fallen höhere Versandkosten an. Dafür werden Versandkostenregeln verwendet, die abhängig von Kategorien funktionieren.

Im Bestellprozess wählt der Kunde eine Versandart. Alle zur Versandart gehörenden Versandkostenregeln werden abgearbeitet. Es wird geprüft, ob die festgelegte Bedingung (zugewiesene Kategorien) hinsichtlich der Artikel im Warenkorb erfüllt ist. Nur wenn eine Bedingung zutrifft, wird die Versandkostenregel bei der Berechnung der Versandkosten angewandt.

In den Versandkostenregeln werden Kategorien als Bedingung definiert.

* Gehen Sie zu :menuselection:`Shopeinstellungen --> Versandkostenregeln`.
* Wählen Sie die Versandkostenregel aus der Liste der Versandkostenregeln.
* Betätigen Sie die Schaltfläche :guilabel:`Kategorien zuordnen` auf der Registerkarte :guilabel:`Artikel`.
* Verschieben Sie die Kategorien per Drag \& Drop in die rechte Liste des Zuordnungsfensters.
* Schließen Sie das Zuordnungsfenster.
* Tragen Sie einen Preis auf der Registerkarte :guilabel:`Stamm` ein.
* Komplettieren Sie alle weiteren Einstellungen der Versandkostenregel.
* Speichern Sie die Änderungen.

Die Versandkostenregel wird einer Versandart zugeordnet.

* Gehen Sie zu :menuselection:`Shopeinstellungen --> Versandarten`.
* Wählen Sie die Versandart aus der Liste der Versandarten.
* Betätigen Sie die Schaltfläche :guilabel:`Versandkostenregeln zuordnen` auf der Registerkarte :guilabel:`Stamm`.
* Verschieben Sie die Versandkostenregel per Drag \& Drop in die rechte Liste des Zuordnungsfensters.
* Schließen Sie das Zuordnungsfenster.

.. hint:: Der Versandart müssen mindestens eine Versandkostenregel und eine Zahlungsart zugeordnet worden sein. Länder sollten zugewiesen sein, damit die Definition von Versand und Zahlung stringent ist. Ohne Länderzuordnung gilt die Versandart für alle Länder.

Beispiel
--------
Das Beispiel zeigt, wie Artikel einer bestimmten Kategorie zu günstigeren Versandkosten als alle anderen Artikel verschickt werden können. Dafür werden zwei Versandkostenregeln verwendet, deren Bedingung die Menge ist. Ein Mengenbereich von 1 bis 99999999 stellt sicher, dass diese Bedingung immer zutrifft. Die Berechnung erfolgt einmal pro Warenkorb. Länder können, aber müssen nicht zugewiesen sein. Die Versandkostenregel muss aktiv sein.

Die erste Versandkostenregel wird mit einem Preis von 4,99 € angelegt. Für alle Artikel außer denen der Kategorie \"Zubehör\" gibt es eine zweite Versandkostenregel mit einem Preisaufschlag von 2,50 €.

.. image:: ../../media/screenshots/oxbafz01.png
   :alt: Versandkosten DHL - Standardartikel: +2,50 Euro
   :class: with-shadow
   :height: 342
   :width: 650

Der im Screenshot gezeigten Versandkostenregel wurden alle Kategorien mit Ausnahme der Kategorie \"Zubehör\ "zugeordnet. Beide Versandkostenregeln gehören zur Versandart \"DHL GoGreen\". Wird diese Versandart beim Kauf ausgewählt, werden beide Versandkostenregeln geprüft.

Liegt ein Artikel aus dem Kiteboarding-Zubehör im Warenkorb, greift die erste Versandkostenregel. Der Versand kostet 4,99 €.

.. image:: ../../media/screenshots/oxbafz02.png
   :alt: Warenkorb mit Kite-Leinen
   :class: with-shadow
   :height: 261
   :width: 550

Wird zusätzlich ein Trapez in den Warenkorb gelegt, ist auch die zweite Versandkostenregel gültig. Die Versandkosten summieren sich auf 7,49 €.

.. image:: ../../media/screenshots/oxbafz03.png
   :alt: Warenkorb mit Kite-Leinen und Trapez
   :class: with-shadow
   :height: 310
   :width: 550

7,49 € kostet auch der Versand eines einzelnen Trapezes, da beide Versandkostenregeln zutreffen. Die erste Versandkostenregel gilt für alle Artikel und die zweite Versandkostenregel schließt nur die Artikel aus dem Kiteboarding-Zubehör aus.

.. seealso:: :doc:`Versandkostenregeln - Registerkarte Artikel <../versandkostenregeln/registerkarte-artikel>` | :doc:`Versandarten - Registerkarte Stamm <../versandarten/registerkarte-stamm>`

.. Intern: oxbafz, Status: