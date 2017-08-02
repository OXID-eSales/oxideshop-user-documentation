OXID eShop 4.9.10/5.2.10
========================

Versionsbezeichnung: 5.2.10 |br|
Edition: Enterprise Edition

Versionsbezeichnung: 4.9.10 |br|
Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 08.08.2017

----------

Allgemeines
-----------
Der Shop läuft unter PHP 5.3, 5.4, 5.5 und 5.6. Er ist kompatibel mit MySQL 5.7 und für Apache 2.2 and 2.4 angepasst. Haben Sie eine Enterprise Edition und MySQL 5.6 im Einsatz, beachten Sie bitte diesen Blog-Post: `Set MySQL 5.6 optimizer setting “block_nested_loop = off” for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_.

Mit diesem Patch-Release wurde eine Sicherheitslücke geschlossen, die mit CVSS = 2.2 eingestuft wurde. Detailliertere Informationen dazu werden in Kürze mit dem Security Bulletin 2017-001 veröffentlicht. Wir empfehlen ein schnelles Update auf diese Shopversion. Eine Anleitung dazu finden Sie unter :doc:`Update-Installation </installation/update-installation/index>`.

Es gab keine Änderungen in Templates für das Frontend und den Administrationsbereich sowie in den Sprachdateien.

----------

Verbesserungen und Anpassungen
------------------------------
Wegen einer Sicherheitslücke im PHPMailer wurde dieser auf die Version 5.2.22 aktualisiert. Details dazu finden Sie im englischsprachigen Blog-Post `PHPMailer < 5.2.21 Remote Code Execution: OXID eShop is safe! <https://oxidforge.org/en/phpmailer-5-2-21-remote-code-execution-oxid-eshop-is-safe.html>`_ auf der OXIDforge.

----------

Korrekturen
-----------
Die mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet:

`https://bugs.oxid-esales.com/changelog_page.php?version_id=324 <https://bugs.oxid-esales.com/changelog_page.php?version_id=324>`_

----------

Keine wichtigen Informationen für Entwickler zu diesem Release.

Änderungen gegenüber der vorhergehenden Version können im Repository der Community Edition auf GitHub eingesehen werden: `https://github.com/OXID-eSales/oxideshop_ce/compare/v4.9.9...v4.9.10 <https://github.com/OXID-eSales/oxideshop_ce/compare/v4.9.9...v4.9.10>`_.

.. Intern: oxaahz, Status: