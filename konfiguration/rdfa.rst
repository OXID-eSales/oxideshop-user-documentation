:orphan:
RDFa
====

.. todo: #SB: klären, in wieweit der RDFa-Tab noch aktuell ist und bei Bedarf die im Folgenden skizzierten Anwendungsfälle klären und beschreiben
.. todo: redirect handler anpassen:
    - admin/shop_rdfa.html # OK (but to be adjusted later when konfiguration/rdfa has been created)
    output: konfiguration/konfiguration.html -> konfiguration/rdfa

|procedure|

Um die RDFa-Einstellungen vorzunehmen, tun Sie Folgendes:

1. Wählen Sie :menuselection:`Stammdaten --> Grundeinstellungen`.
#. Wählen Sie die Registerkarte :guilabel:`RDFa`.

Globale Einstellungen im OXID eShop
-----------------------------------

Datenintegration und RDFa
^^^^^^^^^^^^^^^^^^^^^^^^^

* **Automatische Einbettung der Daten aktivieren:**
  Aktivieren Sie diese Option, um strukturierte Daten (z.B. für Suchmaschinen) automatisch in die Shopseiten einzubetten.

* **RDF-Daten für AGB und Zahlungsarten:**
  - *In welche Content-Seite sollen die RDF-Daten des eShop eingebettet werden?*
    Geben Sie die CMS-Seite an (z.B. „AGB“), in die die RDF-Daten des Shops integriert werden sollen.
  - *Zahlungsarten den RDFa-Zahlungsarten zuweisen:*
    Navigieren Sie zu **Shopeinstellungen → Zahlungsarten → RDFa**, um die Zuordnung vorzunehmen.
  - *Nicht zugewiesene Zahlungsarten:*
    Definieren Sie eine Content-Seite (z.B. „AGB“), in die RDF-Daten von Zahlungsarten eingebettet werden, die keiner spezifischen Seite zugeordnet sind.
  - *Versandarten den RDFa-Versandarten zuweisen:*
    Gehen Sie zu **Shopeinstellungen → Versandarten → RDFa**.
  - *Nicht zugewiesene Versandarten:*
    Geben Sie eine Content-Seite an, in die RDF-Daten von nicht zugewiesenen Versandarten eingebettet werden.

Preis- und Kostenanzeige
^^^^^^^^^^^^^^^^^^^^^^^^

* **Preisdarstellung:**
  Legen Sie fest, ob die angezeigten Preise und Kosten für Kunden *inklusive* oder *exklusive* der gesetzlichen Mehrwertsteuer (MwSt.) angezeigt werden.

* **Gültigkeitszeitraum der Preise und Kosten:**
  Wählen Sie den Zeitraum, für den die angegebenen Preise und Kosten gültig sind (z.B. „gültig bis auf Widerruf“ oder ein konkretes Datum).

Shop-Informationen
------------------

Stammdaten
^^^^^^^^^^

+---------------------+--------------------------+
| **Feld**            | **Beispielwert**         |
+---------------------+--------------------------+
| Firmenname          | Your Company Name        |
| Straße, Nr.         | 2425 Maple Street        |
| PLZ, Ort            | 9041 Any City, CA        |
| Land                | United States            |
| Telefon             | 217-8918712              |
| Fax                 | 217-8918713              |
| URL                 | www.myoxideshop.com      |
+---------------------+--------------------------+

Erweiterte Shop-Daten
^^^^^^^^^^^^^^^^^^^^^

* **Logo-URL:**
  Geben Sie die URL Ihres Shop-Logos an.

* **Geoposition:**
  - Geografische Länge (Longitude)
  - Geografische Breite (Latitude)

* **Identifikationsnummern:**
  - GLN (Global Location Number)
  - NAICS (North American Industry Classification System)
  - ISIC (International Standard Industrial Classification)
  - D-U-N-S (Dun & Bradstreet-Nummer)

Spezielle Artikel-Informationen
-------------------------------

* **Lagerbestand anzeigen:**
  Aktivieren Sie die Anzeige des tatsächlichen Lagerbestands für Artikel.

* **Bewertungspunkte:**
  - Minimaler Bewertungswert (z.B. 1 Punkt)
  - Maximaler Bewertungswert (z.B. 5 Punkte)

* **Artikelzustand:**
  Wählen Sie den Zustand der angebotenen Artikel (z.B. „Neu“, „Gebraucht“ oder „Keine der vorhandenen“).

* **Funktion der Angebote:**
  Definieren Sie, welche Funktion Ihre Angebote erfüllen:
  - Endverbraucher
  - Wiederverkäufer
  - Unternehmen/Gewerbetreibende
  - Öffentliche Einrichtungen

* **Kundengruppen:**
  Geben Sie an, welche Kundengruppen mit Ihren Angeboten angesprochen werden.

* **Gültigkeitszeitraum der Artikel:**
  Wählen Sie den Zeitraum, für den die Artikel im Shop als gültig angezeigt werden.