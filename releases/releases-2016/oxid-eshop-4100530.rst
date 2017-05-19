OXID eShop 4.10.0/5.3.0
***********************
Versionsbezeichnung: 5.3.0

Edition: Enterprise Edition

Versionsbezeichnung: 4.10.0

Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 05.07.2016

Veröffentlichungstermin Beta 1: 26.04.2016

Allgemeines
-----------
Der OXID eShop 4.10.0/5.3.0 wird mit dem responsiven Theme \"Flow\" (Beta-Version für alle Shop-Editionen), dem Visual CMS (nur Professional und Enterprise Edition) und dem Modul PAYONE (alle Shop-Editionen) ausgeliefert. Der Shop läuft unter PHP 5.3, 5.4, 5.5 und 5.6.

Hinweis:

Das Theme \"Flow\", Visual CMS und das Modul PAYONE sind nicht in den kumulativen Update-Paketen, sondern nur im Installationspaket für eine Neu-Installation enthalten.

Installation
++++++++++++
Für die Installation, folgen Sie bitte den Anleitungen in der Dokumentation und Hilfe:

`OXID eShop neu installieren <https://www.oxid-esales.com/de/support-services/dokumentation-und-hilfe/oxid-eshop/installation/oxid-eshop-neu-installieren/server-und-systemvoraussetzungen.html>`_ 

`OXID eShop aktualisieren <https://www.oxid-esales.com/de/support-services/dokumentation-und-hilfe/oxid-eshop/installation/oxid-eshop-aktualisieren/update-vorbereiten.html>`_

Hinweise: Wenn Sie einen OXID eShop auf die Version 4.10.0/5.3.0 aktualisieren wollen, der bisher das Theme RoxIVE von Digidesk verwendete, muss zuvor die Datei :file:`4.10.0.sql` aus dem Verzeichnis :file:`/updateApp/updates/sql` des Update-Paketes gelöscht werden. Der Grund dafür ist, dass ansonsten während des Updates versucht wird, Theme-Einstellungen mit der selben OXID wie für RoxIVE in die Datenbank zu schreiben.

Wir empfehlen dringend, das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, auszuführen. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

Haben Sie eine Enterprise Edition und MySQL 5.6 im Einsatz, beachten Sie bitte diesen `Blog-Post <http://planet.oxidforge.org/2015/11/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_ (in englischer Sprache).

Neue Funktionen
---------------
Responsives Theme \"Flow\"
++++++++++++++++++++++++++
Nach der Installation präsentiert sich der OXID eShop mit dem neuen responsiven Theme \"Flow\", sobald es unter :menuselection:`Erweiterungen --> Themes` aktiviert wurde. Es stellt mit seiner gestalterischen und technischen Umsetzung sicher, dass sich die Anzeige des Shops an die Grüße und Auflösung der Displays aller verwendeten Endgeräte, wie beispielsweise Laptops, Desktop-Computer, Tablets und Smartphones, anpasst. Das betrifft die Anordnung und Darstellung der einzelnen Seitenelemente des Frontends und auch die unterschiedliche Bedienung mit Maus oder Touchscreen. Das Theme \"Flow\" wird das bisherige Standardtheme \"Azure\" ablösen.

Visual CMS
++++++++++++
Der OXID eShop Professional und Enterprise Edition wird mit dem Visual CMS in einer Beta-Version ausgeliefert. Das Modul, welches zunächst unter :menuselection:`Erweiterungen --> Module` aktiviert werden muss, erlaubt die einfache Erstellung und Bearbeitung von CMS-Inhalten. Dafür können so genannte Widgets per Drag \& Drop angeordnet und angepasst werden. Visual CMS ist auf das Thema \"Flow\" abgestimmt. Das aktivierte Modul ersetzt die bisherige Bearbeitung von CMS-Seiten mit dem WYSIWIG-Editor. Bis dahin erstellte CMS-Seiten werden nicht verändert, können aber nur ohne aktiviertes Visual CMS bearbeitet werden.

Dem Installationspaket liegt ein Handbuch im Verzeichnis :file:`/documentation/DDOE_VISUALCMS` bei.

Modul PAYONE
++++++++++++
Mit dem Modul wird die Anbindung an den Payment Service Provider PAYONE realisiert, der Zahlungsabwicklung und alle Finanzdienstleistungen aus einer Hand bietet.

Verbesserungen und Anpassungen
------------------------------
Administrationsbereich mit neuem Layout
+++++++++++++++++++++++++++++++++++++++
Die Anzeige des Administrationsbereiches wurde überarbeitet. Änderungen in den Stylesheets können im Repository der Community Edition auf `GitHub <https://github.com/OXID-eSales/oxideshop_ce/commit/9b8f2d3e5b346cf5b3c4ad616d20d1b22836accd>`_ eingesehen werden.

Aktualisierter PHPMailer
++++++++++++++++++++++++
Die PHP-Klasse zum Erstellen und Versenden von E-Mails wurde auf die Version 5.2.14 aktualisiert.

Warenkorb wird nach Abmelden eines Benutzers geleert
++++++++++++++++++++++++++++++++++++++++++++++++++++
Wenn ein Benutzer sich vom Shop abmeldete nachdem er Artikel in den Warenkorb legte, wurden diese Artikel einem sich danach anmeldenden Benutzer angezeigt, der den selben Browser verwendete. Der Warenkorb wird nun beim Abmelden eines Benutzers geleert. Siehe: `https://bugs.oxid-esales.com/view.php?id=5771 <https://bugs.oxid-esales.com/view.php?id=5771>`_ .

Korrekturen
-----------
Korrekturen 4.10.0/5.3.0: `https://bugs.oxid-esales.com/changelog_page.php?version_id=320 <https://bugs.oxid-esales.com/changelog_page.php?version_id=320>`_

Korrekturen 4.10.0/5.3.0 Beta 1: `https://bugs.oxid-esales.com/changelog_page.php?version_id=315 <https://bugs.oxid-esales.com/changelog_page.php?version_id=315>`_

Korrekturen 4.10.0/5.3.0 Beta 1: `https://bugs.oxid-esales.com/changelog_page.php?version_id=314 <https://bugs.oxid-esales.com/changelog_page.php?version_id=314>`_

Weiterführende Informationen für Entwickler finden Sie auf der `OXIDforge <http://oxidforge.org/en/oxid-eshop-version-4-10-0-ce-pe-5-3-0-ee.html>`_ .

Änderungen gegenüber der vorhergehenden Version können im Repository der Community Edition auf `GitHub <https://github.com/OXID-eSales/oxideshop_ce/compare/v4.9.9...v4.10.0>`_ eingesehen werden.

.. Intern: oxaahe, Status: