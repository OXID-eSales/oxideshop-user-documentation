Systemvoraussetzungen OXID eShop Community Edition
==================================================
Webserver
---------
* Apache Version 1.3 oder höher
* Mindestens 100 MB freier Webspace
* Installierte *mod_rewrite* Erweiterung

MySQL
-----
* MySQL 5.7 - getestet
* MySQL 5.6 - getestet
* MySQL 5.5 - getestet und empfohlen
* MySQL 5.0 - mit bekannten Bugs
  Aufgrund eines `Bugs in MySQL 5.0.36 und 5.0.37 <http://bugs.mysql.com/bug.php?id=27210>`_ sowie `5.0.41 <https://bugs.oxid-esales.com/view.php?id=1877>`_ funktioniert der eShop nicht einwandfrei mit diesen Versionen.
* SUPER-Privilegien für den Datenbankbenutzer während der Installation

PHP
---
* PHP 5.3.* (5.3.25 oder höher), PHP 5.4.*, PHP 5.5.* und PHP 5.6.*
* Das
*  *memory_limit* muss mindestens 14MB hoch sein. Wir empfehlen eine
*  *memory_limit*  
* Einstellung von 30MB.
* PHP Einstellung
* \"
* session.auto_start
* \"
* sollte in der Datei php.ini deaktiviert sein
* \"
* OFF
* \"
* Wir empfehlen Datei-Uploads in PHP zu aktivieren
* Aktiviertes
*  *allow_url_fopen*  
* und
*  *fsockopen*  
* auf Port 80 möglich
* Apache Server Variablen
*  *REQUEST_URI*  
* oder
*  *SCRIPT_URI*  
* müssen vorhanden sein
* Der PHP 4 Kompatibilitätsmodus muss ausgeschaltet sein. (
*  *zend.ze1_compatibility_mode*  
* = Off)
*  *ini_set*  
* erlaubt
*  *register_globals*  
* ausgeschaltet
*  *magic_quotes_gpc*  
* ausgeschaltet
* PHP-Erweiterungen, die installiert sein müssen:
	*  *GD LIB*  
	* Version 2.x
	*  *MySQL* 
	*  *client connector*  
	* für MySQL 5
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
* Anzahl Kategorien 20% der Artikel z. B. 1.000 Artikel ~ 200 Kategorien
* Der Besucherstrom verteilt sich auf über 14 Std. pro Tag durchschnittlich
* Die Artikelanzahl beinhaltet auch mögliche Artikelvarianten
* Dennoch kann es bei manchen lastintensiven Tätigkeiten (z. B. Exporte) zu eingeschränkter Funktionalität kommen – dies ist abhängig von Ihrem Provider (Stichworte PHP max_execution_time und memory_limit).

.. Intern: ---, Status: