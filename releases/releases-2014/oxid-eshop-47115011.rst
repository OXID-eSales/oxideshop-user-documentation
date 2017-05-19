OXID eShop 4.7.11/5.0.11
************************
Versionsbezeichnung: 5.0.11, Revision d89d0f353fce5dbe62b4ce26a805eedc02d77976

Edition: Enterprise Edition

Versionsbezeichnung: 4.7.11, Revision d89d0f353fce5dbe62b4ce26a805eedc02d77976

Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 25.02.2014

Allgemeines
-----------
Der OXID eShop 4.7.11/5.0.11 enthält zwei Security Fixes. Es wird dringend empfohlen, diesen Patch so schnell wie möglich in Ihr Live-System zu übernehmen. Die beiden englischsprachigen Security Bulletins `2014-001 <http://wiki.oxidforge.org/Security_bulletins/2014-001>`_ und `2014-002 <http://wiki.oxidforge.org/Security_bulletins/2014-002>`_ , welche die Sicherheitsprobleme beschreiben, wurden am 11.03.2014 veröffentlicht.

Neue Funktionen
---------------
In der Konfigurationsdatei :file:`config.inc.php` kann mit ``$this-->blDoNotDisableModuleOnError`` definiert werden, ob ein Modul deaktiviert werden soll, wenn eine zugehörige Klasse im Modulverzeichnis nicht gefunden wird. Standardmäßig wird das Modul deaktiviert.

Verbesserungen und Anpassungen
------------------------------
Die automatisch erstellten Installationspakete für die kumulativen Updates weisen diesmal eine Besonderheit auf: im Header der Dateien wurden SVN-Kommentare entfernt. Aus diesem Grund enthält der Ordner :file:`/copy_this` sehr viele geänderte Dateien. Auch im Ordner :file:`/changed_full` gibt es einige Dateien, bei denen nur diese Kommentarzeilen entfernt wurden. Sprachdateien des Administrationsbereiches und des Themes \"Azure\" der Version 4.7.11/5.0.11 wurden aus dem genannten Grund geändert. Eine Übersicht aller Änderungen finden Sie in :file:`/templ_docu_azure/index.html` und :file:`/templ_docu_admin/index.html`. Bitte achten Sie auch auf die Ergänzung in der Datei :file:`config.inc.php`.

Wir bitten, die Unannehmlichkeiten beim Update zu entschuldigen.

Korrekturen
-----------
Alle mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet:

`https://bugs.oxid-esales.com/changelog_page.php?version_id=247 <https://bugs.oxid-esales.com/changelog_page.php?version_id=247>`_

Hinweise für Entwickler

Bug #5625: Die Lösung für diesen Bug (Datenbank-Handling, Views und Anzahl von Sprachen pro Shop) kann Einfluss auf Module haben, welche die MethodeoxLang::getLanguageIds` überschreiben. Bitte beachten Sie die Anmerkungen zum Bug: `https://bugs.oxid-esales.com/view.php?id=5625 <https://bugs.oxid-esales.com/view.php?id=5625>`_ .

.. Intern: oxaaer, Status: