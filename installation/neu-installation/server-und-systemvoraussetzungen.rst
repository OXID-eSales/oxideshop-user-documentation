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

Für den Betrieb des OXID eShop Version 7 muss Ihr System die folgenden Systemvoraussetzungen erfüllen.

Webserver
---------

.. todo: #VL prüfen

* Apache Versionen 2.2 oder 2.4 (auf Linux)
* 500 MB freier Webspace für die Community und die Professional Edition
* 750 MB freier Webspace für die Enterprise Edition
* Installierte Erweiterung *mod_rewrite*

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


atenbank
---------

.. todo: #VL prüfen

* MySQL 5.7 und 8.0
* MariaDB (getestet mit MariaDB 10.4)

Der Datenbankbenutzer benötigt ausreichende Berechtigung, um während der Installation eine Datenbank erstellen zu können, sofern diese nicht bereits existiert. Die Berechtigung muss auch das Erstellen von Views erlauben.

Das Transaction Isolation Level muss serverseitig beim Standardwert *REPEATABLE READ* der InnoDB Storage Engine belassen werden.

PHP
---

.. todo: #VL prüfen

* PHP Versionen 8.0 oder 8.1
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

.. todo: #VL prüfen

* Composer 2.2

.. attention::

   Eine Composer Version aktueller als 2.2 wird nicht unterstützt.

   Bitte beachten Sie, dass zum Stand der OXID eShop Version 6.5.0 die Composer Version 2.2 getestet wurde.

   Installieren Sie die Composer Version 2.2 beispielsweise wie folgt:

   .. code:: bash

      composer selfupdate --2.2


Composer wird für die Installation des OXID eShop und Änderungen im Autoloading von Dateien (nicht zur Laufzeit) benötigt. Die Anforderungen an Composer finden sich unter `https://getcomposer.org/doc/00-intro.md#system-requirements <https://getcomposer.org/doc/00-intro.md#system-requirements>`_.

OpenSSL
-------

Für die zu einer Compilation gehörenden Module wird OpenSSL benötigt.

* *openssl* >= 1.0.1


.. Intern: oxbaac, Status:
