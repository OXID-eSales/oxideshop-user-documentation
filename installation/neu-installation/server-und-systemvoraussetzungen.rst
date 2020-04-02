Server und Systemvoraussetzungen
================================

OXID eShop kann auf verschiedenen Server-Systemen betrieben werden. Die Wahl eines passenden Hosting-Paketes hängt beispielsweise von der Anzahl der Artikel, der erwarteten Besucher im Shop und von der Anzahl der Bestellungen ab. Genügt für einen kleinen Shop mit einigen hundert Artikeln, wenigen Besuchern im Monat und einem überschaubaren Bestellvolumen ein Shared Hosting-System, sollte für größere Shops ein Managed Server-System gewählt werden. Bei steigender Last ist der Betrieb einer Serverfarm mit Loadbalancing und einem Datenbankcluster in Betracht zu ziehen. Beratung und Unterstützung bei der Auswahl des geeigneten Systems finden Sie bei unseren `OXID Partnern (Hosting) <https://www.oxid-esales.com/oxid-welt/partner/partner-finden/>`_. Diese stellen speziell auf den OXID eShop zugeschnittene Lösungen bereit.

Für den Betrieb des OXID eShop Version 6 müssen die unten stehenden Systemvoraussetzungen erfüllt sein. Es gibt einige Änderungen gegenüber den Systemvoraussetzungen für die Shopversionen 4 und 5. Dazu gehören die unterstützten Versionen für den Webserver Apache, für die MySQL-Datenbank und für die serverseitige Script- und Programmiersprache PHP.

Webserver
---------

* Apache Versionen 2.2 und 2.4 (auf Linux)
* 500 MB freier Webspace für die Community und die Professional Edition
* 750 MB freier Webspace für die Enterprise Edition
* Installierte Erweiterung *mod_rewrite*

Bitte beachten Sie, dass trotz installierter Erweiterung *mod_rewrite* bei der Prüfung der Systemgesundheit die Voraussetzungen nicht erfüllt sein können. Ein Grund dafür ist oft die Einstellung für *AllowOverride* in der Apache-Konfiguration des vHosts. Diese wurde mit Apache 2.3.9 auf *AllowOverride None* geändert.

Der Zend Guard Loader wird nicht länger benötigt, da OXID eShop 6 unverschlüsselt ist.

Datenbank
---------

* MySQL 5.5 und 5.7

Der Datenbankbenutzer benötigt ausreichende Berechtigung, um während der Installation eine Datenbank erstellen zu können, sofern diese nicht bereits existiert. Die Berechtigung muss auch das Erstellen von Views erlauben.

Das Transaction Isolation Level muss serverseitig beim Standardwert *REPEATABLE READ* der InnoDB Storage Engine belassen werden.

PHP
---

* PHP Versionen 7.0 und 7.1
* Empfohlen wird ein *memory_limit* von 60 MB, mindestens aber 32 MB
* Die PHP-Einstellung *session.auto_start* in der Datei :file:`php.ini` sollte dektiviert sein (OFF)
* Datei-Uploads sollten in PHP aktiviert sein
* Aktiviertes *allow_url_fopen* und *fsockopen* auf Port 80
* Apache-Servervariablen *REQUEST_URI* oder *SCRIPT_URI* müssen vorhanden sein
* *ini_set* erlaubt

PHP-Erweiterungen, die installiert sein müssen:

* *GD LIB* Version 2.x
* *PDO_MySQL*
* *BC Math*
* *JSON*
* *iconv*
* *tokenizer*
* *mbstring*
* *cURL*
* *SOAP*
* *DOM*

Composer
--------

Composer wird für die Installation des OXID eShop und Änderungen im Autoloading von Dateien (nicht zur Laufzeit) benötigt. Die Anforderungen an Composer finden sich unter `https://getcomposer.org/doc/00-intro.md#system-requirements <https://getcomposer.org/doc/00-intro.md#system-requirements>`_.

OpenSSL
-------

Für die zu einer Compilation gehörenden Module wird OpenSSL benötigt.

* *openssl* >= 1.0.1

.. Intern: oxbaac, Status:
