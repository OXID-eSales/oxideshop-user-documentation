Registerkarte Stamm
===================

Verwalten Sie in der Registerkarte :guilabel:`Stamm` die Grundeinstellungen und Inhalte einer CMS-Seite. Erstellen Sie neue CMS-Seiten oder bearbeiten Sie bestehende Inhalte komfortabel über das integrierte Editorfeld.

.. figure:: ../../media/screenshots/oxbajj01.png
   :alt: CMS-Seiten – Registerkarte Stamm
   :width: 650
   :class: with-shadow

   Abb.: CMS-Seiten – Registerkarte Stamm

|procedure|

1. Öffnen Sie im Adminbereich den Menüpunkt :menuselection:`Kundeninformationen --> CMS-Seiten`.
#. Wählen Sie eine CMS-Seite aus der Liste oder klicken Sie auf :guilabel:`Neue CMS-Seite anlegen`, um eine neue Seite zu erstellen.
#. Pflegen Sie die folgenden Einstellungen und Felder:

   :guilabel:`Aktiv`
      Aktivieren Sie dieses Kontrollkästchen, um die CMS-Seite im Shop oder in E-Mails anzuzeigen. Eine deaktivierte Seite bleibt gespeichert, wird aber nicht angezeigt.

   :guilabel:`Titel`
      Vergeben Sie einen eindeutigen und aussagekräftigen Titel. Der Titel erscheint bei Seiten im Frontend als Überschrift und dient als Suchkriterium im Adminbereich.

   :guilabel:`Ident.`
      Vergeben Sie eine eindeutige Kennung, um die Seite intern anzusprechen. Verwenden Sie einen sprechenden Wert anstelle des automatisch generierten alphanumerischen Codes.

   :guilabel:`Ordner`
      Ordnen Sie die CMS-Seite einem Ordner zu, um sie thematisch zu gruppieren. Standardordner sind z. B. „E-Mails“, „Kunden-Infos“, „Artikel-Information“. Neue Ordner definieren Sie unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstellungen --> Administrationsbereich`.

   :guilabel:`In Sprache`
      Wählen Sie eine aktive Sprache aus der Liste, um die Inhalte sprachspezifisch zu pflegen.

   :guilabel:`Snippet`
      Aktivieren Sie diese Option, um die CMS-Seite als Textbaustein (Snippet) in Templates oder E-Mails zu verwenden. Beispiel: ``[{ oxcontent ident="oxagb" }]``

   :guilabel:`Hauptmenü`
      Diese Option ist veraltet und wird in aktuellen Themes nicht mehr verwendet.

   :guilabel:`Kategorie`
      Aktivieren Sie diese Einstellung, um die CMS-Seite als Link in der Kategorienavigation anzuzeigen. Nach dem Speichern erscheint das Feld :guilabel:`Eingefügt vor`.

   :guilabel:`Eingefügt vor`
      Legen Sie hier fest, an welcher Position zwischen den Kategorien der CMS-Link angezeigt werden soll. Nur sichtbar, wenn :guilabel:`Kategorie` aktiviert ist.

   :guilabel:`Manuell`
      Ermöglicht das Einbinden der CMS-Seite in eine andere. Nach dem Speichern erscheint ein Link wie: ``[{ oxgetseourl ident="oxcredits" type="oxcontent" }]``.

   :guilabel:`Link`
      Zeigt den Einbindungscode der CMS-Seite an. Nur sichtbar, wenn :guilabel:`Manuell` aktiviert ist.

#. Pflegen Sie den Textinhalt der CMS-Seite im Editor auf der rechten Seite. Der Editor unterstützt WYSIWYG („What You See Is What You Get“) und zeigt den Text wie im Shop an.

   Verwenden Sie Formatierungen, fügen Sie Links, Bilder oder Videos ein, oder wechseln Sie in den HTML-Modus für erweiterte Anpassungen.

   Auch Smarty-Ausdrücke sind möglich – etwa in der CMS-Seite ``Ihr Passwort im eShop``, die im Rahmen des Passwort-Resets an Kunden gesendet wird.

#. Speichern Sie Ihre Einstellungen.

|result|

Nach dem Speichern stehen die CMS-Seiteninhalte im Frontend, in E-Mails oder in Templates zur Verfügung – abhängig von den gesetzten Optionen.

.. seealso:: :doc:`CMS-Seiten <cms-seiten>` | :doc:`Registerkarte SEO <registerkarte-seo>`

.. Intern: oxbajj, Status:

