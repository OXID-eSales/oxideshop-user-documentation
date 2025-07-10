:orphan:
System
======


Systeminfo im OXID eShop
------------------------

.. todo: #SB. Use case prüfen:

Prüfen Sie bei Problemen im Shop (z.B. Fehlermeldungen, Upload-Probleme, Datenbankverbindung) gezielt:

* Welche PHP-Version und Extensions aktiv sind
* Ob die erlaubten Dateitypen korrekt konfiguriert sind
* Welche Umgebungsvariablen und Server-Parameter gesetzt sind
* Ob alle Systemvoraussetzungen für Module oder Themes erfüllt sind

Die Systeminfo ist besonders hilfreich für Entwickler, Administratoren und Support, um bei Updates, Migrationen oder Supportanfragen schnell eine fundierte technische Grundlage zu haben.

Die Systeminfo im OXID eShop bietet eine umfassende Übersicht über alle wichtigen technischen Parameter und Umgebungsvariablen des Shopsystems. Diese Informationen sind essenziell für die Fehleranalyse, Systemwartung und die sichere Konfiguration des Shops.

Überblick über die Systeminfo-Bereiche
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Shop- und Datenbank-Konfiguration
   - Datenbank-Infos: Zeichensatz, Port, Treiberoptionen, Unix-Socket, Shop-Edition
   - Upload-Typen: Erlaubte Dateiformate (z.B. jpg, gif, png, pdf, mp3, avi)
   - Logging & Debug: Log-Level, Fehlerprotokollierung, SEO-Logging, Template-Debugging
   - Sonstiges: Session-Handling, Cookie-Domains/Pfade, erlaubte Roboter, Trusted IPs, Multishop-Felder

2. PHP-Konfiguration
   - PHP-Version und Betriebssystem
   - Build-Informationen, verwendete Konfigurationsdateien
   - Wichtige PHP-Direktiven: z.B. ``allow_url_fopen``, ``memory_limit``, ``upload_max_filesize``, ``post_max_size``, ``max_execution_time``, ``display_errors``
   - Geladene PHP-Module: z.B. bcmath, curl, gd, mysqli, openssl, pdo, soap, zip, mbstring, iconv
   - Sitzungsverwaltung: Einstellungen zu Sessions, Cookies, Garbage Collection, Upload-Progress

3. Server- und Umgebungseinstellungen
   - System-Variablen: Hostname, Benutzer, Pfade, Umgebungsvariablen, Server-Software (z.B. Apache-Version)
   - Server-API: FPM/FastCGI, Konfigurationspfade, zusätzliche ini-Dateien
   - Netzwerk: IP-Adressen, Ports, Protokolle, unterstützte Transports und Filter

4. Erweiterte PHP-Module & Features
   - Xdebug: Debug- und Profiler-Einstellungen, IDE-Key, Pfade, aktivierte Features
   - GDlib: Bildbearbeitungsfunktionen und unterstützte Formate
   - cURL: Version, unterstützte Protokolle und Features
   - OpenSSL: Version und unterstützte Verschlüsselungen
   - PDO: Unterstützte Datenbanktreiber

5. PHP- und Server-Variablen
   - Anzeige aller aktuellen Werte von ``$_REQUEST``, ``$_GET``, ``$_COOKIE``, ``$_SERVER``, ``$_ENV`` für Debugging und Fehlersuche

|procedure|

Um die Systeminfo anzuzeigen wählen Sie im Administrationsbereich :menuselection:`Service --> Systeminfo`.

Systemgesundheit
----------------

.. todo: #SB. Use case prüfen:

Stellen Sie sicher, dass der Shop stabil, sicher und performant läuft. Fehlende Voraussetzungen können zu Problemen oder Einschränkungen im Betrieb führen.

Bei der Systemgesundheit prüfen Sie, ob die wichtigsten technischen Voraussetzungen für den stabilen und sicheren Betrieb des OXID eShops erfüllt sind.


Prüfbereiche
^^^^^^^^^^^^

- **Server-Konfiguration**

  - Überprüfung, ob der Webserver (z.B. Apache) korrekt eingerichtet ist
  - Besonders wichtig: Aktiviertes ``mod_rewrite``-Modul für saubere URLs

- **Dateizugriffsrechte**

  - Kontrolle, ob der Shop die notwendigen Schreib- und Leserechte auf wichtige Dateien und Verzeichnisse besitzt

- **PHP-Konfiguration**

  - ``allow_url_fopen`` oder ``fsockopen`` auf Port 80 aktiviert
  - ``REQUEST_URI`` ist vorhanden
  - ``ini_set`` ist erlaubt
  - PHP Memory Limit: mindestens 32 MB, empfohlen 60 MB
  - UTF-8-Unterstützung
  - Datei-Uploads erlaubt (``file_uploads``)
  - ``session.auto_start`` ist ausgeschaltet

- **PHP-Erweiterungen**

  - ``DOM``
  - ``JSON``
  - ``ICONV``
  - ``Tokenizer``
  - ``PDO_MySQL``
  - ``GDlib v2`` (mit JPEG-Unterstützung)
  - ``mbstring``
  - ``cURL``
  - ``BCMath``
  - ``OpenSSL``
  - ``SOAP``

Bewertung der Prüfergebnisse
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- **Erfüllt:** Alle Anforderungen sind erfüllt.
- **Nicht oder nur teilweise erfüllt:** Der OXID eShop kann sich in Bereichen unerwartet verhalten.
- **Nicht erfüllt:** Der OXID eShop wird sich in einzelnen Bereichen unerwartet verhalten.
- **Konnte nicht überprüft werden:** Die Prüfung konnte für diesen Punkt nicht durchgeführt werden.

|procedure|

Um die Systemgesundheit anzuzeigen wählen Sie im Administrationsbereich :menuselection:`Service --> Systemgesundheit`.

OXID Diagnose
-------------

.. todo: #SB: Use case klären:

Dieses Modul sammelt technische Informationen über Ihren Shop und den Server.

Diese Informationen können vor einem Update, einer Modulinstallation oder zu Diagnosezwecken interessant sein.


|procedure|

Um die Diagnose zu starten, tun Sie folgendes:

1. Wählen Sie im Administrationsbereich unter :menuselection:`Service --> Diagnosewerkzeug`.
#. Legen Sie den Umfang fest.

   * :guilabel:`Module ermitteln`
   * :guilabel:`Systemgesundheit abfragen`
   * :guilabel:`PHP-Konfiguration (Auswahl) abfragen`
   * :guilabel:`Serverinformationen abfragen (sofern möglich)`

#. Wählen Sie :guilabel:`Diagnose starten`.

|result|

Das Ergebnis wird angezeigt und zum Herunterladen bereitgestellt.


SQL-Dateien importieren
-----------------------

.. todo: #SB: Use case klären:

Importieren Sie SQL-Dateien für Updates, Migrationen, Datenübernahmen, individuelle Anpassungen oder Backups.

Aktualisieren Sie Views nach dem Import einer SQL-Datei oder nach strukturellen Anpassungen an der Datenbank.

Durch das Neu-Generieren der Views werden Fehler wie fehlende Artikel, fehlerhafte Darstellungen oder unerwartete Shop-Probleme vermieden.

Diese Routine ist essenziell, um nach Datenbankänderungen die volle Funktionsfähigkeit und Datenkonsistenz im OXID eShop sicherzustellen.


|procedure|

Um eine SQL-Datei zu importieren, tun Sie folgendes:

1. Wählen Sie im Administrationsbereich unter :menuselection:`Service --> Tools`.
#. Laden Sie die SQL-Datei hoch.
#. Wählen Sie :guilabel:`Update starten`.
#. Um die Views zu aktualisieren, wählen Sie :guilabel:`Views etzt updaten`.


