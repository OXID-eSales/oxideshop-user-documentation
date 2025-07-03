:orphan:
Sprachen
========

.. todo: #SB: bei Bedarf die im Folgenden skizzierten Anwendungsfälle klären und beschreiben
.. todo: redirect handler anpassen:
    # Stammdaten -> Sprachen
    - input: admin/language_main.html # OK (but to be adjusted later when konfiguration/sprachen has been created)
    output: konfiguration/konfiguration.html

|procedure|

Um die Hersteller als Marken im Frontend anzuzeigen, tun Sie Folgendes:

1. Wählen Sie :menuselection:`Stammdaten --> Sprachen`.


Frontend-Sprache „Deutsch“ konfigurieren
----------------------------------------

Die folgenden Einstellungen betreffen die Konfiguration der deutschen Sprache im OXID eShop. Sie bestimmen, wie und wo die Sprache im Shop-Frontend zur Verfügung steht und wie sie technisch eingebunden wird.

+-------------------+-----------------------------+
| **Feld**          | **Wert / Bedeutung**        |
+===================+=============================+
| Im Frontend aktiv | Ja                          |
|                   | (Sprache ist für Kunden     |
|                   | sichtbar und auswählbar)    |
+-------------------+-----------------------------+
| Sprachkürzel      | de                          |
|                   | (ISO-Code für Deutsch)      |
+-------------------+-----------------------------+
| Name              | Deutsch                     |
|                   | (Angezeigter Name im Shop)  |
+-------------------+-----------------------------+
| Standardsprache   | Ja                          |
|                   | (Wird als Standard gesetzt, |
|                   | wenn keine andere Sprache   |
|                   | gewählt wurde)              |
+-------------------+-----------------------------+
| Basis URL         | [URL eintragen]             |
|                   | (Stamm-URL für diese        |
|                   | Sprache, z.B.               |
|                   | https://www.shop.de/)       |
+-------------------+-----------------------------+
| Basis SSL URL     | [SSL-URL eintragen]         |
|                   | (Stamm-URL für HTTPS, z.B.  |
|                   | https://www.shop.de/)       |
+-------------------+-----------------------------+
| Sprach-ID         | 0                           |
|                   | (Interne ID, Standard: 0)   |
+-------------------+-----------------------------+
| Sortierung        | 1                           |
|                   | (Reihenfolge in der         |
|                   | Sprachauswahl)              |
+-------------------+-----------------------------+

**Hinweise zur Konfiguration:**

- Die Option „Im Frontend aktiv“ sorgt dafür, dass die Sprache im Shop für Besucher sichtbar und auswählbar ist.
- Das Sprachkürzel „de“ entspricht dem internationalen Standard für Deutsch und wird für die URL-Struktur und Lokalisierung verwendet.
- Die Sprach-ID „0“ ist in OXID eShop üblicherweise für die Standardsprache reserviert.
- Die Sortierung legt fest, an welcher Position die Sprache in der Sprachauswahl erscheint (1 = ganz oben).
- Die Basis-URL und Basis-SSL-URL müssen korrekt eingetragen werden, damit der Shop die Sprache richtig zuordnet und Links generiert.

**Empfehlung:**
Prüfen Sie nach der Konfiguration, ob die Sprache im Frontend korrekt angezeigt wird und alle Inhalte wie gewünscht lokalisiert sind.



