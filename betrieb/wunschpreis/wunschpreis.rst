Wunschpreis
===========

Kunden können für Artikel aus dem Shop einen Preis angeben, zu dem sie diesen gern kaufen würden. Der Shopbetreiber kann die Kunden per E-Mail informieren, sobald dieser Wunschpreis erreicht oder unterschritten wurde. Die Funktion wird in den Einstellungen des Themes in der Sektion :guilabel:`Funktionen` für den Shop global aktiviert oder deaktiviert. Sie lässt sich aber auch auf einzelne Artikel anwenden. Aktivieren Sie das Kontrollkästchen :guilabel:`Wunschpreis deaktivieren` auf der Registerkarte :guilabel:`Erweitert` eines Artikels, um die Funktion für den jeweiligen Artikel abzuschalten. Wunschpreis hieß bis OXID eShop 6.2.1 Preisalarm.

.. image:: ../../media/screenshots/oxbajm01.png
   :alt: Detailansicht Artikel, Wunschpreis
   :height: 390
   :width: 650

Ist die Funktion Wunschpreis aktiv, wird in der Detailansicht des Artikels die Registerkarte :guilabel:`[!] Wunschpreis` angezeigt, welche ein kleines Formular enthält. Hier kann der Kunde den Wunschpreis und seine E-Mail-Adresse eintragen. Nach dem Abschicken der Informationen erhält er eine Bestätigung, dass er benachrichtigt wird, sobald der Wunschpreis erreicht ist. Der Shopbetreiber wird per E-Mail darüber informiert, dass der Kunde sich einen Artikel zu einem bestimmten Preis wünscht. Die Vorlage zur E-Mail ist die CMS-Seite "Wunschpreis" (Ident: oxpricealarmemail).

.. image:: ../../media/screenshots/oxbajm02.png
   :alt: Wunschpreis
   :height: 522
   :width: 650

Die von den Kunden angefragten Wunschpreise werden im Administrationsbereich unter :menuselection:`Kundeninformationen --> Wunschpreis` gesammelt. Dort werden alle Eingänge für einen Wunschpreis aufgelistet.

Die Liste mit den Wunschpreis-Eingängen zeigt jeweils die E-Mail-Adresse, den Namen des Kunden, das Datum des Eingangs, das Datum der E-Mail-Benachrichtigung, den Namen des Artikels, seinen regulären Preis und den Wunschpreis des Kunden. Nach Wunschpreis-Eingängen kann gesucht werden, indem die Suchfelder oberhalb der Liste verwendet werden.

Die Wunschpreis-Eingänge können in der Liste sortiert werden, indem die jeweilige Spaltenüberschrift angeklickt wird. Sie werden dadurch in aufsteigender Reihenfolge angezeigt. Wunschpreis-Eingänge lassen sich durch einen Klick auf das Löschsymbol am Ende der Zeile endgültig aus der Datenbank entfernen.

Wird ein Eintrag aus der Liste ausgewählt, werden die Details in den Eingabebereich geladen. Auf der Registerkarte  :guilabel:`Stamm` kann der Text der E-Mail bearbeitet werden, die den Kunden über den Wunschpreis informieren soll. Die Registerkarte :guilabel:`E-Mail` ermöglicht es, die E-Mails an die Kunden zu verschicken.

-----------------------------------------------------------------------------------------

Registerkarte Stamm
-------------------
**Inhalte**: E-Mail-Adresse, Name des Kunden, Sprache, Datum des Eingangs, Datum der Benachrichtigung, Artikel, Wunschpreis, regulärer Preis, Text der E-Mail, Preisalarm bis OXID eShop 6.2.1 |br|
:doc:`Artikel lesen <registerkarte-stamm>` |link|

Registerkarte E-Mail
--------------------
**Inhalte**: Wunschpreis erreicht, Benachrichtigungsmail(s) versenden
Artikel lesen |br| :doc:`Artikel lesen <registerkarte-e-mail>` |link|

.. seealso:: :doc:`Artikel, Registerkarte Erweitert <../../einrichtung/artikel/registerkarte-erweitert>`


.. Intern: oxbajm, Status: Latitute-images