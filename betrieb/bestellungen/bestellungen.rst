Bestellungen verwalten
======================

Schließt ein Kunde seinen Einkauf im OXID eShop ab, wird automatisch eine Bestellung erzeugt.

Der Kunde erhält eine **Bestellbestätigung per E-Mail**, die folgende Informationen enthält:

* Liste der bestellten Artikel
* Einzel- und Gesamtpreise
* Rechnungs- und Lieferadresse
* Zahlungs- und Versandart
* Bestellnummer

Gleichzeitig wird der Shopbetreiber per E-Mail über den Auftrag informiert.

.. figure:: ../../media/screenshots/oxbaeb01.png
   :alt: Bestellungen bearbeiten
   :width: 650
   :class: with-shadow

   Abb.: Bestellungen bearbeiten


Bestellungen suchen und filtern
-------------------------------

* Nutzen Sie die Filter oberhalb der Liste zur gezielten Auswahl von Bestellungen:

  * Auswahl eines **Ordners** („Neu“, „Bearbeitet“, „Probleme“)
  * Einschränkung nach **Datum** im Format `JJJJ-MM-TT` (Teilformate wie `JJJJ-MM` sind möglich)
  * Anzeige **bezahlter Bestellungen** per Dropdown und Bezahldatum
  * Suche nach **Artikeln** (Titel, Artikelnummer)
  * Suche nach **Käufern** (Bestellnummer, Vorname, Nachname)

* Sortierung der Liste möglich nach:

  * Bestellzeit
  * Bezahlstatus
  * Bestellnummer
  * Käufername

Bestellungen bearbeiten
-----------------------

|procedure|

1. Öffnen Sie den Menüpunkt :menuselection:`Bestellungen verwalten --> Bestellungen`.
2. Wählen Sie eine Bestellung aus der Liste aus.

   Die Daten werden in den Eingabebereich geladen.

3. Bearbeiten Sie die gewünschten Informationen.
4. Optional: Um individuelle Absprachen mit dem Kunden zu einer Bestellung zu dokumentieren, wählen Sie in der Fußzeile des Eingabebereichs den Link :guilabel:`Notiz anfügen`.

   Weitere Informationen finden Sie unter :ref:`betrieb/bestellungen/registerkarte-historie:Registerkarte Historie`.

|result|

* Die Änderungen gelten sofort und sind im jeweiligen Register sichtbar.
* Dokumentieren Sie Zahlungseingang und Versandstatus im jeweiligen Register.

Bestellungen stornieren oder löschen
------------------------------------

* Klicken Sie auf das Symbol am Ende der Zeile in der Bestellliste:

  * **Löschen**: entfernt die Bestellung dauerhaft aus der Datenbank.
  * **Stornieren**: kennzeichnet die Bestellung als storniert.

.. warning::

   Eine Stornierung kann **nicht rückgängig gemacht** werden.
   Ein **Löschen** entfernt die Bestellung **endgültig**.



-----------------------------------------------------------------------------------------

Registerkarten im Überblick
---------------------------

Registerkarte Übersicht
^^^^^^^^^^^^^^^^^^^^^^^
**Inhalte**: Bestellübersicht, Rechnungsadresse, Lieferadresse, bestellte Artikel, Gesamtpreis mit einzelnen Positionen, Zahlungsart, Versandart, Mitteilung zur Bestellung, Bestellnummer, Kundennummer, Ordner für Bestellungen, Neu, Bearbeitet, Probleme, Bestellungen des aktuellen Tages, Bestellungen total, Bestellung versenden, Versandbestätigung |br|
:doc:`Artikel lesen <registerkarte-uebersicht>` |link|

Registerkarte Stamm
^^^^^^^^^^^^^^^^^^^
**Inhalte**: IP-Adresse und Bestellung, Trusted Shops, Bestellnummer, Rechnungsnummer, Rabatt, Bezahlinformationen, Bezahldatum, Zahlungsart, Versandinformationen, Versandart, Versandkosten, Bestellung versenden, Versandbestätigung, Links zu Download-Artikeln |br|
:doc:`Artikel lesen <registerkarte-stamm>` |link|

Registerkarte Adressen
^^^^^^^^^^^^^^^^^^^^^^
**Inhalte**: Rechnungsadresse, Lieferadresse, Benutzer, Konto, Rechnungs- und Liefereinstellungen |br|
:doc:`Artikel lesen <registerkarte-adressen>` |link|

Registerkarte Artikel
^^^^^^^^^^^^^^^^^^^^^
**Inhalte**: Artikel einer Bestellung, Anzahl der Artikel ändern, bestellte Artikel stornieren, Artikel aus Bestellung löschen, Artikel suchen, Artikel zur Bestellung hinzufügen, Gesamtpreis mit einzelnen Positionen |br|
:doc:`Artikel lesen <registerkarte-artikel>` |link|

Registerkarte Historie
^^^^^^^^^^^^^^^^^^^^^^
**Inhalte**: Notiz, Protokoll, Kundenaktionen, Kundeninformationen |br|
:doc:`Artikel lesen <registerkarte-historie>` |link|

Registerkarte Downloads
^^^^^^^^^^^^^^^^^^^^^^^
**Inhalte**: Download-Artikel einer Bestellung, herunterladbare Dateien, erster und letzter Download, Anzahl erfolgter Downloads, maximal mögliche Downloads, Gültigkeit der Download-Links, Reset, Downloads zurücksetzen |br|
:doc:`Artikel lesen <registerkarte-downloads>` |link|


.. Intern: oxbaeb, Status: