Mehrwertsteuer
==============

Legen Sie die globalen Grundeinstellungen für die Berechnung und Anzeige der Mehrwertsteuer in Ihrem Shop fest.

Bei Bedarf können Sie im nächsten Schritt spezielle Mehrwertsteuer-Sätze für Artikel-Kategorien oder einzelne Artikel und Varianten festlegen.


Globale MwSt.-Einstellungen vornehmen
-------------------------------------

Nehmen Sie grundlegende Einstellungen zur Mehrwertsteuer vor.

Die Standardeinstellungen nach der Installation sind für die meisten Shops geeignet, so dass hier in der Regel keine Änderungen notwendig sind.

Alle aufgelisteten Optionen sind standardmäßig nicht aktiv, und für die Mehrwertsteuer gilt 19 Prozent als Standard.


|procedure|

Prüfen Sie im Administrationsbereich unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Mehrwertsteuer`, welche der folgenden Optionen für Sie infrage kommt:

:guilabel:`Standard-MwSt.-Satz für alle Artikel`
   Die Zahl 19 im Eingabefeld steht dafür, dass für alle Artikel in Ihrem Shop standardmäßig eine Mehrwertsteuer von 19 Prozent gilt.
   |br|
   Optional: Definieren Sie bei Bedarf für einzelne Artikel einen vom Standard-MwSt.-Satz abweichenden Mehrwertsteuersatz definieren, beispielsweise 7 Prozent für Lebensmittel.

:guilabel:`Artikelpreise netto eingeben (zuzüglich MwSt.)`
   Optional: Geben Sie bei allen Artikeln den Artikelpreis als Nettopreis ein.
   |br|
   Für jeden Artikel im Shop muss dann die Mehrwertsteuer berechnet werden, bevor der Artikel mit seinem Bruttopreis angezeigt werden kann.
   |br|
   Es gibt eine Einstellung, die dafür sorgt, dass die Mehrwertsteuer ausschließlich im Warenkorb und Bestellprozess angezeigt wird.
   |br|
   Der Shop würde also Artikel mit Nettopreisen anzeigen und erst, wenn ein Artikel in den Warenkorb gelegt wird, würde die Mehrwertsteuer berechnet und angezeigt.
   |br|
   Die Einstellung :guilabel:`MwSt. nur im Warenkorb und Bestellprozess berechnen` findet sich unter :menuselection:`Stammdaten --> Grundeinstellungen --> Perform.`

:guilabel:`Nettopreise im Shop anzeigen (B2B)`
   Optional: Betreiben Sie Ihren Shop als Shop für Geschäftskunden.

:guilabel:`Berechnung der MwSt. für Nebenleistungen`
   Optional: Legen Sie fest, wie Sie die Mehrwertsteuer für Versandkosten, Gebühren oder Verpackung berechnen wollen.

.. todo: #tbd 7.x: add details
   |br|
   :guilabel:`MwSt. ausgehend vom größten Nettowert berechnen`:
   |br|
   :guilabel:`MwSt. anteilig berechnen`:

**Optional**: Legen Sie fest, ob die Nebenleistungen (Versand, Zahlungsgebühren oder Verpackung) als Nettopreise einzugeben sind.

**Optional**: Legen Sie fest, wie Beträge für Nebenleistungen im Warenkorb und in der Rechnung angezeigt werden sollen.

Standardmäßig wird der Bruttobetrag angezeigt. Sie können aber auch jeweils den Nettobetrag plus Mehrwertsteuer anzeigen.

:guilabel:`Die Lieferadresse anstatt der Rechnungsadresse für die Mehrwertsteuerberechnung verwenden`
   Die Standardeinstellung nach der Installation ist, dass die Mehrwertsteuer auf Basis der Rechnungsadresse berechnet wird.
   |br|
   Die Adresse des Rechnungsempfängers entscheidet darüber, ob Mehrwertsteuer berechnet wird oder nicht.
   |br|
   Optional: Legen Sie die Lieferadresse als Basis für die Berechnung der Mehrwertsteuer fest.

.. todo: #tbd 7.x: guilabels
   :guilabel:`Online UST-ID Prüfung deaktivieren`
   :guilabel:`Alternative URL für die Online UST-ID Prüfung`


Spezielle MwSt.-Einstellungen vornehmen
---------------------------------------

Legen Sie die Mehrwertsteuer-Sätze fest, die abweichend von den global gültigen MwSt.-Sätzen für bestimmte Kategorien oder einzelne Artikel gelten sollen.


|prerequisites|

* Sie haben unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Mehrwertsteuer --> Standard-MwSt.-Satz für alle Artikel` den global gültigen Standard-MwSt.-Satz festgelegt (siehe :ref:`konfiguration/mehrwertsteuer:Globale MwSt.-Einstellungen vornehmen`).

|procedure|

Legen Sie spezielle Mehrwertsteuer-Sätze wie folgt fest:

* Für eine Kategorie: Wählen Sie :menuselection:`Artikel verwalten --> Kategorien --> [gewünschte Kategorie] --> Stamm --> Spez. MwSt.`
* Für einen Artikel: Wählen Sie :menuselection:`Artikel verwalten > Artikel --> [gewünschter Artikel] --> Stamm --> Spez. MwSt.`
* Variante eines Artikels: Wählen Sie :menuselection:`Artikel verwa--lten --> Artikel --> [gewünschter Artikel] --> Variante --> Variante editieren --> Spez. MwSt.`

.. hint::

   **Kategorien mit unterschiedlichen Mehrwertsteuersätzen**

   Es kann vorkommen, dass derselbe Artikel Kategorien mit unterschiedlichen Mehrwertsteuersätzen zugeordnet ist.

   In diesem Fall berechnet der OXID eShop die Mehrwertsteuer nach dem Mehrwertsteuersatz der übergeordneten Kategorie oder nach derjenigen Kategorie, der Sie den Artikel zuerst zugeordnet haben.


.. Intern: oxbaay, Status: