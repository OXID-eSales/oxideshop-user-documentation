Individualisierung
******************
Die beim Anlegen eines neuen Shops erfolgte Vererbung kann zu einem späteren Zeitpunkt angepasst werden. In den Vererbungseinstellungen eines neuen Shops, kann die Vererbung aller Artikel, Attribute, Auswahllisten, Versandkosten, Versandkostenregeln, Hersteller, Lieferanten, Rabatte, Gutscheine, Geschenkverpackungen, Nachrichten und Links rückgängig gemacht werden. Die Vererbungseinstellungen sind auf der Registerkarte :guilabel:`Mall` unter :menuselection:`Stammdaten --> Grundeinstellungen` zu finden. Wird beispielsweise das Häkchen beim Kontrollkästchen :guilabel:`Alle Artikel vom Elternshop erben` entfernt, sind die geerbten Artikel nach dem Speichern der Vererbungseinstellungen nicht mehr verfügbar.

.. image:: ../../../media/screenshots-de/oxaags01.png
   :alt: Vererbter Artikel
   :height: 324
   :width: 650

Die vererbten Artikel und Einstellungen sind zum größten Teil inhaltlich nicht änderbar. Es gibt jedoch Ausnahmen. Bei vererbten Artikeln können die Preise geändert werden, wenn beim Anlegen des neuen Shops individuelle Preise erlaubt wurden. Dadurch lassen sich der Verkaufspreis des Artikels, die alternativen Preise und die Staffelpreise anpassen. Den vererbten Artikeln und Attributen können Kategorien zugeordnet werden. So kann eine andere Struktur des Warenkatalogs als die im Elternshop umgesetzt werden.

Für Rechte und Rollen sind ebenfalls eigene Zuordnungen von Benutzergruppen möglich. Die SEO-Einstellungen von Artikeln und Kategorien sind komplett editierbar.

In der Konfigurationsdatei :file:`config.inc.php` des OXID eShop können für Artikel Eigenschaften definiert werden, die nach einer Vererbung editierbar sein sollen. Dazu muss das Array ``aMultishopArticleFields`` mit dem zur Eigenschaft gehörenden Datenbankfeld erweitert werden.

Beispiel: Außer den Preisen soll, wie im obigen Screenshot zu sehen, auch die Kurzbeschreibung änderbar sein.

Eintrag in der Konfigurationsdatei:

``$this--> aMultishopArticleFields = array(\"OXPRICE\",\"OXPRICEA\",\"OXPRICEB\",\"OXPRICEC\", \"OXUPDATEPRICE\",\"OXUPDATEPRICEA\",\"OXUPDATEPRICEB\",\"OXUPDATEPRICEC\",\"OXUPDATEPRICETIME\", 
\"OXSHORTDESC\");``

In der Datenbanktabelle oxfield2shops muss für OXSHORTDESC ein Eintrag erstellt werden.

``ALTER TABLE oxfield2shop ADD OXSHORTDESC VARCHAR(255) NOT NULL DEFAULT '' COMMENT 'Kurzbeschreibung';``

.. Intern: oxaags, Status: