Server und Systemvoraussetzungen
================================

Sie können OXID eShop auf verschiedenen Server-Systemen betreiben.

Die Wahl eines passenden Hosting-Pakets hängt beispielsweise von der Anzahl der Artikel, der erwarteten Besucher im Shop und von der Anzahl der Bestellungen ab.

Sie haben folgende Möglichkeiten:

* Für einen kleinen Shop mit einigen hundert Artikeln, wenigen Besuchern im Monat und einem überschaubaren Bestellvolumen genügt ein Shared Hosting-System.
* Für größere Shops wählen Sie ein Managed Server-System.
* Bei steigender Last empfiehlt sich eine Serverfarm mit Loadbalancing und einem Datenbank-Cluster.

Beratung und Unterstützung bei der Auswahl des geeigneten Systems finden Sie bei unseren `OXID Partnern (Hosting) <https://www.oxid-esales.com/oxid-welt/partner/partner-finden/>`_. Diese stellen speziell auf den OXID eShop zugeschnittene Lösungen bereit.

----------------------------------------------------------------------------------------------------------

Für den Betrieb des OXID eShop Version 6 muss Ihr System die folgenden Systemvoraussetzungen erfüllen.

Webserver
---------

* Apache Versionen 2.2 oder 2.4 (auf Linux)
* 500 MB freier Webspace für die Community und die Professional Edition
* 750 MB freier Webspace für die Enterprise Edition
* Installierte Erweiterung *mod_rewrite*

.. hint::

   Nach der Installation gelangen Sie ins webbasierte Setup des Shops.

   Bevor Sie das Setup ausführen können, prüft das System, ob die Systemvoraussetzungen erfüllt sind.

   Es kann sein, dass unter :guilabel:`Server-Konfiguration` das *Apache mod_rewrite Module* als fehlerhaft markiert ist, obwohl Sie das Modul installiert haben.

   Ein Grund dafür ist oft die Einstellung für *AllowOverride* in der Apache-Konfiguration des vHosts.

   Wenn Sie Apache 2.3.9 haben, stellen Sie sicher, dass *AllowOverride* den Wert *None* hat.


Der Zend Guard Loader wird nicht benötigt, da OXID eShop 6 unverschlüsselt ist.

Datenbank
---------

* MySQL 5.5 oder 5.7
* MariaDB (getestet mit MariaDB 10.4)

Der Datenbankbenutzer benötigt ausreichende Berechtigung, um während der Installation eine Datenbank erstellen zu können, sofern diese nicht bereits existiert. Die Berechtigung muss auch das Erstellen von Views erlauben.

Das Transaction Isolation Level muss serverseitig beim Standardwert *REPEATABLE READ* der InnoDB Storage Engine belassen werden.

PHP
---

* PHP Versionen 8.0 oder 7.4
* Empfohlen wird ein *memory_limit* von 60 MB, mindestens aber 32 MB
* Die PHP-Einstellung *session.auto_start* in der Datei :file:`php.ini` sollte deaktiviert sein (OFF)
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

.. note:: Für den Betrieb von PHP 8 wird dringend empfohlen, das error_reporting von PHP auf ``error_reporting = E_ALL & ~E_NOTICE & ~E_WARNING & ~E_DEPRECATED`` zu setzen, da Sie sonst eine Vielzahl von Warnungen erhalten werden.

Composer
--------

* Composer 1 oder 2 für OXID eShop 6.3.0
* Composer 2 ab OXID eShop 6.3.1

Composer wird für die Installation des OXID eShop und Änderungen im Autoloading von Dateien (nicht zur Laufzeit) benötigt. Die Anforderungen an Composer finden sich unter `https://getcomposer.org/doc/00-intro.md#system-requirements <https://getcomposer.org/doc/00-intro.md#system-requirements>`_.

OpenSSL
-------

Für die zu einer Compilation gehörenden Module wird OpenSSL benötigt.

* *openssl* >= 1.0.1


.. Intern: oxbaac, Status:
