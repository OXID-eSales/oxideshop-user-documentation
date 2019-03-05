OXID eShop 6.0.3
================

Veröffentlichungstermin: 31.07.2018

-----------------------------------------------------------------------------------------

Allgemeines
-----------
Der OXID eShop 6.0.3 wird als Compilation bereitgestellt. Diese enthält folgende Komponenten:

* OXID eShop 6.2.1
* Theme "Flow" 3.0.0
* AmazonPay 3.1.4
* GDPR Opt-In 2.1.1
* Klarna 4.0.1
* Paymorrow 2.0.1
* PAYONE 1.0.8
* PayPal 5.2.2
* Visual CMS 3.2.1 (PE/EE)
* WYSIWIG-Editor und die Mediathek Summernote 2.1.1

Alle Änderungen in der Compilation können im Metapackage eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.0.2…v6.0.3>`_.

Mit OXID eShop 6.0.3 wurden zwei Sicherheitslücken geschlossen. Eine der beiden Sicherheitslücken ist nur dann relevant, wenn im Shop die Zahlungsart Paymorrow aktiv genutzt wird. Details zu beiden Sicherheitslücken finden Sie auf folgenden Seiten der OXIDforge: `Security Bulletin 2018-002 <https://oxidforge.org/en/security-bulletin-2018-002.html>`_ und `Security Bulletin 2018-003 <https://oxidforge.org/en/security-bulletin-2018-002.html>`_. Wir empfehlen ein schnelles Update auf diese Shopversion (6.0.3) und auf das ausgelieferte Modul Paymorrow 2.0.1. Eine Anleitung zum Shop-Update finden Sie unter :doc:`Update-Installation <../../installation/update-installation/index>`.


Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^
Der OXID eShop 6.0.3 läuft unter PHP 5.6 oder 7.0. Als Datenbank wird MySQL in der Version 5.5 oder 5.7 unterstützt. Der Einsatz von MySQL 5.6 wird nicht empfohlen, da es Probleme mit einer Enterprise Edition geben könnte. Beachten Sie dazu bitte den Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Als Webserver kann Apache 2.2 oder 2.4 auf einem Linux-System eingesetzt werden.

Installation
^^^^^^^^^^^^
Für die Installation, folgen Sie bitte den Anleitungen im Abschnitt "Installation":

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Update-Installation <../../installation/update-installation/update-installation>`

Bitte führen Sie das Update erst in einer Test- oder Entwicklungsumgebung, einer Kopie Ihres aktuellen Shops, aus. Testen Sie anschließend den Bestellprozess sowie Zahlungs- und Versandarten. Arbeitet der Shop korrekt, kann der Shop im Live-System durch den aus der Test- oder Entwicklungsumgebung ersetzt werden.

-----------------------------------------------------------------------------------------

Neue Funktionen
---------------

Neue Komponenten der OXID eShop Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Die OXID eShop Compilation wurde durch die Module GDPR Opt-in 2.1.1 und Klarna 4.0.1 erweitert. Das Modul GDPR Opt-in stellt Opt-in-Funktionen bereit, welche der OXID eShop für die Umsetzung der Datenschutz-Grundverordnung (DSGVO) benötigt. Mit dem Modul Klarna wird ein weiteres Zahlungsmodul ausgeliefert, mit dem Shopbetreiber beispielsweise Zahlungen auf Rechnung, per Ratenkauf oder per Sofortüberweisung über den Finanzdienstleister Klarna abwickeln können.

-----------------------------------------------------------------------------------------

Verbesserungen und Anpassungen
------------------------------

Aktualisierte Komponenten der OXID eShop Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Folgende Komponenten wurden auf eine neue Version aktualisiert:

* OXID eShop (Update von 6.2.0 auf 6.2.1), `Changelog 6.2.1 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.2.1/CHANGELOG.md>`_
* AmazonPay (Update von 3.0.2 auf 3.1.4)
* Paymorrow (Update von 2.0.0 auf 2.0.1), `Changelog 2.0.1 <https://github.com/OXID-eSales/paymorrow-module/blob/v2.0.1/CHANGELOG.md>`_
* PAYONE (Update von 1.0.5 auf 1.0.8), `Changelog 1.0.8 <https://github.com/PAYONE-GmbH/oxid-6/blob/1.0.8/Changelog.txt>`_
* PayPal (Update von 5.1.6 auf 5.2.2), `Changelog 5.2.2 <https://github.com/OXID-eSales/paypal/blob/v5.2.2/CHANGELOG.md>`_
* Visual CMS (PE/EE, Update von 3.2.0 auf 3.2.1), `Changelog 3.2.1 <https://github.com/OXID-eSales/visual_cms_module/blob/v3.2.1/CHANGELOG.md>`_

Wechseln Sie jeweils zur Registerkarte :guilabel:`Files changed`, um die Liste aller geänderten Dateien aufzurufen.

-----------------------------------------------------------------------------------------

Korrekturen
-----------
Es wurden die oben genannten Sicherheitslücken geschlossen. Darüber hinaus sind die mit diesem Patch behobenen Bugs in unserem Bugtrack-System aufgelistet.

`<https://bugs.oxid-esales.com/changelog_page.php?version_id=433>`_

.. Intern: oxbaij, Status: