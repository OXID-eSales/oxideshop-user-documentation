OXID eShop 4.10.3/5.3.3
=======================
Versionsbezeichnung: 5.3.3

Edition: Enterprise Edition

Versionsbezeichnung: 4.10.3

Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 31.01.2017

Allgemeines
-----------
Der Shop läuft unter PHP 5.3, 5.4, 5.5 und 5.6. Er ist kompatibel mit MySQL 5.7 und für Apache 2.2 and 2.4 angepasst. Haben Sie eine Enterprise Edition und MySQL 5.6 im Einsatz, beachten Sie bitte diesen `Blog-Post <http://planet.oxidforge.org/2015/11/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_ (in englischer Sprache).

Eine Anleitung zum Update finden Sie unter `http://doku.oxid-esales.com/oxid-eshop/installation/oxid-eshop-aktualisieren.html <de/support-services/dokumentation-und-hilfe/oxid-eshop/installation/oxid-eshop-aktualisieren/update-vorbereiten.html>`_ .

Verbesserungen und Anpassungen
------------------------------
Wegen einer Sicherheitslücke im PHPMailer wurde dieser auf die Version 5.2.22 aktualisiert. Details dazu finden Sie in einem englischsprachigen `Blogpost <https://oxidforge.org/en/phpmailer-5-2-21-remote-code-execution-oxid-eshop-is-safe.html>`_ auf der OXIDforge.

Eine Sicherheitslücke ist auch der Grund für die Aktualisierung des in der Professional und Enterprise Edition enthaltenen Visual CMS auf die Version 1.0.2.

Das Modul PAYONE, für das eine Korrektur notwendig wurde, liegt in der neuen Version 2.1.5 dem Installationspaket bei. Änderungen gegenüber der vorhergehenden Version können im Repository auf `GitHub <https://github.com/PAYONE-GmbH/oxid-5/compare/v2.0.9...v2.1.5>`_ eingesehen werden.

Korrekturen
-----------
Mit diesem Patch wurde ein Bug im Modul PAYONE behoben.

`https://bugs.oxid-esales.com/changelog_page.php?version_id=340 <https://bugs.oxid-esales.com/changelog_page.php?version_id=340>`_

Keine wichtigen Informationen für Entwickler zu diesem Release.

Änderungen gegenüber der vorhergehenden Version können im Repository der Community Edition auf `GitHub <https://github.com/OXID-eSales/oxideshop_ce/compare/v4.10.2...v4.10.3>`_ eingesehen werden.

.. Intern: oxaahw, Status: