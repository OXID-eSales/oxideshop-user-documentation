Versandkosten nach Kategorien differenzieren
============================================

.. todo: #SB: prüfen

In einem Online-Shop gibt es in der Regel einen Warenkatalog aus ganz verschiedenen Artikeln.

Richten Sie beispielsweise den Versand so ein, dass Artikel aus bestimmten Kategorien besonders günstig verschickt werden.

Werden zusätzlich Artikel aus anderen Kategorien in den Warenkorb gelegt, fallen höhere Versandkosten an. Dafür werden Versandkostenregeln verwendet, die abhängig von Kategorien funktionieren.

Im Bestellprozess wählt der Kunde eine Versandart. Alle zur Versandart gehörenden Versandkostenregeln werden abgearbeitet. Es wird geprüft, ob die festgelegte Bedingung (zugewiesene Kategorien) hinsichtlich der Artikel im Warenkorb erfüllt ist.

Nur wenn eine Bedingung zutrifft, wird die Versandkostenregel bei der Berechnung der Versandkosten angewandt.

Vorgehen
--------

1. Definieren Sie Kategorien als Bedingung

   a. Gehen Sie zu :menuselection:`Shopeinstellungen --> Versandkostenregeln`.
   #. Wählen Sie die Versandkostenregel aus der Liste der Versandkostenregeln.
   #. Betätigen Sie auf der Registerkarte :guilabel:`Artikel` die Schaltfläche :guilabel:`Kategorien zuordnen`.
   #. Verschieben Sie die Kategorien per Drag \& Drop in die rechte Liste des Zuordnungsfensters.
   #. Schließen Sie das Zuordnungsfenster.
   #. Tragen Sie einen Preis auf der Registerkarte :guilabel:`Stamm` ein.
   #. Komplettieren Sie alle weiteren Einstellungen der Versandkostenregel.
   #. Speichern Sie die Änderungen.

#. Ordnen Sie eine Versandkostenregel einer Versandart zu.

   .. hint:: Der Versandart müssen mindestens eine Versandkostenregel und eine Zahlungsart zugeordnet worden sein.

      Länder sollten zugewiesen sein, damit die Definition von Versand und Zahlung stringent ist. Ohne Länderzuordnung gilt die Versandart für alle Länder.

   a. Gehen Sie zu :menuselection:`Shopeinstellungen --> Versandarten`.
   #. Wählen Sie die Versandart aus der Liste der Versandarten.
   #. Betätigen Sie auf der Registerkarte :guilabel:`Stamm` die Schaltfläche :guilabel:`Versandkostenregeln zuordnen`.
   #. Verschieben Sie die Versandkostenregel per Drag \& Drop in die rechte Liste des Zuordnungsfensters.
   #. Schließen Sie das Zuordnungsfenster.

Beispiel: Kategorien und Versandkostenregeln im Demo-Shop
---------------------------------------------------------

In unseren Demoshop-Daten sind Kategorien beispielsweise wie folgt den Versandkostenregeln zugeordnet und priorisiert (:ref:`oxbafz01`, Pos. 2):

======================== ================================================= ====================
Kategorie                Versandregel                                      Priorität
======================== ================================================= ====================
Fahrzeuge                Versandregel Zustellung PKW                       0
Achsen, Achteile,        Versandregel Spedition                            5
Karosserie, Räder
Alle übrigen Kategorien  Versandregeln Standard und Express                10
======================== ================================================= ====================


Durch das Aktivieren der Einstellung :guilabel:`Keine weiteren Regeln nach dieser berechnen` (:ref:`oxbafz01`, Pos. 3) ist sichergestellt, dass ein Kunde jeweils nur die höchste Versandkosten bezahlt.

.. _oxbafz01:

.. figure:: ../../media/screenshots/oxbafz01.png
   :alt: Beispiel: Versandkostenregel für Kategorie Fahrzeuge
   :width: 650
   :class: with-shadow

   Abb.: Beispiel: Versandkostenregel für Kategorie Fahrzeuge

Dies würde in unserem einfachen Beispiel den Fall abdecken, dass Sie Fahrzeuge verkaufen, die dann bei der Überführung beispielsweise auch einen Satz Winterräder sowie Merchandise-Waren transportieren könnten.

Wenn die Artikel dagegen getrennt transportiert werden, dann deaktivieren Sie die Einstellung :guilabel:`Keine weiteren Regeln nach dieser berechnen`. In diesem Fall werden beide Versandkostenregeln angewendet, und die Versandkosten werden addiert.

In unserem Beispiel wird entsprechend die Überführung für jede Überführung separat abgerechnet (:ref:`oxbafz01`, Pos.1), die Kosten für die Spedition oder den Paketversand dagegen werden einmalig pro Warenkorb berechnet.

.. seealso:: :doc:`Versandkostenregeln - Registerkarte Artikel <../versandkostenregeln/registerkarte-artikel>` | :doc:`Versandarten - Registerkarte Stamm <../versandarten/registerkarte-stamm>`

.. Intern: oxbafz, Status: