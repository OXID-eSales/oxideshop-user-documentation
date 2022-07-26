OXID eShop 6.5.0
================

Veröffentlichungstermin: 02.08.2022

OXID eShop 6.5.0

* behebt Bugs
  |br|
  Siehe :ref:`releases/releases-65/oxid-eshop-650:Korrekturen`.
* unterstützt PHP 8.1
  |br|
  Siehe unter :ref:`installation/neu-installation/server-und-systemvoraussetzungen:Server und Systemvoraussetzungen` Abschnitt :ref:`installation/neu-installation/server-und-systemvoraussetzungen:PHP`.
* verwendet Symfony 5.4 statt Symfony 3.4
  |br|
  Hintergrund: Symfony 3.4 wird nicht mehr mit (Sicherheits-) Updates unterstützt und ist nicht mit PHP 8.1 kompatibel.

  .. attention::

     **Breaking Changes**

     Prüfen Sie, ob Sie alle Module in OXID eShop 6.5 weiter verwenden können.

     * Drittanbieter-Module

       Wenn Sie Drittanbieter-Module verwenden, ragen Sie die Hersteller, ob sie mit Symfony 5.4 und PHP 8.1 kompatibel sind.

     * Amazon Pay

       :productname:`Amazon Pay` wird nicht mehr von OXID eShop unterstützt.

       Hintergrund: :productname:`Amazon Pay` wird durch das neue Modul :productname:`Amazon Pay für OXID` ersetzt.

       Machen Sie kein Update auf OXID eShop 6.5, wenn Sie Amazon Pay verwenden.
       |br|
       Wenn Sie Amazon Pay verwenden, müssen Sie  :productname:`Amazon Pay` und :productname:`Amazon Pay für OXID` vorübergehend im parallel betreiben, bevor Sie das Update auf OXID eShop 6.5 machen können.
       |br|
       Der Parallelbetrieb ist so lange nötig, bis alle alten Bestellungen abgeschlossen sind, die mit :productname:`Amazon Pay` erfolgt sind.
       |br|
       Tun Sie Folgendes:

       1. Wenn Sie OXID 6.1 oder früher haben, machen Sie ein Update auf OXID eShop Version 6.2 oder 6.3.
          |br|
          Hintergrund: Der Parallelbetrieb nur in in den Versionen OXID 6.2 und OXID 6.3 möglich.

          .. todo: #ML klären: Aussage falsch: "Installieren Sie Amazon Pay für den OXID eShop ab Version 6.1." ?
          .. todo: #VL klärt, ob das alte Amazon noch mit OXID *6.4* kompatibel war? Mario ist sich nicht sicher, evtl. war es nur bis 6.3 kompatibel.

       #. Installieren und konfigurieren Sie :productname:`Amazon Pay für OXID`.
          |br|
          Weitere Informationen finden Sie unter https://docs.oxid-esales.com/modules/amazon-pay/de/latest/installation.html.
       #. Planen Sie eine Downtime für Ihren OXID eShop ein und tun Sie Folgendes:

          * Schalten Sie :productname:`Amazon Pay für OXID` für den Live-Betrieb frei.
          * Deaktivieren Sie alle Zahlungsarten, die zu :productname:`Amazon Pay` gehören.

          Resultat: Ihre Kunden wickeln künftige Zahlungen mit :productname:`Amazon Pay für OXID` ab. Zahlungen für alte Bestellungen können Sie weiterhin mit :productname:`Amazon Pay` überwachen.
       #. Sobald alle alten Bestellungen abgewickelt sind, führen Sie das Update auf OXID eShop 6.5 durch.


.. todo: #VL: Symfony 5.4: als Requirement bisher nie erwähnt, wird es nicht mit Composer installiert? Warum erwähnenswert? -- Vorteil: 3.4 nicht mehr supported; nicht mit PHP 8.1 kompatibel 3.4 auf 5.4 bc break: evtl. Module zu aktualisieren: Drittanbieter frgen
.. todo: #VL: Welchen Vorteil hat PHP 8.1? -- einfach nur neueste Version;

Verbesserungen und Anpassungen
------------------------------

.. todo: #VL: There isn’t anything to compare. -- erst mit Release?

Sehen Sie Änderungen in der Compilation im Metapackage ein: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.4.3…v6.5.0>`_.

Folgende Komponente können Sie in OXID eShop nicht mehr verwenden:

* Amazon Pay 3.6.8 `Changelog 3.6.8 <https://github.com/OXID-eSales/amazon-pay-oxid/blob/3.6.8/CHANGELOG.md>`_

Hintergrund: Wir ersetzen Amazon Pay 3.6.8 durch Ammazon Pay für OXID Version 1.

Folgende Komponenten wurden aktualisiert oder sind neu hinzugekommen:

.. todo: #VL: Verifizieren: weitere Komponenten aktualisiert?
.. todo: #VL: Ist Makaira oxid-connect richtig?
.. todo: #VL: Fliegt das alte Amazon-Modul raus? * Amazon Pay 3.6.8 `Changelog 3.6.8 <https://github.com/OXID-eSales/amazon-pay-oxid/blob/3.6.8/CHANGELOG.md>`_

* OXID eShop CE (Update von 6.10.3 zu 6.11.0) `Changelog 6.11.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.11.0/CHANGELOG.md>`_
* PAYONE (Update von 1.6.2 zu 1.7.0) `Changelog 1.7.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.7.0/Changelog.txt>`_
* Klarna (Update von 5.5.2 zu 5.5.3) `Changelog 5.5.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.3/CHANGELOG.md>`_
* Neu: Makaira (2.11.0) `Changelog 2.11.0 <https://github.com/MakairaIO/oxid-connect/blob/stable/CHANGELOG.md>`_
* Neu: Unzer (Version 1.0 als Release Candidate):
* Neu: Amazon Pay für OXID (Version 1.2) `Changelog 1.2 <https://github.com/OXID-eSales/amazon-pay-module/blob/b-6.2.x/CHANGELOG.md>`_

Die Compilation enthält folgende Komponenten:

* OXID eShop CE 6.11.0 `Changelog 6.11.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.11.0/CHANGELOG.md>`_
* Theme "Flow" 3.8.0 `Changelog 3.8.0 <https://github.com/OXID-eSales/flow_theme/blob/v3.8.0/CHANGELOG.md>`_
* Theme "Wave" 1.6.1 `Changelog 1.6.1 <https://github.com/OXID-eSales/wave-theme/blob/v1.6.1/CHANGELOG.md>`_
* GDPR Opt-In 2.3.3 `Changelog 2.3.3 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* Klarna 5.5.3 `Changelog 5.5.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.3/CHANGELOG.md>`_
* OXID Cookie Management 1.2.0 powered by usercentrics `Changelog 1.2.0 <https://github.com/OXID-eSales/usercentrics/blob/v1.2.0/CHANGELOG.md>`_
* PAYONE 1.7.0 `Changelog 1.7.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.7.0/Changelog.txt>`_
* PayPal 6.4.0 `Changelog 6.4.0 <https://github.com/OXID-eSales/paypal/blob/v6.4.0/CHANGELOG.md>`_
* WYSIWYG Editor + Mediathek 2.4.1 `Changelog 2.4.1 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v2.4.1/CHANGELOG.md>`_
* Geo blocking 1.1.0 `Changelog 1.1.0 <https://github.com/OXID-eSales/geo-blocking-module/blob/v1.1.0/CHANGELOG.md>`_
* Country VAT Administration 1.0.3 `Changelog 1.0.3 <https://github.com/OXID-eSales/country-vat-module/blob/v1.0.3/CHANGELOG.md>`_
* OXID Econda Analytics (EE) 1.3.0 `Changelog 1.3.0 <https://github.com/OXID-eSales/econda-analytics-module/blob/v1.3.0/CHANGELOG.md>`_
* GraphQL 6.0.1 `Changelog 6.0.1 <https://github.com/OXID-eSales/graphql-base-module/blob/v6.0.1/CHANGELOG-v6.md>`_


Korrekturen
-----------

Korrekturen finden Sie in unserem Bugtracking-System aufgelistet.
|br|
https://bugs.oxid-esales.com/changelog_page.php?version_id=670


Installation
------------

Zum Installieren oder Aktualisieren folgen Sie den Anleitungen im Abschnitt *Installation*:


:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Minor Update installieren <../../installation/update/minor-update>` |br|
:doc:`Patch-Update installieren <../../installation/update/patch-update>`

.. Intern: , Status:
