OXID eShop 4.10.8/5.3.8
=======================

Versionsbezeichnung: 5.3.8 |br|
Edition: Enterprise Edition

Versionsbezeichnung: 4.10.8 |br|
Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 31.07.2018

----------

Allgemeines
-----------
Der Shop läuft unter PHP 5.3, 5.4, 5.5 und 5.6. Er ist kompatibel mit MySQL 5.7 und für Apache 2.2 and 2.4 angepasst. Haben Sie eine Enterprise Edition und MySQL 5.6 im Einsatz, beachten Sie bitte diesen Blog-Post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_.

Mit OXID eShop 4.10.8/5.3.8 wurden zwei Sicherheitslücken geschlossen. Eine der beiden Sicherheitslücken ist nur dann relevant, wenn im Shop die Zahlungsart Paymorrow aktiv genutzt wird. Details zu beiden Sicherheitslücken finden Sie auf folgenden Seiten der OXIDforge: `Security Bulletin 2018-002 <https://oxidforge.org/en/security-bulletin-2018-002.html>`_ und `Security Bulletin 2018-003 <https://oxidforge.org/en/security-bulletin-2018-002.html>`_. Wir empfehlen ein schnelles Update auf diese Shopversion (PE und CE 4.10.8 bzw. EE 5.3.8) und auf das mitgelieferte Modul Paymorrow 1.0.2. Eine Anleitung zum Shop-Update finden Sie unter :doc:`Update-Installation <../../installation/update-installation/index>`.

OXID eShop 4.10.8/5.3.8 wird mit folgenden Modulen ausgeliefert:

* Amazon Pay 2.5.1
* Paymorrow 1.0.2
* PAYONE 2.1.6
* PayPal 3.3.1
* Visual CMS 1.0.4 (PE/EE)

Es gab keine Änderungen in Templates für das Frontend und den Administrationsbereich, aber kleine Korrekturen in den Sprachdateien.

.. important:: OXID eShop 4.10.*/5.3.* hat nun End of Life (EOL) erreicht und wird nicht mehr unterstützt. Bitte führen Sie ein Update aus, falls Sie noch einen Shop dieser Serie einsetzen.

----------

Korrekturen
-----------
Es wurden die oben genannten Sicherheitslücken geschlossen. Darüber hinaus wurden mit diesem Patch keine Bugs behoben.

----------

Änderungen gegenüber der vorhergehenden Version können im Repository der Community Edition auf GitHub eingesehen werden: `<https://github.com/OXID-eSales/oxideshop_ce/compare/v4.10.7...v4.10.8>`_.

.. Intern: oxaaic, Status: