﻿Server und Systemvoraussetzungen
================================

OXID eShop kann auf verschiedenen Server-Systemen betrieben werden. Die Wahl eines passenden Hosting-Paketes hängt beispielsweise von der Anzahl der Artikel, der erwarteten Besucher im Shop und von der Anzahl der Bestellungen ab. Genügt für einen kleinen Shop mit einigen hundert Artikeln, wenigen Besuchern im Monat und einem überschaubaren Bestellvolumen ein Shared Hosting-System, sollte für größere Shops ein Managed Server-System gewählt werden. Bei steigender Last ist der Betrieb einer Serverfarm mit Loadbalancing und einem Datenbankcluster in Betracht zu ziehen. Beratung und Unterstützung bei der Auswahl des geeigneten Systems finden Sie bei unseren `OXID Partnern (Hosting) <https://www.oxid-esales.com/oxid-welt/partner/partner-finden/>`_. Diese stellen speziell auf den OXID eShop zugeschnittene Lösungen bereit.

Für den Betrieb des OXID eShop Version 7 müssen die unten stehenden Systemvoraussetzungen erfüllt sein.

Webserver
---------

* Apache Versionen 2.2 und 2.4 (auf Linux)
* 500 MB freier Webspace für die Community und die Professional Edition
* 750 MB freier Webspace für die Enterprise Edition
* *mod_rewrite* Erweiterung installiert

  .. note::

      Auch wenn die *mod_rewrite*-Erweiterung installiert ist, kann es sein, dass die Systemüberprüfung nicht den Anforderungen entspricht.

      Einer der Gründe dafür ist oft die Einstellung für *AllowOverride* in der Apache vhost-Konfiguration.

      Diese wurde mit Apache 2.3.9 auf *AllowOverride None* geändert.

* Kryptographisch ausreichende Konfiguration

  .. note::
      **Was ist eine kryptographisch ausreichende Konfiguration und wie erreicht Sie sie?**

      Eines der Merkmale einer sicheren Webanwendung ist die Fähigkeit, kryptografisch starke Zufallswerte zu erzeugen.

      Aus diesem Grund muss der PHP-Prozess Zugang zu einer geeigneten Zufallsquelle für seine CSPRNG (*Cryptographically Secure Pseudorandom Number Generator*) Funktionen (`random_int()`, `random_bytes()`) haben.

      In den meisten Fällen sind dazu keine zusätzlichen Anpassungen Ihrerseits erforderlich, und die Anwendungselemente sollten sofort zusammenarbeiten.

      Wenn jedoch durch eine der PHP-Funktionen (`random_int()` oder `random_bytes()`) eine Ausnahme ausgelöst wird, beginnen Sie mit der Fehlersuche, indem Sie die Dokumentation für die Funktionen unter `php.net/manual/de/function.random-bytes.php <https://www.php.net/manual/de/function.random-bytes.php>`_ und `php.net/manual/de/function.random-int.php <https://www.php.net/manual/de/function.random-int.php>`_ durchsehen.



Datenbank
---------

* MySQL 5.7 und 8.0
* MariaDB (getestet mit MariaDB 10.4)

Der Datenbankbenutzer benötigt ausreichende Berechtigung, um während der Installation eine Datenbank erstellen zu können, sofern diese nicht bereits existiert. Die Berechtigung muss auch das Erstellen von Views erlauben.

Das Transaction Isolation Level muss serverseitig beim Standardwert *REPEATABLE READ* der InnoDB Storage Engine belassen werden.

PHP
---

* PHP Versionen 8.0 und 8.1
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

* Composer

Composer wird für die Installation des OXID eShop und Änderungen im Autoloading von Dateien (nicht zur Laufzeit) benötigt. OXID eShop 7.0.0 wurde mit der Versionen 2.4 von Composer getestet.

OpenSSL
-------
Für die zu einer Compilation gehörenden Module wird OpenSSL benötigt.

* *openssl* >= 1.0.1


.. Intern: oxbaac, Status:
