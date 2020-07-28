OXID eShop 6.2.0
================

Veröffentlichungstermin: 31.03.2020 |br|
Veröffentlichungstermin RC2: 26.02.2020 |br|
Veröffentlichungstermin RC1: 11.11.2019 |br|
Veröffentlichungstermin Beta 1: 02.08.2019

-----------------------------------------------------------------------------------------

Allgemeines
-----------
OXID eShop 6.2.0 wird als Compilation bereitgestellt. Diese enthält u.a. folgende Komponenten:

* OXID eShop CE 6.5.3
* OXID eShop PE 6.4.0
* OXID eShop EE 6.5.1
* Theme "Flow" 3.4.1
* Theme "Wave" 1.3.1
* Amazon Pay 3.6.4
* GDPR Opt-In 2.3.0
* Klarna 5.1.4
* Paymorrow 2.0.3
* PAYONE 1.3.1
* PayPal 6.1.0
* Summernote WYSIWIG-Editor und Mediathek 2.2.0
* Visual CMS (PE/EE) 3.3.3

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/b-6.1...b-6.2>`_.

OXID eShop 6.2.0 enthält eine Sicherheitsverbesserung im Zahlungsmodul PAYONE.

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
OXID eShop 6.2.0 läuft unter PHP 7.1 bis 7.4. Als Datenbank wird MySQL in der Version 5.5 oder 5.7 und MariaDB in der Version 10.4 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

Installation
^^^^^^^^^^^^
Die Neu-Installation und das Update von 6.1.x auf 6.2.0 werden im Abschnitt "Installation" beschrieben.

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Von 6.1.x auf 6.2.0 aktualisieren <../../installation/update/von-6.1.x-auf-6.2.0-aktualisieren>`

Bei der Installation wird das neue Verzeichnis :file:`/var` auf der gleichen Ebene wie :file:`/source` und :file:`/vendor` erstellt, auf welches der HTTP-Server und der CLI-Benutzer Lese- und Schreibzugriff benötigt.

Bitte führen Sie ein Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, aus. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

OXID eShop 6.0.* hat nun EOL (End of Life) erreicht und wird nicht mehr unterstützt. Bitte führen Sie ein Update aus, falls Sie noch einen Shop dieser Serie einsetzen.

-----------------------------------------------------------------------------------------

Neue Funktionen
---------------

Reverse Proxy NGINX
^^^^^^^^^^^^^^^^^^^
Die OXID eShop Hochlastoption ist ein Add-On für den OXID eShop Enterprise Edition in der Version 6. Mit Caching wird vor allem in Lastspitzen das schnelle Generieren und Ausliefern der HTML-Seiten sichergestellt. Das Caching übernimmt ein Reverse Proxy, der vor dem eigentlichen Webserver eingehende Anfragen von Web-Clients verarbeitet. Die OXID eShop Hochlastoption unterstützt jetzt NGINX Version 1.14.0 und höher als Reverse Proxy und bietet damit eine Alternativ zum bisher verwendeten Varnish.

OXID eShop console
^^^^^^^^^^^^^^^^^^
OXID eShop 6.2.0 nutzt die `Symfony Console <https://symfony.com/doc/current/console.html>`_. Mit dieser können Entwickler eigene Kommandos für Komponenten und Module schreiben, registrieren und ausführen. Informationen dazu sind in der englischsprachigen Entwicklerdokumentation zu finden: https://docs.oxid-esales.com/developer/en/6.2/development/tell_me_about/console.html.

Template Engine Twig
^^^^^^^^^^^^^^^^^^^^
OXID eShop unterstützt `Twig <https://twig.symfony.com>`_, ein Symfony Project, als alternative Template Engine. Entwickler können entscheiden, ob sie Twig anstelle von Smarty in den Templates verwenden möchten. Für die Umstellung von Smarty auf Twig werden Tools zur Verfügung gestellt.

Dependency Injection
^^^^^^^^^^^^^^^^^^^^
Dependency Injection (DI), ein Entwurfsmuster in der objektorientierten Programmierung, kann jetzt in Modulen genutzt werden.
Implementiert wird DI innerhalb von OXID eShop mit Hilfe des Symfony DI containers. Dependency Injection bedeutet verkürzt und zusammengefasst, dass ein Objekt, welches die Funktionalität eines anderen Objektes benötigt, dieses nicht selbst instantiieren darf. Das Objekt wird von außen injiziert. Was Depency Injection für Projektentwickler bedeutet, wird in einem dreiteiligen Beitrag unseres neuen Corporate Blogs vorgestellt: `Teil 1: die Grundlagen <https://www.oxid-esales.com/blog/dependency-injection-fuer-projektentwickler-in-oxid/>`_, `Teil 2: DI innerhalb von Modulen <https://www.oxid-esales.com/blog/dependency-injection-innerhalb-von-oxid-modulen/>`_ und `Teil 3: Erweiterung der Shop-Logik mit Hilfe des Symfony DI containers <https://www.oxid-esales.com/blog/erweiterung-des-oxid-eshops-mit-hilfe-des-symfony-di-containers/>`_.

Events
^^^^^^
Mit OXID eShop 6.2.0 wird ein Eventhandling eingeführt, welches auf `Symfony Events and Event Listeners <https://symfony.com/doc/3.4/event_dispatcher.html>`_ basiert. Erste Events, die implementiert wurden, erlauben einen verlässlicheren Weg, die Funktionalität des Shops zu erweitern. Events sind die bessere Alternative zur traditionellen Vererbung innerhalb der Klassenkette. Sie können vom Shop und von Modulen verarbeitet werden. Die englischsprachigen Entwicklerdokumentation enthält eine Einführung zum Eventhandling und eine Übersicht der aktuell verfügbaren Events: https://docs.oxid-esales.com/developer/en/6.2/development/tell_me_about/event/index.html.

Doctrine SQL Query Builder
^^^^^^^^^^^^^^^^^^^^^^^^^^
Der `Doctrine SQL Query Builder <https://www.doctrine-project.org/projects/doctrine-dbal/en/2.5/reference/query-builder.html#sql-query-builder>`_ kann jetzt auch in Modulen genutzt werden. Eine Anleitung für eine Datenbankabfrage ist ebenfalls in der Entwicklerdokumentation zu finden: https://docs.oxid-esales.com/developer/en/6.2/development/modules_components_themes/module/using_database.html#making-a-query.

.. _new-codeception:

Codeception
^^^^^^^^^^^
Für den OXID eShop werden `Codeception acceptance tests <https://codeception.com>`_ eingeführt, die für das Schreiben von Acceptance Tests für Module der Themes "Flow" und "Wave" empfohlen werden. Für die Entwickler sind diese Tests einfacher zu schreiben, zu verwenden und zu warten. Ein weiterer Vorteil ist, dass neuere Treiber unterstützt werden. Ausführliche Informationen sind in der englischsprachigen Entwicklerdokumentation zu finden: https://docs.oxid-esales.com/developer/en/6.2/development/modules_components_themes/module/testing/codeception/index.html.

Neues Verzeichnis /var
^^^^^^^^^^^^^^^^^^^^^^
Der Shop hat nun das neue Verzeichnis :file:`/var` auf der gleichen Ebene wie :file:`/source` und :file:`/vendor`. Es nimmt, durch Unterverzeichnisse strukturiert, die Modulkonfigurationen auf. Diese werden pro Subshop (bei einer Enterprise Edition) und umgebungsspezifisch (Produktion, Staging, Entwicklung) in .yaml-Dateien gespeichert. Das Verzeichnis benötigt bei der Installation und zur Laufzeit rekursiv Lese- und Schreibzugriff für HTTP-Server und CLI-Benutzer.

Benutzerdefinierte Shop offline-Seite
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Der Shop kann eine benutzerdefinierte Shop offline-Seite mit angepasstem Layout und/oder speziellen Funktionen anstatt der Standardseite, die auf Wartungsarbeiten hinweist, anzeigen. Dies kann durch Überschreiben der Methode ``oxTriggerOfflinePageDisplay`` erreicht werden.

Zeichensatz der Datenbankverbindung
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In der Konfigurationsdatei :file:`config.inc.php` kann der Zeichensatz der Datenbankverbindung durch einen neuen Parameter festgelegt werden. Beispiel: ``$this->dbCharset = 'utf8';``

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------

Aktualisierte Komponenten der OXID eShop Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Folgende Komponenten wurden auf eine neue Version aktualisiert:

* OXID eShop CE (Update von 6.3.6 auf 6.5.3), `Changelog 6.5.3 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.5.3/CHANGELOG.md>`_
* OXID eShop PE (Update von 6.2.2 auf 6.4.0)
* OXID eShop EE (Update von 6.2.3 auf 6.5.1)
* Theme "Flow" (Update von 3.3.0 auf 3.4.1), `Changelog 3.4.1 <https://github.com/OXID-eSales/flow_theme/blob/v3.4.1/CHANGELOG.md>`_
* Theme "Wave" (Update von 1.2.0 auf 1.3.1), `Changelog 1.3.1 <https://github.com/OXID-eSales/wave-theme/blob/v1.3.1/CHANGELOG.md>`_
* Amazon Pay (Update von 3.3.1 auf 3.6.4), `Changelog 3.6.4 <https://github.com/bestit/amazon-pay-oxid/blob/3.6.4/CHANGELOG.md>`_
* GDPR Opt-In (Update von 2.2.0 auf 2.3.0), `Changelog 2.3.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.0/CHANGELOG.md>`_
* Klarna (Update von 4.3.0 auf 5.1.4), `Changelog 5.1.4 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.1.4/CHANGELOG.md>`_
* Paymorrow (Update von 2.0.1 auf 2.0.3), `Changelog 2.0.3 <https://github.com/OXID-eSales/paymorrow-module/blob/v2.0.3/CHANGELOG.md>`_
* PAYONE (Update von 1.0.10 auf 1.3.1), `Changelog v1.3.1 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.3.1/Changelog.txt>`_
* PayPal (Update von 5.2.5 auf 6.1.0), `Changelog 6.1.0 <https://github.com/OXID-eSales/paypal/blob/v6.1.0/CHANGELOG.md>`_
* Visual CMS (PE/EE) (Update von 3.3.2 auf 3.3.3)

Sortierung von Zubehör für Artikel
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Im Zuordnungsfenster für das Zubehör lässt sich die Reihenfolge der zugeordneten Artikel ändern. Nachdem ein Artikel in der rechten Liste markiert wurde, kann dieser mit den jetzt angezeigten Minischaltflächen nach oben oder unten verschoben werden.

Änderungen im Modulsystem
^^^^^^^^^^^^^^^^^^^^^^^^^
Heute ist es in größeren und mittleren Projekten Standard, den OXID eShop in verschiedenen Umgebungen wie Integration, Staging und Produktion zu betreiben. Um Module einfach zu konfigurieren, anstatt sie in jeder Umgebung separat zu verwalten, wurde das Modulsystem entsprechend erweitert. Es ist nun möglich, die Umgebung über YAML-Konfigurationsdateien zu verwalten. Diese werden im neuen Verzeichnis :file:`/var` und seinen strukturierten Unterverzeichnissen gespeichert. Detaillierte Informationen dazu finden Sie in der englischsprachigen Entwicklerdokumentation: https://docs.oxid-esales.com/developer/en/6.2/development/modules_components_themes/project/module_configuration/modules_configuration.html#configuring-module-20190910

Die Datei :file:`metadata.php` wird strikter validiert. Die Versionsangabe ist jetzt verpflichtend und zusätzlicher Quellcode ist nicht gestattet.

Änderungen im Testing-Framework
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Es gab eine Reihe von Änderungen im Testing-Framework.

* Die PHPUnit Komponente wurde von Version 4.8.26 auf 6 aktualisiert. Informationen zu hinzugefügten, geänderten und entfernten Methoden sind in den Changelogs der PHPUnit zu finden: https://github.com/sebastianbergmann/phpunit/blob/6.0.0/ChangeLog-6.0.md und https://github.com/sebastianbergmann/phpunit/blob/6.0.0/ChangeLog-5.0.md.
* Für das einfachere Schreiben von Acceptance Tests wurde Codeception eingeführt, worauf im Abschnitt "Neue Funktionen" bereits eingegangen wurde, siehe: :ref:`new-codeception`.
* Änderungen in der OXID eShop testing library sind im Changelog dokumentiert: https://github.com/OXID-eSales/testing_library/blob/v7.1.0/CHANGELOG.md.

Ausführliche Information zum Testen von Modulen hält die englischsprachige Entwicklerdokumentation bereit: https://docs.oxid-esales.com/developer/en/6.2/development/modules_components_themes/module/testing/index.html.

Übersicht aller Änderungen
^^^^^^^^^^^^^^^^^^^^^^^^^^
Änderungen gegenüber den vorhergehenden Versionen der Komponente OXID eShop können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.3.6…v6.5.3. Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

-----------------------------------------------------------------------------------------

Korrekturen
-----------

Korrekturen 6.2.0: https://bugs.oxid-esales.com/changelog_page.php?version_id=542 |br|
Korrekturen 6.2.0 RC 1: https://bugs.oxid-esales.com/changelog_page.php?version_id=529 |br|
Korrekturen 6.2.0 Beta 1: https://bugs.oxid-esales.com/changelog_page.php?version_id=459


.. Intern: oxbais, Status:
