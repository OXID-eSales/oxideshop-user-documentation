:orphan:
Geschenkverpackung
==================

.. todo: #SB: bei Bedarf den im Folgenden skizzierten Anwendungsfall klären und beschreiben
.. todo: redirect handler anpassen:
# Stammdaten -> Sprachen
- input: admin/language_main.html # OK (but to be adjusted later when konfiguration/sprachen has been created)
output:

(but to be adjusted later when konfiguration/rdfa has been created)

|procedure|

Um Ihren Kunden Geschenkverpackungen anzubieten, tun Sie Folgendes:

1. Wählen Sie :menuselection:`Schopeinstellungen --> Geschenkverpackung`.

Mit dieser Konfigurationsmaske können Sie eine Geschenkverpackung als Zusatzoption im OXID eShop anlegen und verwalten. Die wichtigsten Felder und Optionen sind:

+-------------------+-------------------------------------------------------------+
| **Feld**          | **Beschreibung**                                            |
+===================+=============================================================+
| Aktiv             | Aktiviert die Geschenkverpackung für den Shop.              |
+-------------------+-------------------------------------------------------------+
| Typ               | Art der Zusatzoption, hier: Geschenkverpackung.             |
+-------------------+-------------------------------------------------------------+
| Name              | Interner Name, z.B. „Geschenkverpackung“.                                 |
+-------------------+-------------------------------------------------------------+
| Preis (€)         | Preis der Geschenkverpackung in Euro.                       |
+-------------------+-------------------------------------------------------------+
| Bild              | Optionales Bild der Geschenkverpackung.                     |
|                   | (Max. 2 MB, max. 1500x1500 px, Upload möglich)              |
+-------------------+-------------------------------------------------------------+

**Hinweise zur Konfiguration:**

- Die Option „Aktiv“ steuert, ob die Geschenkverpackung im Bestellprozess auswählbar ist.
- Der Typ „Geschenkverpackung“ sorgt dafür, dass diese Zusatzleistung im Warenkorb und an der Kasse als Option erscheint.
- Der Name „Geschenkverpackung“ dient der internen Zuordnung und kann im Frontend übersetzt werden.
- Der Preis wird dem Kunden zusätzlich zum Warenwert berechnet.
- Ein Bild kann hochgeladen werden, um die Geschenkverpackung im Shop visuell darzustellen. Die Bilddatei darf maximal 2 MB groß sein und die Abmessungen von 1500x1500 Pixeln nicht überschreiten.

**Empfehlung:**
Laden Sie ein ansprechendes Bild hoch, um die Geschenkverpackung für Ihre Kunden attraktiver zu machen. Prüfen Sie nach dem Speichern, ob die Option im Warenkorb korrekt angezeigt wird.

**Tipp:**
Weitere Geschenkoptionen (z.B. verschiedene Verpackungsarten) können Sie auf die gleiche Weise anlegen und individuell bepreisen.

