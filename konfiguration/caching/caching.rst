Caching
=======

In allen Shop-Editionen werden standardmäßig die Tabellenstrukturen der Datenbank, die Inhalte der verwendeten Sprachdateien und die durch die Smarty Template Engine kompilierten Templates gespeichert. Auch Abfragen der Datenbanktabelle OXSEO werden, wenn in den Performance-Einstellungen aktiviert, in Dateien geschrieben, um wiederholte Datenbankzugriffe zu vermeiden. Speicherort der Dateien ist das Verzeichnis :file:`/tmp` des Shops und dessen Unterverzeichnisse, beispielsweise :file:`/tmp/smarty`. Das Zwischenspeichern bewirkt, dass – wenn immer möglich – Inhalte aus dem Cache genutzt und an die anfragenden Web-Clients geschickt werden. Damit werden die Datenbankzugriffe reduziert und die Antwortzeiten des OXID eShop signifikant verkürzt.

OXID eShop Enterprise Edition bietet für das Caching weit darüber hinausgehende Möglichkeiten.

Dynamic Content Cache war von Anfang an integraler Bestandteil der Enterprise Edition. Es ist eine Caching-Lösung, bei der die erstellten HTML-Seiten einschließlich ihrer dynamischen Inhalte zwischengespeichert werden. Dabei können die technischen Möglichkeiten eines Zend Servers genutzt werden oder einfach das Dateisystem des Servers, auf dem der Shop läuft. Wird eine Seite vom Browser angefordert, wird zunächst geprüft, ob diese Seite im Cache und noch gültig ist. Die Gültigkeit wird anhand der gesetzten Lebensdauer (TTL, Time To Live) bestimmt. Ist die Seite im Cache und enthält dynamischen Inhalt, wird dieser nachgeladen und anschließend wird die komplette Seite an den Browser geschickt. Befindet sich die angeforderte Seite nicht im Cache, wird sie erstellt, angezeigt und im Cache abgelegt.

Mit der Version 5.0.0 der Enterprise Edition wurde das Caching erweitert.

Das neue und erweiterte Caching wird durch drei Hauptkomponenten umgesetzt: durch den in den OXID eShop integrierten Cache Manager, unterstützt durch den Reverse Proxy Varnish und/oder durch Memcached.

Der *Cache Manager*, welcher direkter Bestandteil des OXID eShop ist, verarbeitet alle Caching-Anforderungen und stellt sicher, dass die Daten in den verschiedenen eingesetzten Caches stets aktuell sind.

Der *Reverse Proxy Varnish* ist ein Webbeschleuniger. Das System verarbeitet noch vor dem Webserver eingehende Anfragen von Web-Clients und stellt die auszuliefernden Webseiten überwiegend aus zwischengespeicherten Inhalten zusammen. Inhalte werden vom Webserver abgefragt und aus der Datenbank gelesen, sobald die Lebensdauer des Caches abgelaufen ist.

*Memcached* ist ein Cache-Server. Durch dessen Einsatz wird es möglich, den Cache im Arbeitsspeicher anstatt im Dateisystem zu speichern. Der Zugriff auf Daten im Arbeitsspeicher ist deutlich schneller als ein Festplattenzugriff.

-----------------------------------------------------------------------------------------

Memcached
---------
**Inhalte**: Memcached, Hinweise zur Installation, Konfiguration |br|
:doc:`Artikel lesen <memcached>` |link|

Caching-Einstellungen
---------------------
**Inhalte**: Default Cache Backend, Cache Lebensdauer (TTL), Cache Connector, Dateisystem, Cache-Verzeichnis, Memcached, Memcached Server,  cachebare Seiten, Dynamic Content Caching, cachebare Klassen |br|
:doc:`Artikel lesen <caching-einstellungen>` |link|

.. note:: Weiterführende Links: Smarty Template Engine: `http://www.smarty.net <http://www.smarty.net/>`_ | Zend Server: `http://www.zend.com/en/products/zend_server <http://www.zend.com/en/products/zend_server>`_  | Memcached: `http://memcached.org <http://memcached.org/>`_

.. Intern: oxbabz, Status: