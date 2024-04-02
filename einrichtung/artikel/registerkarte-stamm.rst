﻿Registerkarte Stamm
===================

Die Registerkarte :guilabel:`Stamm` nimmt wichtige Informationen zum Artikel auf. Erstellen oder bearbeiten Sie hier einen Artikel.

Wenn Sie einen Artikel neu anlegen, können Sie ihn direkt einer Kategorie zuzuordnen. Verwenden Sie dafür die Dropdown-Liste :guilabel:`In Kategorie` am unteren Ende des Eingabebereichs.

Nach dem Speichern des Artikels ist die schnelle Zuordnung der Kategorie auf dieser Registerkarte nicht mehr möglich.

.. figure:: ../../media/screenshots/oxbaci01.png
   :alt: Artikel - Registerkarte Stamm
   :width: 650
   :class: with-shadow

   Abb.: Artikel - Registerkarte Stamm

Mit der Sprachumstellung, die erst nach Anlegen des Artikels unten im Eingabebereich angezeigt wird, lassen sich die Informationen und Einstellungen zum Artikel direkt in einer weiteren Sprache bearbeiten.

:guilabel:`Aktiv`
   Aktivieren Sie dieses Kontrollkästchen, damit der Artikel im Shop angezeigt wird.

   Wenn ein Artikel nicht aktiviert wurde, ist er in der Datenbank vorhanden, erscheint jedoch nicht im Shop.

:guilabel:`Versteckt`
   Wenn dieses Kontrollkästchen aktiviert ist, wird der Artikel nicht im Shop-Frontend angezeigt, ist aber mit einem direkten Link aufrufbar.

   Dadurch kann der Artikel im Shop gefunden werden, auch wenn er momentan oder gar nicht mehr angeboten wird, der Link aber noch in den Suchmaschinen gelistet ist.

.. _zeitaktivierung:

:guilabel:`Oder aktiv von` ... :guilabel:`bis` ...
   Definieren Sie einen Zeitraum, in dem ein Artikel aktiv ist.

   Durch solche zeitgesteuerten Artikel können Sie beispielsweise ein Angebot umsetzen, das nur für eine bestimmte Zeit gültig sein soll.

   **Vorgehen**

   1. Aktivieren Sie unter :menuselection:`Stammdaten --> Grundeinstellungen` auf der Registerkarte :guilabel:`Perform.` das Kontrollkästchen :guilabel:`Beim Laden von Artikeln \"Aktiv von/bis\" berücksichtigen`.
   #. Deaktivieren Sie beim Artikel das Kontrollkästchen :guilabel:`Aktiv` (:ref:`oxbaci02`, Pos. 2).
   #. Geben Sie Anfang und Ende im Format :code:`JJJJ-MM-TT HH:MM:SS` an (:ref:`oxbaci02`, Pos. 3). Datum und Zeit des Endes der Aktivierung sind nicht optional.

      Wollen Sie einen Artikel im Grunde nur ab einem bestimmten Datum aktiv schalten, dann geben Sie eine weit in der Zukunft liegende Endezeit ein.

   Ihr zeitgesteuerte Artikel ist in der Artikelliste mit einem Sanduhr-Icon markiert (:ref:`oxbaci02`, Pos. 1).

   .. _oxbaci02:

   .. figure:: ../../media/screenshots/oxbaci02.png
      :alt: Angebote zeitlich steuern
      :width: 650
      :class: with-shadow

      Abb.: Angebote zeitlich steuern

:guilabel:`Titel`
   Der Artikel wird mit diesem Titel im Shop angezeigt.

   Vergeben Sie prägnante Artikeltitel mit genauen Informationen. Das ist informativ für die Besucher des Shops und gleichermaßen interessant für Suchmaschinen.

:guilabel:`Art.-Nr.`
   Versehen Sie den Artikel mit einer eindeutigen Artikelnummer. Diese wird dem Kunden im Shop in der Detailansicht des Artikels angezeigt. Darüber ist der Artikel auch suchbar.

   Wie Sie die Artikelnummer aufbauen, ist nicht vorgeschrieben. Das hängt von der Anzahl der Artikel ab oder aber auch davon, ob die Artikelnummer beispielsweise durch ein Warenwirtschaftssystem vorgegeben wird.

:guilabel:`EAN`
   Eindeutige Produktkennzeichnung, welche hier hinterlegt werden kann.

   Für Europa ist dies die `Europäische Artikelnummer (EAN) <http://de.wikipedia.org/wiki/European_Article_Number>`_ .

   In Amerika ist es der `Universal Product Code (UPC) <http://de.wikipedia.org/wiki/Universal_Product_Code>`_ und in Japan die Japanese Article Number (JAN).

   Das Feld kann auch die `Internationale Standardbuchnummer (ISBN) <http://de.wikipedia.org/wiki/ISBN>`_ aufnehmen.

:guilabel:`Hersteller EAN`
   Zusatzfeld für eine weitere Kategorisierung des Artikels, beispielsweise die EAN-Identifizierung des Herstellers (Zahlen 4 bis 7 des Barcodes).

:guilabel:`Hersteller-Artikelnummer (MPN)`
   MPN (Manufacturer's Part Number). Nummer, welche dem Artikel eindeutig einem Hersteller zuordnet.

:guilabel:`Kurzbeschr.`
   Beschreiben Sie den Artikel mit wenigen Worten.

   Die Kurzbeschreibung wird in der Detailansicht des Artikels zusammen mit Titel, Artikelnummer, Preis und Artikelbild angezeigt.

   Diese Informationen charakterisieren den Artikel und der Kunde kann sie auf einen Blick erfassen.

:guilabel:`Suchbegriffe`
   Geben Sie hier Begriffe ein, mit welchen der Artikel im Shop gesucht werden kann.

   Ergänzen Sie dabei die im Titel und in der Beschreibung eines Artikels vorkommenden Wörter und verwenden Sie Verallgemeinerungen.

   So finden Kunden auch Artikel im Shop, wenn sie nach einem Begriff suchen, der weder im Titel noch in der Beschreibung eines Artikels enthalten ist.

   Trennen Sie mehrere Suchbegriffe durch Leerzeichen oder Komma.

:guilabel:`Lieferant`
   Wählen Sie hier den Lieferanten des Artikels aus.

   Lieferanten werden unter :menuselection:`Stammdaten --> Lieferanten` erstellt und bearbeitet.

:guilabel:`Hersteller`
   Sie können den Hersteller des Artikels aus der Liste auswählen.

   Hersteller werden unter :menuselection:`Stammdaten --> Hersteller` erstellt und bearbeitet.

:guilabel:`Preis (€)`
   Tragen Sie hier den Verkaufspreis des Artikels ein.

   Standard ist der Bruttopreis.

   Der Preis wird an die Varianten eines Artikels vererbt, wenn für diese kein gesonderter Preis festgelegt wurde.

   Es ist auch möglich, die Eingabe des Preises auf netto umzustellen. Die Einstellung dafür finden Sie in :menuselection:`Stammdaten --> Grundeinstellungen`, Registerkarte :guilabel:`Einstell.` unter :guilabel:`Weitere Einstellungen`. Sie gilt generell für alle Artikel.

   Neben dem Eingabefeld für den Preis wird immer in Klammern der tatsächliche Verkaufspreis angezeigt. Gibt es für einen Artikel einen Rabatt, wird auch dessen rabattierter Preis angezeigt.

:guilabel:`Alt. Preise (€)`
   In den drei Feldern können Sie alternative Preise hinterlegen. Diese sind direkt mit den Benutzergruppen \"Preis A\", \"Preis B\" und \"Preis C\" verbunden.

   Damit lassen sich für bestimmte Kunden eigene Preise anstelle des regulären Preises einrichten und anzeigen.

:guilabel:`Spez. MwSt.`
   Benötigen Artikel eine vom Standard im Shop abweichende Mehrwertsteuer, kann dieser Mehrwertsteuersatz hier eingetragen werden.

   Der Mehrwertsteuersatz, welcher standardmäßig im Shop verwendet wird, ist in :menuselection:`Stammdaten --> Grundeinstellungen`, Registerkarte :guilabel:`Einstell.` unter :guilabel:`Mehrwertsteuer` festgelegt.

:guilabel:`In Sprache`
   Der Artikel lässt sich auch in weiteren aktiven Sprachen des Shops bearbeiten. Wählen Sie eine Sprache aus der Liste aus.

Langbeschreibung des Artikels
-----------------------------
Auf der rechten Seite der Registerkarte :guilabel:`Stamm` geben Sie die Langbeschreibung des Artikels in einen Editor ein.

Dieser arbeitet nach dem Prinzip WYSIWYG (What You See Is What You Get), er zeigt also den Text so an, wie er später in der Detailansicht des Artikels als Beschreibung zu sehen sein wird.

Der Editor bietet die Möglichkeit der Textformatierung, des Einfügens von Links, Bildern und Videos. Für spezielle und darüber hinausgehende Anforderungen kann der HTML-Code angezeigt und bearbeitet werden.

.. seealso:: :doc:`Alternative Preise für Benutzergruppen <../artikel-und-kategorien/alternative-preise-fuer-benutzergruppen>` | :doc:`Hersteller <../hersteller/hersteller>` | :doc:`Lieferanten <../lieferanten/lieferanten>`

.. Intern: oxbaci, Status:, F1: article_main.html