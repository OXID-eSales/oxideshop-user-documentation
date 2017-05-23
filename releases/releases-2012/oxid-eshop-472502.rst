OXID eShop 4.7.2/5.0.2
======================
Versionsbezeichnung: 5.0.2, Revision 53018

Edition: Enterprise Edition

Versionsbezeichnung: 4.7.2, Revision 53018

Edition: Professional Edition und Community Edition

Veröffentlichungstermin: 18.12.2012

Allgemeines
-----------
Enterprise Edition: Das Caching mit Varnish Reverse Proxy wurde optimiert, um Antwortzeiten unter Hochlast weiter zu reduzieren. Seiten, die nicht gecached werden sollen, werden in Varnish als solche markiert. Die Anweisung ``set beresp.ttl = 300s;`` vor ``return(hit_for_pass);`` in \"oxSkipCacheRulesFetch\" der Konfigurationsdatei :file:`default.vlc` stellt sicher, dass Varnish eine markierte Seite 5 Minuten nicht im Cache sucht.

Mehr Informationen finden Sie hier: `https://www.varnish-cache.org/docs/3.0/reference/vcl.html <https://www.varnish-cache.org/docs/3.0/reference/vcl.html>`_ .

Verbesserungen und Anpassungen
------------------------------
In Version 4.7.2/5.0.2 gab es kleinere Änderungen in Sprachdateien des Administrationsbereichs und des Themes \"Azure\" sowie eine Änderung im Template :file:`article_stock.tpl` in :file:`/application/views/admin/tpl`.

Eine Übersicht aller Änderungen finden Sie in :file:`/templ_docu_admin/index.html` und :file:`/templ_docu_azure/index.html` des Installationspaketes.

Korrekturen
-----------
Alle mit diesem Patch behobenen Bugs sind in unserem Bugtrack-System aufgelistet: `https://bugs.oxid-esales.com/changelog_page.php?version_id=182 <https://bugs.oxid-esales.com/changelog_page.php?version_id=182>`_ .

.. Intern: oxaacx, Status: