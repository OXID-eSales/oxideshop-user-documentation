OXID eShop 4.9.5/5.2.5
**********************
Versionsbezeichnung: 5.2.5

Edition: Enterprise Edition

Versionsbezeichnung: 4.9.5

Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 28.07.2015

Allgemeines
-----------
Unterstützte PHP-Versionen
++++++++++++++++++++++++++
Der OXID eShop 4.9.5/5.2.5 läuft mit PHP 5.3, 5.4, 5.5 und 5.6.

Varnish ab Version 4.0.3 für Caching (Enterprise Edition)
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Varnish Version 3.0 wird nicht mehr länger unterstützt, da die Software bereits seit April 2015 den Status End Of Life (EOL) erreicht hat. Die jetzt ausgelieferte Datei :file:`default.vcl` enthält die Konfiguration für Varnish ab Version 4.0.3. Bitte setzen Sie nicht die Versionen 4.0.0, 4.0.1 und 4.0.2 ein, da diese Probleme in der Behandlung von Cookies hatten, die dazu führten, dass Artikel nicht in den Warenkorb gelegt und Kunden sich nicht an den Shop anmelden konnten.

Wenn dieses Verhalten in Ihrem Shop auftritt und Sie nicht auf die neueste Version von Varnish aktualisieren können, verwenden Sie den im Dokument `Reverse Proxy Varnish <de/support-services/dokumentation-und-hilfe/oxid-eshop/enterprise-edition/caching/reverse-proxy-varnish.html>`_ der Dokumentation zur Enterprise Edition beschriebenen Workaround.

OXID eFire Extension PayPal 3.2.2
+++++++++++++++++++++++++++++++++
Die OXID eFire Extension PayPal ist in der neuen Version 3.2.2 verfügbar, mit der zwei `Bugs <https://bugs.oxid-esales.com/changelog_page.php?version_id=275>`_ behoben wurden. Das Installationspaket enthält das Modul, das bei einem Update des OXID eShop separat aktualisiert werden muss.

Korrekturen
-----------
Alle mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet:

`https://bugs.oxid-esales.com/changelog_page.php?version_id=303 <https://bugs.oxid-esales.com/changelog_page.php?version_id=303>`_

Keine wichtigen Informationen für Entwickler zu diesem Release.

Änderungen gegenüber der vorhergehenden Version können im Repository der Community Edition auf `GitHub <https://github.com/OXID-eSales/oxideshop_ce/compare/v4.9.4...v4.9.5>`_ eingesehen werden.