OXID eShop 4.10.7/5.3.7
=======================

Versionsbezeichnung: 5.3.7 |br|
Edition: Enterprise Edition

Versionsbezeichnung: 4.10.7 |br|
Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 30.01.2018

----------

Allgemeines
-----------
Der Shop läuft unter PHP 5.3, 5.4, 5.5 und 5.6. Er ist kompatibel mit MySQL 5.7 und für Apache 2.2 and 2.4 angepasst. Haben Sie eine Enterprise Edition und MySQL 5.6 im Einsatz, beachten Sie bitte diesen Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_.

Mit OXID eShop 4.10.7/5.3.7 wird eine Sicherheitslücke geschlossen, die mit CVSS = 4.9 eingestuft wurde und nur in der Enterprise Edition mit Hochlastoption und aktivem Varnish auftritt. Details zur Sicherheitslücke finden Sie auf folgender Seite der OXIDforge: `Security Bulletin 2018-001 <https://oxidforge.org/en/security-bulletin-2018-001.html>`_. Wir empfehlen ein schnelles Update auf diese Shopversion. Eine Anleitung dazu finden Sie unter `Update-Installation <https://docs.oxid-esales.com/eshop/de/5.3/installation/update-installation/index.html>`_.

Es gab keine Änderungen in Templates für das Frontend und den Administrationsbereich sowie in den Sprachdateien.

----------

Verbesserungen
--------------
Mit OXID eShop 4.10.7/5.3.7 gab es Updates für folgende Erweiterungen:

* Visual CMS (PE/EE) wurde auf die Version 1.0.4 aktualiert.
* Das Modul Amazon Pay wurde auf die Version 2.5.1 aktualisiert.
* Das Modul PayPal wurde auf die Version 3.3.1 aktualisiert. Alle Änderungen finden Sie im Changelog: `<https://github.com/OXID-eSales/paypal/blob/v3.3.1/CHANGELOG.md>`_.

----------

Korrekturen
-----------
Es wurde die oben genannte Sicherheitslücke geschlossen. Darüber hinaus wurden mit diesem Patch keine Bugs behoben.

----------

Änderungen gegenüber der vorhergehenden Version können im Repository der Community Edition auf GitHub eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_ce/compare/v4.10.6...v4.10.7>`_.

.. Intern: oxaaic, Status: