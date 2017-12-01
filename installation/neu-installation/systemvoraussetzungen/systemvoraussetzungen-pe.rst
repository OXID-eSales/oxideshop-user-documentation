Systemvoraussetzungen OXID eShop Professional Edition
=====================================================

Webserver
---------

* Apache Version 1.3 oder höher
* Zend Guard Loader
* Mindestens 100 MB freier Webspace
* Installierte Erweiterung *mod_rewrite*

Bitte beachten Sie, dass trotz installierter Erweiterung *mod_rewrite* bei der Prüfung der Systemgesundheit die Voraussetzungen nicht erfüllt sein können. Ein Grund dafür ist oft die Einstellung für *AllowOverride* in der Apache-Konfiguration des vHosts. Diese wurde mit Apache 2.3.9 auf *AllowOverride None* geändert.

MySQL
-----

* MySQL 5.7 - getestet
* MySQL 5.6 - getestet
* MySQL 5.5 - getestet und empfohlen
* MySQL 5.0 - mit bekannten Bugs |br|
  Aufgrund eines `Bugs in MySQL 5.0.36 und 5.0.37 <http://bugs.mysql.com/bug.php?id=27210>`_ sowie `5.0.41 <https://bugs.oxid-esales.com/view.php?id=1877>`_ funktioniert der eShop nicht einwandfrei mit diesen Versionen.
* SUPER-Privilegien für den Datenbankbenutzer während der Installation

PHP
---

* PHP 5.3.* (5.3.25 oder höher), PHP 5.4.*, PHP 5.5.* und PHP 5.6.*
* Empfohlen wird ein *memory_limit* von 30 MB, mindestens aber 14 MB.
* Die-PHP Einstellung *session.auto_start* sollte in der Datei :file:`php.ini` deaktiviert sein (OFF).
* Datei-Uploads sollten in PHP aktiviert sein.
* Aktiviertes *allow_url_fopen* und *fsockopen* auf Port 80.
* Apache-Servervariablen *REQUEST_URI* oder *SCRIPT_URI* müssen vorhanden sein.
* Der PHP 4-Kompatibilitätsmodus muss ausgeschaltet sein (*zend.ze1_compatibility_mode* = OFF)
* *ini_set* erlaubt
* *register_globals* ausgeschaltet
* *magic_quotes_gpc* ausgeschaltet
* PHP-Erweiterungen, die installiert sein müssen:
	* *GD LIB* Version 2.x
	*  *MySQL client connector* für MySQL 5
	*  *bcmath*
	*  *JSON*
	*  *php-xml*
	*  *libxml2*
	*  *iconv-extension*
	*  *tokenizer*
	*  *mbstring*
	*  *cURL*

Übersicht über die möglichen Betriebsrahmenbedingungen, welche auf folgenden Annahmen basiert:
----------------------------------------------------------------------------------------------

* Anzahl Kategorien 20% der Artikel, beispielsweise 1.000 Artikel ~ 200 Kategorien
* Der Besucherstrom verteilt sich auf über 14 Stunden pro Tag durchschnittlich
* Die Artikelanzahl beinhaltet auch mögliche Artikelvarianten
* Dennoch kann es bei manchen lastintensiven Tätigkeiten (z.B. Exporte) zu eingeschränkter Funktionalität kommen. Dies ist abhängig von Ihrem Provider (PHP-Einstellungen *max_execution_time* und *memory_limit*).

.. Intern: ---, Status: