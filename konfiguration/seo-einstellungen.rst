SEO-Einstellungen
=================

Optimieren Sie Ihren OXID eShop für Suchmaschinen, indem Sie Seitentitel, URLs und Metadaten gezielt anpassen.

|background|

Viele Kunden gelangen über Suchmaschinen zu Ihrem Shop. Um dort besser sichtbar zu sein, nehmen Sie die folgenden SEO-Einstellungen vor.

Nutzen Sie dazu die Suchmaschinenoptimierung, englisch: Search Engine Optimization (SEO). Die SEO-Implementierung erstellt automatisch sprechende URLs für Kategorien und Artikel. Dabei werden reservierte Wörter und Sonderzeichen ebenso berücksichtigt wie unterschiedliche Sprachen des Shops.

Nehmen Sie als Shopbetreiber die nötigen Einstellungen vor, um konkrete Inhalte für die Suchmaschinenoptimierung vorzugeben.

Dabei handelt es sich um

* den Seitentitel
* den Aufbau der URLs
* die sogenannten Metadaten (:ref:`oxbabi01`).

Definieren Sie die Inhalte für jede Sprache Ihres OXID eShops.

Seitentitel festlegen
---------------------
Der Seitentitel wird bei einigen Browsern noch in der Titelleiste angezeigt und beim Abspeichern einer Seite als Lesezeichen oder Favorit verwendet.

Suchmaschinen werten den Seitentitel als eines der wichtigsten Signale zur Seiteninhalte. Suchmaschinen entnehmen dem Seitentitel die Information, welcher Inhalt auf einer Webseite zu finden ist.

Die Seitentitel, außer der für die Startseite des OXID eShops, werden automatisch aus dem Titel eines Artikels oder einer Kategorie generiert und mit einem Präfix und einem Suffix versehen.

Beispiel für den Aufbau eines Seitentitels (:ref:`oxbabi01`, Pos. 1, 2, 3): OXID eShop | VisControl LCD | online kaufen


.. todo: Struktur des Titels auf Startseite: OXDEV-6802

|procedure|

1. Um die Einstellungen für den Seitentitel Ihres OXID eShops vorzunehmen, wählen Sie :menuselection:`Stammdaten --> Grundeinstellungen --> SEO`.
#. Stellen Sie sicher, dass die gewünschte Sprache ausgewählt ist.
#. Nehmen Sie die folgenden Einstellungen vor:

   * :guilabel:`Titel Präfix` :ref:`oxbabi01`, Pos. 1): Text, der :emphasis:`vor` den generierten Teil des Seitentitels gestellt wird ().

     Empfehlung: Tragen Sie den Namen Ihres OXID eShops ein. Beispiel aus dem Demoshop: "OXID eShop".

   * :guilabel:`Titel Suffix` (:ref:`oxbabi01`, Pos. 2): Text, der an den generierten Teil des Seitentitels angehängt wird.

     Ergänzen Sie hier, was für alle Seiten des OXID eShops charakteristisch ist. Beispiel aus dem Demoshop: "online kaufen".

   * :guilabel:`Titel der Startseite` (:ref:`oxbabi01`, Pos. 1): Legen Sie den Seitentitel für die Startseite fest.

     Beschreiben Sie das Angebot Ihres Onlineshops prägnant.

   .. _oxbabi01:

   .. figure:: ../media/screenshots/oxbabi01.png
      :alt: Metadaten: Seitentitel festlegen
      :width: 650
      :class: with-shadow

      Abb.: Metadaten: Seitentitel festlegen

|result|

Das System setzt den Seitentitel im Metadaten-Tag ``<title>`` zusammen.

Das passiert bei der Startseite Ihres OXID eShops anders als bei den übrigen Seiten.

Bei der Startseite setzt sich der Seitentitel aus dem Präfix (:ref:`oxbabi02`, Pos. 1 entspricht :ref:`oxbabi01`, Pos. 1) und dem Titel der Startseite (:ref:`oxbabi02`, Pos. 3 entspricht entspricht :ref:`oxbabi01`, Pos. 1) zusammen. Der mittlere Ausdruck `Startseite` (:ref:`oxbabi02`, Pos. 2) ist fest vorgegeben.

Anders als bei allen anderen Seiten besteht der Seitentitel der Startseite also aus Präfix und definiertem Text.

Das Suffix wird :emphasis:`nicht` verwendet. Beispiel aus dem Demoshop: "Der Onlineshop".

.. todo: META-Title of the startpage to be configurable: OXDEV-6802

.. _oxbabi02:

.. figure:: ../media/screenshots/oxbabi02.png
   :alt: Seitentitel der Startseite
   :width: 650
   :class: with-shadow

   Abb.: Seitentitel der Startseite

Der Seitentitel der übrigen Seiten besteht aus Präfix (:ref:`oxbabi03`, Pos. 1 entspricht :ref:`oxbabi01`, Pos. 1) und Suffix (:ref:`oxbabi03`, Pos. 3 entspricht :ref:`oxbabi01`, Pos. 2).

Der mittlere Teil in unserem Beispiel `VisControl LCD`,  :ref:`oxbabi03`, Pos. 2) entspricht dem Titel des Produkts, der Kategorie, der CMS-Seite, des Herstellers oder des Lieferanten.

.. _oxbabi03:

.. figure:: ../media/screenshots/oxbabi03.png
   :alt: Seitentitel und Metadaten einer untergeordneten Seite
   :width: 650
   :class: with-shadow

   Abb.: Seitentitel und Metadaten einer untergeordneten Seite

Sprechende URLs bilden
----------------------
Sogenannte sprechende URLs sind ebenfalls ein wichtiger Teil der Suchmaschinenoptimierung.

Statt technisch generierter URLs mit Parametern zeigt der Shop sprechende URLs mit Artikelnamen und Kategorien an. Das verbessert sowohl die Sichtbarkeit in Suchmaschinen als auch die Benutzerfreundlichkeit für Besucher Ihres Onlineshops.

Beispiel:

* Intern verwendete URL: ``www.ihreshopurl.de/index.php?cl=details\&anid=f4f73033cf5045525644042325355732\&cnid=fadcb6dd70b9f6248efa425bd159684e``
* Umgeschriebene, sprechende URL: ``www.ihreshopurl.de/Nach-Hersteller/Eng-Depot/VisControl-LCD.html``

|procedure|

Um sprechende URLs zu konfigurieren, tun Sie Folgendes:

1. Nehmen Sie unter :menuselection:`Stammdaten --> Grundeinstellungen --> SEO` folgende Einstellungen vor.

   Ebenso wie die Festlegungen für den Seitentitel sind auch die für die URLs sprachabhängig. Achten Sie darauf, dass die gewünschte Sprache ausgewählt ist.

   * :guilabel:`Standardsprache für SEO URLs`: Für die hier eingestellte Standardsprache werden keine Sprachkürzel (de, en usw.) in den URLs verwendet.

     In den URLs der anderen Sprachen wird das entsprechende Sprachkürzel eingefügt.

   * :guilabel:`SEO IDs Trennzeichen (z. B. +, -)`: Das Trennzeichen wird verwendet, wenn Kategorie- oder Artikeltitel aus mehreren Worten bestehen. Es wird anstelle eines Leerzeichens in die URL eingefügt. Der Bindestrich ist das Standard-Trennzeichen.

     Beispiel: ``www.ihreshopurl.de/Kategorie-aus-mehreren-Worten/Artikel-aus-mehreren-Worten.html``.

   * :guilabel:`SEO-Suffix, um gleiche Artikel zu unterscheiden`: Wenn mehrere Artikel den gleichen Titel haben und in der gleichen Kategorie sind, würden sie die gleiche URL erhalten.

     Damit das nicht passiert, wird das SEO-Suffix angehängt. Dadurch werden gleiche URLs vermieden.

     Wenn Sie kein SEO-Suffix angeben, wird ``-oxid`` als Standard verwendet.

   *  :guilabel:`Zeichen, die in SEO URLs ersetzt werden`: Bestimmte Sonderzeichen wie Umlaute (Ä, Ö, Ü) sollten in URLs nicht vorkommen, da Sie Probleme verursachen können. In dem Eingabefeld wird angegeben, mit welchen Zeichen die Sonderzeichen ersetzt werden.

     Die Syntax ist Sonderzeichen =\>Ersatzzeichen, zum Beispiel Ü =\>Ue.

     Für die deutsche Sprache sind die Ersetzungen bereits eingetragen. Falls Sie Sonderzeichen und Ersetzungen, beispielsweise für eine neue Sprache, eintragen oder ergänzen wollen, verwenden Sie dafür jeweils eine separate Zeile.

   * :guilabel:`Reservierte Wörter (werden automatisch mit dem SEO-Suffix versehen)`: Bestimmte URLs sind im eOXID eShop festgelegt, zum Beispiel ``www.ihreshopurl.de/admin``, um den Administrationsbereich zu öffnen.

     Wenn eine Kategorie \"admin\" heißen würde, wäre deren URL ebenfalls ``www.ihreshopurl.de/admin``. Die Kategorie könnte nicht geöffnet werden. Deswegen wird an solche URLs automatisch das SEO-Suffix angehängt.

     Standardmäßig behandelt der OXID eShop alle Verzeichnisse, auch selbst hinzugefügte, wie reservierte Wörter.

     Im Eingabefeld können Sie weitere reservierte Wörter hinzufügen.

   * :guilabel:`Wörter, die bei der Erzeugung der Meta-Tags für Suchmaschinen ignoriert werden`: Wenn für Artikel oder Kategorien keine eigenen Meta-Tags definiert sind, werden sie aus der Beschreibung erstellt.

     Lassen Sie Wörter weg, die keinen Mehrwert für Suchmaschinen bieten.

     Alle Wörter, die im Eingabefeld aufgelistet sind, werden bei der automatischen Generierung ignoriert.

   * :guilabel:`Statische URLs`: Für eine Reihe von Seiten wurden statische URLs definiert. Diese ersetzen die internen URLs mit den verschiedenen Parametern.

     Sie können neue statische URLs anlegen oder bestehende, auch in verschiedenen Sprachen, ändern.

   .. _oxbabi04:

   .. figure:: ../media/screenshots/oxbabi04.png
      :alt: URL-Einstellungen vornehmen
      :width: 650
      :class: with-shadow

      Abb.: URL-Einstellungen vornehmen

#. Speichern Sie Ihre Einstellungen.
#. Damit die Einstellungen wirksam werden, wählen Sie :guilabel:`SEO-URLs neu berechnen`.

Metadaten pflegen
-----------------

Metadaten tragen zur besseren Darstellung in Suchergebnissen bei. Daher empfiehlt es sich, sie manuell zu pflegen.

Definieren Sie Metadaten für die Startseite und Metadaten für Artikel und Kategorien. Das sind Formulierungen und Begriffe, die als Description :ref:`oxbabi03`, Pos. 4) und Keywords (:ref:`oxbabi03`, Pos. 5) mit der jeweiligen Seite ausgeliefert werden.


Metadaten für die Startseite erfassen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Definieren Sie Description und Keywords für die Startseite Ihres OXID eShops.

|procedure|

1. Wählen Sie :menuselection:`Kundeninformationen --> CMS-Seiten`.

#. Wählen Sie die betreffende Seite:

   * Um die Description Ihres OXID eShops einzugeben, wählen Sie die CMS-Seite ``META Description Startseite`` (Ident: ``oxstartmetadescription``) (:ref:`oxbabi05`).
   * Um die Keywords einzugeben, wählen Sie die CMS-Seite "META Keywords Startseite" (Ident: ``oxstartmetakeywords``).
#. Geben Sie die Metadaten auf der Registerkarte :guilabel:`Stamm` ein.
#. Speichern Sie Ihre Einstellungen

.. _oxbabi05:

.. figure:: ../media/screenshots/oxbabi05.png
   :alt: Beispiel: Description für die Startseite erfassen
   :width: 650
   :class: with-shadow

   Abb.: Beispiel: Description für die Startseite erfassen

Metadaten für Kategorien und Artikel erfassen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Standardmäßig werden die Metadaten für Kategorien und Artikel automatisch aus deren Beschreibung generiert.

Sie können die automatisch erzeugten Metadaten durch eigene Texte ersetzen.

|procedure|

Um die Metadaten manuell zu erfassen, tun Sie Folgendes:

1. Wählen Sie den Artikel oder Kategorie.
2. Geben Sie auf der Registerkarte :guilabel:`SEO` die Metadaten ein (:ref:`oxbabi06`).
#. Speichern Sie Ihre Einstellungen.

.. _oxbabi06:

.. figure:: ../media/screenshots/oxbabi06.png
   :alt: Beispiel: Metadaten für einen Artikel erfassen
   :width: 650
   :class: with-shadow

   Abb.: Beispiel: Metadaten für einen Artikel erfassen

|result|

Die Metadaten werden in die betreffende Seite eingebettet (:ref:`oxbabi03`, Pos. 4, 5).

.. Intern: oxbabi, Status:
