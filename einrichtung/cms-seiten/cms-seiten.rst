CMS-Seiten
==========

Verwalten Sie die Textinhalte Ihres Shops zentral über die CMS-Seiten im Administrationsbereich. CMS steht für Content-Management-System und ermöglicht Ihnen, Inhalte ohne Programmierkenntnisse im Frontend des OXID eShop anzuzeigen.

Nutzen Sie CMS-Seiten für vollständige Informationsseiten wie `Impressum`, `AGB` oder Hinweise zu `Zahlung und Versand`. Darüber hinaus lassen sich CMS-Seiten auch in spezifischen Bereichen des Shops integrieren – etwa im Footer oder in automatisch versendeten E-Mails.

Im unteren Bereich des Shops (Footer) erscheint beispielsweise der über eine CMS-Seite definierte Slogan (:ref:`oxbaji02`, Pos. 1):

.. _oxbaji02:

.. figure:: ../../media/screenshots/oxbaji02.png
   :alt: Footer im Frontend
   :width: 650
   :class: with-shadow

   Abb.: Footer im Frontend

|procedure|

1. Öffnen Sie den Administrationsbereich.
2. Wählen Sie :menuselection:`Kundeninformationen --> CMS-Seiten`.

   Die Liste zeigt alle CMS-Seiten mit ihrem :guilabel:`Titel` und ihrer :guilabel:`Ident`. Ein grünes Häkchen markiert aktive Seiten.

   * Suchen Sie gezielt nach CMS-Seiten über die verfügbaren Suchfelder.
   * Filtern Sie die Liste nach Ordnern (z. B. :guilabel:`E-Mails`, :guilabel:`Kundeninformationen`, :guilabel:`Artikelinformationen`).
   * Wählen Sie :guilabel:`Kein`, um spezielle CMS-Seiten anzuzeigen, die keinem Ordner zugeordnet sind.

3. Bearbeiten Sie eine vorhandene Seite (:ref:`oxbaji01`) oder klicken Sie auf :guilabel:`Neue CMS-Seite anlegen`, um eine neue Seite zu erstellen.

   .. _oxbaji01:

   .. figure:: ../../media/screenshots/oxbaji01.png
      :alt: CMS-Seite bearbeiten
      :width: 650
      :class: with-shadow

      Abb.: CMS-Seite bearbeiten

#. Speichern Sie Ihre Einstellungen.

|background|

Die verfügbaren Ordner definieren Sie unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Administrationsbereich`.

Beispiel: Der Eintrag ``CMSFOLDER_EMAILS => #706090`` erzeugt den Ordner :guilabel:`E-Mails` mit der Schriftfarbe Dunkelviolett. Die eigentlichen Ordnernamen sind sprachabhängig und stammen aus den Sprachdateien des Adminbereichs.

|result|

Nach dem Speichern stehen die CMS-Inhalte im Shop oder in System-E-Mails zur Verfügung – abhängig vom Einsatzzweck der jeweiligen Seite (in unserem Beispiel der Footer: :ref:`oxbaji02`, Pos. 1).

Um eine CMS-Seite endgültig zu löschen, klicken Sie auf das Papierkorb-Symbol am Ende der jeweiligen Zeile.

-----------------------------------------------------------------------------------------

Registerkarte Stamm
-------------------
**Inhalte**: aktive CMS-Seite, Titel, Ident, Ordner für CMS-Seiten, Snippet, Hauptmenü, Kategorie, Link in Kategorienavigation, manuell, inkludierte CMS-Seite, Inhalt der CMS-Seite, Editor, WYSIWYG, HTML-Code |br|
:doc:`Artikel lesen <registerkarte-stamm>` |link|

Registerkarte SEO
------------------
**Inhalte**: Suchmaschinenoptimierung, SEO, URL fixieren, oxseohistory, Weiterleitung, 301, SEO URL, Metadaten, Meta-Tags, meta name=”description”, meta name=”keywords”  |br|
:doc:`Artikel lesen <registerkarte-seo>` |link|


.. Intern: oxbaji, Status: