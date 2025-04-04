Registerkarte SEO
=================

Optimieren Sie die Sichtbarkeit Ihrer CMS-Seiten in Suchmaschinen über die Registerkarte :guilabel:`SEO`. Hier definieren Sie gezielt URL-Strukturen sowie Meta-Informationen, die in den HTML-Quelltext übernommen werden.

.. figure:: ../../media/screenshots/oxbajk01.png
   :alt: CMS-Seiten – Registerkarte SEO
   :width: 650
   :class: with-shadow

   Abb.: CMS-Seiten – Registerkarte SEO

|procedure|

1. Öffnen Sie im Adminbereich die gewünschte CMS-Seite.
#. Wechseln Sie zur Registerkarte :guilabel:`SEO`.
#. Bearbeiten Sie bei Bedarf die folgenden Felder:

   :guilabel:`SEO URL`
      Passen Sie die automatisch generierte URL der CMS-Seite an. Ändern Sie diese nur, wenn Sie eine gezielte Struktur für Ihre Seiten-URLs benötigen.

   :guilabel:`URL fixiert`
      Verhindern Sie, dass sich die SEO-URL bei Änderungen am Seitentitel automatisch anpasst. Aktivieren Sie dieses Kontrollkästchen, um die bestehende URL beizubehalten. Änderungen werden sonst in der Tabelle :db:`oxseohistory` dokumentiert und mit einem 301-Redirect weitergeleitet.

   :guilabel:`Stichworte für Meta-Tags`
      Tragen Sie relevante Keywords ein, die im HTML-Quelltext als Meta-Tags erscheinen. Wenn Sie dieses Feld leer lassen, generiert der Shop automatisch Stichwörter auf Basis des Titels der CMS-Seite.

   :guilabel:`Beschreibungstext für Meta-Tags`
      Geben Sie hier eine prägnante Beschreibung der Seite ein. Diese erscheint in vielen Suchmaschinen in den Suchergebnissen. Ohne Eintrag generiert der Shop die Beschreibung automatisch.

#. Wählen Sie im Feld :guilabel:`In Sprache` die gewünschte Sprache, um die SEO-Einstellungen sprachspezifisch zu hinterlegen.
#. Speichern Sie Ihre Einstellungen.

|result|

Nach dem Speichern verwendet der Shop die eingegebenen SEO-Daten für die CMS-Seite – sowohl im HTML-Code als auch bei der Anzeige in Suchmaschinen.

.. seealso:: :doc:`SEO-Einstellungen <../../konfiguration/seo-einstellungen>` | :doc:`CMS-Seiten <cms-seiten>`

.. Intern: oxbajk, Status: