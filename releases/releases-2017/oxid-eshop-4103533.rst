OXID eShop 4.10.3/5.3.3
=======================

Versionsbezeichnung: 5.3.3 |br|
Edition: Enterprise Edition

Versionsbezeichnung: 4.10.3 |br|
Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 31.01.2017

----------

Allgemeines
-----------

Der Shop läuft unter PHP 5.3, 5.4, 5.5 und 5.6. Er ist kompatibel mit MySQL 5.7 und für Apache 2.2 and 2.4 angepasst. Haben Sie eine Enterprise Edition und MySQL 5.6 im Einsatz, beachten Sie bitte diesen Blog-Post: `Set MySQL 5.6 optimizer setting “block_nested_loop = off” for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_.

Eine Anleitung zum Update finden Sie unter :doc:`Update-Installation </installation/update/index>`.

----------

Verbesserungen und Anpassungen
------------------------------

Wegen einer Sicherheitslücke im PHPMailer wurde dieser auf die Version 5.2.22 aktualisiert. Details dazu finden Sie im englischsprachigen Blog-Post `PHPMailer < 5.2.21 Remote Code Execution: OXID eShop is safe! <https://oxidforge.org/en/phpmailer-5-2-21-remote-code-execution-oxid-eshop-is-safe.html>`_ auf der OXIDforge.

Eine Sicherheitslücke ist auch der Grund für die Aktualisierung des in der Professional und Enterprise Edition enthaltenen Visual CMS auf die Version 1.0.2.

Das Modul PAYONE, für das eine Korrektur notwendig wurde, liegt in der neuen Version 2.1.5 dem Installationspaket bei. Änderungen gegenüber der vorhergehenden Version können im Repository auf GitHub eingesehen werden: `https://github.com/PAYONE-GmbH/oxid-5/compare/v2.0.9...v2.1.5 <https://github.com/PAYONE-GmbH/oxid-5/compare/v2.0.9...v2.1.5>`_.

----------

Korrekturen
-----------

Mit diesem Patch wurde ein Bug im Modul PAYONE behoben: `https://bugs.oxid-esales.com/changelog_page.php?version_id=340 <https://bugs.oxid-esales.com/changelog_page.php?version_id=340>`_.

----------

Keine wichtigen Informationen für Entwickler zu diesem Release.

Änderungen gegenüber der vorhergehenden Version können im Repository der Community Edition auf GitHub eingesehen werden: `https://github.com/OXID-eSales/oxideshop_ce/compare/v4.10.2...v4.10.3 <https://github.com/OXID-eSales/oxideshop_ce/compare/v4.10.2...v4.10.3>`_.

.. Intern: oxaahw, Status: