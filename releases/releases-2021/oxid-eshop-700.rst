OXID eShop 7.0.0
================

Veröffentlichungstermin RC 1: xx.07.2021


https://docs.oxid-esales.com/eshop/de/6.0/releases/releases-2017/oxid-eshop-600.html


-----------------------------------------------------------------------------------------

Allgemeines
-----------
ToDo: Komponenten und ihre aktuellen Versionen |br|
OXID eShop 7.0.0 wird als Compilation bereitgestellt. Diese enthält u.a. folgende Komponenten:

* OXID eShop CE (vorher 6.8.0)
* OXID eShop (vorher PE 6.5.0)
* OXID eShop (vorher EE 6.6.0)
* Theme "Flow" (vorher 3.7.0)
* Theme "Wave" (vorher 1.6.0)
* Amazon Pay (vorher 3.6.8)
* GDPR Opt-In (vorher 2.3.3)
* Klarna (vorher 5.5.0)
* OXID Cookie Management powered by usercentrics (vorher 1.1.3)
* Paymorrow (vorher 2.0.4)
* PAYONE (vorher 1.3.1)
* PayPal (vorher 6.2.3)
* WYSIWYG Editor + Mediathek (vorher 2.4.0)
* Visual CMS (vorher 3.5.3) (PE/EE)

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
ToDo: unterstützte PHP-Versionen |br|
OXID eShop 7.0.0 läuft unter PHP 8.0, 7.4 und 7.3.

ToDo: unterstützte Datenbanken und ihre Versionen |br|
Als Datenbank wird MySQL in der Version 5.5 oder 5.7 und MariaDB in der Version 10.4 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_.

ToDo: unterstützte Webserver und Versionen |br|
Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

ToDo: Composer 1 noch unterstützt? |br|
Composer wird in den Versionen 1 und 2 unterstützt.

Installation
^^^^^^^^^^^^
Für die Installation, folgen Sie bitte den Anleitungen im Abschnitt "Installation":

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Update <../../installation/update/update>`

Bitte führen Sie das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, aus. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

-----------------------------------------------------------------------------------------

Neue Funktionen
---------------
Setup per Kommandozeile
^^^^^^^^^^^^^^^^^^^^^^^
Als Ergänzung zum webbasierten Setup kann OXID eShop jetzt auch über die Kommandozeile erstellt und konfiguriert werden. Das neue Kommando der OXID eShop console ``oe:setup:shop``erstellt die Datenbank und konfiguriert den Shop. Die dafür notwendigen Informationen werden mit Parametern übergeben. In einem zweiten Schritt wird mit ``oe:admin:create-user`` der Shop-Administrator erstellt. Siehe: :doc:`Setup per Kommandozeile <../../installation/neu-installation/setup-kommandozeile>`

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------
Kreditkarte als Zahlungsart nicht mehr unterstützt
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Beschreibung hier

Newsletter-Versand entfernt
^^^^^^^^^^^^^^^^^^^^^^^^^^^
Beschreibung hier

Nachrichten entfernt
^^^^^^^^^^^^^^^^^^^^
Beschreibung hier







-----------------------------------------------------------------------------------------

Korrekturen
-----------
ToDo: Text hier

.. Intern: , Status: