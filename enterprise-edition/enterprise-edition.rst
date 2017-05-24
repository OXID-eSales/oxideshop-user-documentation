Enterprise Edition
==================
Dieser Abschnitt enthält die Dokumentation zum OXID eShop Enterprise Edition. Darin werden ausschließlich die Funktionen beschrieben, welche die Enterprise Edition von der Professional und Community Edition unterscheiden. Alle gemeinsamen Funktionen sind in der übrigen Dokumentation und Hilfe dokumentiert.

Mall - Shops und Subshops
-------------------------
In der Enterprise Edition können mehrere Shops angelegt und über einen gemeinsamen Administrationsbereich bearbeitet werden. Abhängig von der erworbenen Lizenz sind derzeit bis zu 1.500 Subshops möglich. Mit der OXID eShop Enterprise Edition Version 5.2.0 wurde dafür die Mandantenfähigkeit komplett überarbeitet. Bis dahin wurden etwa 200 Subshops unterstützt.

Für die signifikante Steigerung der Anzahl von Mandanten waren Änderungen an der Kernfunktionalität, der Datenbank und der Templates notwendig. Die Präsentation des Warenkataloges in den einzelnen Subshops wird nicht mehr länger durch die Datenbankfelder OXSHOPINCL und OXSHOPEXCL gehandhabt. Alle Datenbanktabellen, die für die Abbildung von Subshops notwendig sind, erhielten sogenannte Mapping-Tabellen. *Beispiel* : Tabelle für die Artikel *oxarticles*  und deren Mapping-Tabelle *oxarticles2shop* .

Nach der Installation hat der OXID eShop Enterprise Edition einen einzigen Shop, der seine Artikel und Einstellungen an alle neue Shops vererben kann. Diese werden direkt im Administrationsbereich angelegt. Dabei kann eingestellt werden, ob der neue Shop ein normaler Subshop, ein Supershop und/oder ein Multishop sein soll. Subshops können Artikel erben und an ihre Subshops oder auch an Supershops vererben. Die besondere Funktion eines Supershops ist, dass seine Artikel mit jedem beliebigen Shop verknüpft werden können, unabhängig davon, ob er für diesen Shop der Elternshop ist. Mall-Funktion eines Multishop ist es hingegen, Artikel aus allen anderen Shops zu übernehmen und zusammen zu präsentieren.

Die Flexibilität beim Anlegen von Shops in der Enterprise Edition erlaubt die Umsetzung unterschiedlicher Szenarien für das Betreiben mehrerer Onlineshops. Das wird noch ergänzt durch die bestehenden Anpassungsmöglichkeiten in jedem einzelnen Shop. Das beginnt beim individuellen Layout, geht über die Darstellung in verschiedenen Sprachen und schließt die Feinjustierung bei den vererbten Eigenschaften, wie einen generellen Aufschlag auf Artikelpreise, das individuelle Anpassen von Preisen oder anderer Artikelmerkmale ein. Es ist auch möglich, dass die einzelnen Shops separate Bestellnummern generieren oder dass sich Benutzer an alle Shops anmelden dürfen.

Alle Details zum Hauptshop, zu Elternshops, Subshops, Supershops und Multishops finden Sie im Abschnitt :doc:`Mall-Funktion <mall-funktion/mall-funktion>`.

Rechte und Rollen
-----------------
Die Enterprise Edition verfügt über eine Rechte- und Rollenverwaltung, mit der Berechtigungen für Benutzer und Benutzergruppen vergeben werden können.

Die Berechtigungen können sich auf den Shop selbst, also das Frontend, beziehen. Es kann beispielsweise festgelegt werden, dass Artikel und Kategorien nur für bestimmte Benutzer und Benutzergruppen angezeigt werden oder dass sie ausschließlich für einen definierten Kundenkreis kaufbar sein sollen. Darüber hinaus können einzelne Bereiche der Artikeldarstellung, wie die Beschreibung, der Preis oder die Warenkorbfunktionalität nur für bestimmte Benutzer und Benutzergruppen sichtbar sein. Die Rechte für die Anzeige von Artikeln und Kategorien werden in Rollen zusammengefasst und den jeweiligen Benutzergruppen zugeordnet.

Für den Administrationsbereich des Shops können ebenfalls Rollen definiert werden. Die Rollen bilden verschiedene Aufgabenbereiche bei der Administration des OXID eShop ab. Sie erlauben unterschiedliche Zugriffe auf Menüs und Untermenüs der Navigation und auch auf einzelne Registerkarten des Eingabebereiches. Darüber hinaus können für Artikel und Kategorien Rechte sehr differenziert definiert werden. Diese regeln beispielsweise das Anlegen, Ändern und Löschen von Artikeln und Kategorien insgesamt und wenn nötig den Zugriff auf jedes einzelne Steuerelement (Feld, Kontrollkästchen oder Option) des jeweiligen Eingabebereiches.

Eine Übersicht über die Rechte- und Rollenverwaltung finden Sie im Dokument :doc:`Rechte und Rollen <rechte-und-rollen/rechte-und-rollen>`.

Caching
-------
Das Caching-System der Enterprise Edition wird durch drei Hauptkomponenten umgesetzt: durch den in den OXID eShop integrierten Cache Manager, unterstützt durch den Reverse Proxy Varnish und/oder durch Memcached. Das Zusammenwirken der Komponenten bewirkt, dass – wenn immer möglich – zwischengespeicherte Inhalte genutzt und an die anfragenden Web-Clients geschickt werden. Damit werden die Datenbankzugriffe reduziert und die Antwortzeiten des OXID eShop verkürzt.

In :doc:`Caching <caching/caching>` finden Sie eine Anleitung zur Konfiguration von Varnish inklusive der Möglichkeit zum Download der Konfigurationsdateien. Ebenso werden die Konfiguration von Memcached und die Einstellungen für das Caching beschrieben.

Master/Slave
------------
Die Enterprise Edition kann bei aktiviertem Master/Slave mit mehreren Datenbanken betrieben werden. Dabei ist eine Datenbank die Master-Datenbank, die hauptsächlich Schreibzugriffe verarbeitet. Die Slave-Datenbanken enthalten gespiegelte Daten und bedienen die Lesezugriffe. Ein Load-Balancer verteilt die Datenbankzugriffe nach dieser grundsätzlichen Unterscheidung auf die Master-Datenbank und auf die Slave-Datenbanken.

Eine Anleitung zur Konfiguration finden Sie im Dokument :doc:`Master/Slave <master-slave/master-slave>`.

.. Intern: oxbacy, Status: