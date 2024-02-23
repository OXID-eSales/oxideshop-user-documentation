OXID eShop 6.3.3
================

Veröffentlichungsdatum: 27.02.2024

-----------------------------------------------------------------------------------------

Installieren Sie OXID eShop 6.3.3, um eine Sicherheitslücke in Composer zu schließen.

OXID eShop 6.3.3 erfordert aus Sicherheitsgründen Composer Version 2.2.23.

Weitere Informationen finden Sie unter

* `Composer Version 2.2.23 <https://github.com/composer/composer/releases/tag/2.2.23>`_
* `CVE-2024-24821 <https://nvd.nist.gov/vuln/detail/CVE-2024-24821>`_

.. note::

   **Neue Nutzungsbedingungen der OXID eShop Community Edition (CE)**

   Beachten Sie, dass Sie mit Installieren von OXID eShop 6.3.3 den neuen Nutzungsbedingungen zustimmen, die seit dem 15.08.2022 gelten.

   Weitere Informationen finden Sie unter

   * `CE Lizenzbedingungen Update <https://www.oxid-esales.com/ce-lizenzbedingungen-update/>`_
   * `Auch für uns beginnt ein neues Zeitalter <https://www.oxid-esales.com/blog/auch-fuer-uns-beginnt-ein-neues-zeitalter/>`_


Allgemeines
-----------

OXID eShop 6.3.3 wird als Compilation bereitgestellt. Die Compilaton enthält unter anderen folgende Komponenten:

* OXID eShop CE 6.9.1
* OXID eShop PE 6.5.1
* OXID eShop EE 6.6.1
* Theme "Flow" 3.7.2
* Theme "Wave" 1.6.1
* Amazon Pay 3.6.8
* GDPR Opt-In 2.3.3
* Klarna 5.5.1
* OXID Cookie Management powered by usercentrics 1.1.3
* Paymorrow 2.1.0
* PAYONE 1.5.0
* PayPal 6.3.1
* WYSIWYG Editor + Mediathek 2.4.0
* Visual CMS 3.5.3 (PE/EE)


Verbesserungen und Anpassungen
------------------------------

.. todo: #HR: Welche neuen Versionen?

Sehen Sie sich die Änderungen an der Kompilierung im folgenden Metapackage an: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.3.2...v6.3.3>`_.

Folgende Komponente wurde auf eine neue Version aktualisiert:

.. todo: #HR: Welche neuen Versionen?

* OXID eShop CE (Update von 6.9.0 auf 6.9.1) `Changelog 6.9.1 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.9.1/CHANGELOG.md>`_

Änderungen gegenüber der vorhergehenden Version der Komponente OXID eShop CE können im Repository der Community Edition auf GitHub eingesehen werden: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.9.0...v6.9.1.
|br|
Wechseln Sie zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.


Systemvoraussetzungen
---------------------
OXID eShop 6.3.3 läuft unter PHP 8.0, 7.4 und 7.3.

Als Datenbank wird MySQL in der Version 5.5 oder 5.7 und MariaDB in der Version 10.4 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_.

Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

Composer wird in der Version 2.2.23 unterstützt.

Installation
------------
Für die Installation folgen Sie bitte den Anleitungen im Abschnitt "Installation":

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Update <../../installation/update/update>`

Führen Sie das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, aus. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.





.. Intern: , Status: