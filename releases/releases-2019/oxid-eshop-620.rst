OXID eShop 6.2.0
================

Veröffentlichungstermin: 29.10.2019 |br|
Veröffentlichungstermin Beta 1: 02.08.2019

-----------------------------------------------------------------------------------------

Allgemeines
-----------

* Release Notes 6.0.0 - https://docs.oxid-esales.com/eshop/de/6.0/releases/releases-2017/oxid-eshop-600.html
* Release Notes 6.0.0 - https://docs.oxid-esales.com/eshop/de/6.1/releases/releases-2018/oxid-eshop-610.html

Der OXID eShop 6.2.0 wird als Compilation bereitgestellt. Diese enthält u.a. folgende Komponenten:

* OXID eShop CE 6.4.0
* OXID eShop PE
* OXID eShop EE
* Theme "Flow"
* Theme "Wave"
* Amazon Pay
* GDPR Opt-In
* Klarna
* Paymorrow
* PAYONE
* PayPal
* Summernote WYSIWIG-Editor und Mediathek
* Visual CMS (PE/EE)

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/b-6.1...b-6.2-beta>`_.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
Der OXID eShop 6.2.0 läuft unter PHP 7.1 und 7.2. Der Support für PHP 7.0 wurde eingestellt. Als Datenbank wird MySQL in der Version 5.5 oder 5.7 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

Installation
^^^^^^^^^^^^
Für die Installation, folgen Sie bitte den Anleitungen im Abschnitt "Installation":

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Update <../../installation/update/update>` |br|
:doc:`Spezial: von 6.1.x auf 6.2.0 aktualisieren <../../installation/update/von-6.1.x-auf-6.2.0-aktualisieren>`





Bitte führen Sie das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, aus. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------

Aktualisierte Komponenten der OXID eShop Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Folgende Komponenten wurden auf eine neue Version aktualisiert:

* OXID eShop CE (Update von 6.3.5 auf 6.4.0), `Changelog 6.4.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.4.0/CHANGELOG.md>`_
* OXID eShop EE (Update von ... auf ...)


Änderung beim Erstellen von Datenbankverbindungen und Suchanfragen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Folgende Klassen werden nicht mehr unterstützt:

.. code:: bash

   OxidEsales\EshopCommunity\Core\DatabaseProvider
   OxidEsales\EshopCommunity\Core\Database\Adapter\Doctrine\Database
   OxidEsales\EshopCommunity\Core\Database\Adapter\Doctrine\ResultSet
   OxidEsales\EshopCommunity\Core\Database\Adapter\DatabaseInterface
   OxidEsales\EshopCommunity\Core\Database\Adapter\ResultSetInterface

So kann die Methode ``getDb`` nicht mehr verwendet werden. Stattdessen wird die ``QueryBuilderFactory`` bereitgestellt, um Datenbankverbindungen herzustellen und Abfragen zu erstellen.

Der QueryBuilderFactoryInterface Namespace lautet:

.. code:: bash

   OxidEsales\EshopCommunity\Internal\Framework\Database\QueryBuilderFactoryInterface

Weitere Informationen dazu finden Sie im englischsprachigen Dokument <Interacting with the database> der Entwicklerdokumentation.

Sortierung von Zubehör für Artikel
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Im Zuordnungsfenster für das Zubehör lässt sich die Reihenfolge der zugeordneten Artikel ändern. Nachdem ein Artikel in der rechten Liste markiert wurde, kann dieser mit den jetzt angezeigten Minischaltflächen nach oben oder unten verschoben werden.



-----------------------------------------------------------------------------------------

Korrekturen
-----------

Korrekturen 6.0.0 Beta 1: https://bugs.oxid-esales.com/changelog_page.php?version_id=459


.. Intern: oxbais, Status: