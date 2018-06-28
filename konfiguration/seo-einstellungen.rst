SEO-Einstellungen
=================

Kunden beginnen die Suche nach Artikeln sehr oft mit Anfragen bei Suchmaschinen und -portalen. Damit sie dabei genau Ihren Shop, die Artikel und speziellen Angebote finden, müssen die entsprechenden Informationen optimal aufbereitet und indiziert sein. Der OXID eShop beherrscht seit der 4er Version die Suchmaschinenoptimierung, englisch: Search Engine Optimization (SEO). Die SEO-Implementierung erzeugt automatisch sprechende URLs für Kategorien und Artikel. Dabei werden reservierte Wörter und Sonderzeichen ebenso berücksichtigt, wie unterschiedliche Sprachen des Shops.

Shopbetreiber müssen lediglich einige Einstellungen vornehmen, um konkrete Inhalte für die Suchmaschinenoptimierung vorzugeben. Dabei handelt es sich um den Seitentitel, den Aufbau der URLs und die sogenannten Metadaten. Die Inhalte können in jeder Sprache des Shops definiert werden.

Seitentitel
-----------
Der Seitentitel wird bei einigen Browsern noch in der Titelleiste angezeigt und beim Abspeichern einer Seite als Lesezeichen oder Favorit verwendet. Obwohl der Seitentitel im Shop also nahezu unsichtbar ist, spielt er für Suchmaschinen eine wichtige Rolle. Suchmaschinen entnehmen dem Seitentitel die Information, welcher Inhalt auf einer Webseite zu finden ist. Die Seitentitel, außer der für die Startseite des Shops, werden automatisch aus dem Titel eines Artikels oder einer Kategorie generiert und mit einem Präfix und einem Suffix versehen.

Beispiel für den Aufbau eines Seitentitels: OXID Surf- und Kiteshop | Transportcontainer THE BARREL | online kaufen

Die Einstellungen für den Seitentitel befinden sich unter :menuselection:`Stammdaten --> Grundeinstellungen --> SEO`. Achten Sie darauf, dass die gewünschte Sprache ausgewählt ist.

:guilabel:`Titel Präfix` |br|
Text, der vor den generierten Teil des Seitentitels gestellt wird. Tragen Sie hier am besten den Namen Ihres Shops ein. Beispiel aus dem Demoshop: OXID Surf- und Kiteshop.

:guilabel:`Titel Suffix` |br|
Text, der an den generierten Teil des Seitentitels angehangen wird. Ergänzen Sie hier, was für alle Seiten des Shops charakteristisch ist. Beispiel aus dem Deomshop: online kaufen.

:guilabel:`Titel der Startseite` |br|
Für die Startseite wird der Text des Seitentitels festgelegt. Er sollte das Angebot Ihres Onlineshops mit prägnanten Worten beschreiben. Abweichend von allen anderen Seiten, besteht der Seitentitel der Startseite aus Präfix und definiertem Text. Der Suffix wird nicht verwendet. Beispiel aus dem Demoshop: OXID Surf- und Kiteshop | Der Onlineshop für Wassersport und Sommerspass.

Aufbau der URLs
---------------
Sogenannte sprechende URLs sind ebenfalls ein wichtiger Teil der Suchmaschinenoptimierung. Anstatt URLs mit Parametern und kryptischen Werten anzuzeigen, wird die URL umgeschrieben und zeigt stattdessen den Namen der Kategorie und des Artikels. Das ist gut für Suchmaschinen und für Besucher Ihres Onlineshops allemal.

Beispiel für intern verwendete URL: ``www.ihreshopurl.de/index.php?`` |br|
``cl=details\&anid=f4f73033cf5045525644042325355732\&cnid=fadcb6dd70b9f6248efa425bd159684e``

Beispiel für umgeschriebene, sprechende URL: ``www.ihreshopurl.de/Angebote/Transportcontainer-THE-BARREL.html``

Ebenso wie die Festlegungen für den Seitentitel sind die für die URLs sprachabhängig. Achten Sie darauf, dass die gewünschte Sprache ausgewählt ist.

:guilabel:`Standardsprache für SEO URLs` |br|
Für die hier eingestellte Standardsprache werden keine Sprachkürzel (de, en usw.) in den URLs verwendet. In den URLs der anderen Sprachen wird das entsprechende Sprachkürzel eingefügt.

:guilabel:`SEO IDs Trennzeichen (z. B.\"+\",\"-\")` |br|
Das Trennzeichen wird verwendet, wenn Kategorie- oder Artikeltitel aus mehreren Worten bestehen. Es wird anstelle eines Leerzeichens in die URL eingefügt. Der Bindestrich ist der Standard für das Trennzeichen.

Beispiel: ``www.ihreshopurl.de/Kategorie-aus-mehreren-Worten/Artikel-aus-mehreren-Worten.html``.

:guilabel:`SEO Suffix um gleiche Artikel zu unterscheiden` |br|
Wenn mehrere Artikel den gleichen Titel haben und in der gleichen Kategorie sind, würden sie die gleiche URL erhalten. Damit das nicht passiert, wird das SEO Suffix angehängt. Dadurch werden gleiche URLs vermieden. Wenn Sie kein SEO Suffix angeben, wird ``-oxid`` als Standard verwendet.

:guilabel:`Zeichen, die in SEO URLs ersetzt werden` |br|
Bestimmte Sonderzeichen wie Umlaute (Ä, Ö, Ü) sollten in URLs nicht vorkommen, da Sie Probleme verursachen können. In dem Eingabefeld wird angegeben, mit welchen Zeichen die Sonderzeichen ersetzt werden. Die Syntax ist Sonderzeichen =\>Ersatzzeichen, zum Beispiel Ü =\>Ue. Für die deutsche Sprache sind die Ersetzungen bereits eingetragen. Falls Sie Sonderzeichen und Ersetzungen, beispielsweise für eine neue Sprache, eintragen oder ergänzen wollen, verwenden Sie dafür jeweils eine separate Zeile.

.. hint:: Seit der Shopversion 4.7.0/5.0.0 wird die Liste der Zeichen, die in der URL durch andere Zeichen zu ersetzen sind (Transliteration), in der Datei :file:`/application/translation/{local}/translit_lang.php` definiert. Der Eingabebereich auf der Registerkarte :guilabel:`SEO` wurde entfernt.

:guilabel:`Reservierte Wörter (werden automatisch mit dem SEO Suffix versehen)` |br|
Bestimmte URLs sind im eShop festgelegt, zum Beispiel ``www.ihreshopurl.de/admin``, um den Administrationsbereich zu öffnen. Wenn eine Kategorie\"admin\"heißen würde, wäre deren URL ebenfalls ``www.ihreshopurl.de/admin``. Die Kategorie könnte nicht geöffnet werden. Deswegen wird an solche URLs automatisch das SEO Suffix angehängt. Standardmäßig behandelt der OXID eShop alle Verzeichnisse des Shops, auch selbst hinzugefügte, wie reservierte Wörter. Im Eingabefeld können Sie weitere reservierte Wörter hinzufügen.

:guilabel:`Wörter, die bei der Erzeugung der Meta-Tags für Suchmaschinen ignoriert werden` |br|
Wenn bei Artikeln oder Kategorien keine eigenen Meta-Tags vorhanden sind, werden diese Informationen aus der Beschreibung generiert. Dabei sollten Wörter weggelassen werden, die keinen Informationswert haben. Alle Wörter die im Eingabefeld aufgelistet sind, werden bei der automatischen Generierung ignoriert.

:guilabel:`Statische URLs` |br|
Für bestimmte Seiten, beispielsweise Kontakt und Newsletter, wurden statische URLs definiert. Diese ersetzen die internen URLs mit den verschiedenen Parametern. Sie können neue statische URLs anlegen oder bestehende, auch in verschiedenen Sprachen, ändern.

Metadaten
---------
Obwohl Metadaten nicht mehr die entscheidende Bedeutung für Suchmaschinen haben, gibt es die Möglichkeit, auf deren Inhalte Einfluß zu nehmen. Es gibt Metadaten für die Startseite und Metadaten für Artikel und Kategorien. Das sind Formulierungen und Begriffe, die als Bescheibung oder Schlüsselworte mit der jeweiligen Seite ausgeliefert werden.

Beispiel aus dem Demoshop:

``\<meta name=\"description\"content=\"Alles zum Thema Wassersport, Sportbekleidung und Mode.`` |br|
``Umfangreiches Produktsortiment mit den neusten Trendprodukten. Blitzschneller Versand.\"\>``

``\<meta name=\"keywords\"content=\"kite, kites, kiteboarding, kiteboards, wakeboarding, wakeboards,`` |br|
``boards, strand, sommer, wassersport, mode, fashion, style, shirts, jeans, accessoires, angebote\"\>``

Startseite
^^^^^^^^^^
Die Metadaten für die Startseite des Shops können unter :menuselection:`Kundeninformationen --> CMS` eingetragen werden. Die CMS-Seite\"META Description Startseite\"nimmt dabei die Beschreibung des Shops, die CMS-Seite\"META Keywords Startseite\"die Keywörter auf.

Kategorien und Artikel
^^^^^^^^^^^^^^^^^^^^^^
Die Metadaten für Kategorien und Artikel werden automatisch aus deren Beschreibung generiert. Sie können durch selbst formulierte Bescheibungen und Schlüsselworte für jede einzelne Kategorie oder jeden einzelnen Artikel überschrieben werden. Die Metadaten werden auf der Registerkarte :guilabel:`SEO` bei der Kategorie oder beim Artikel eingetragen.

.. Intern: oxbajb, Status: