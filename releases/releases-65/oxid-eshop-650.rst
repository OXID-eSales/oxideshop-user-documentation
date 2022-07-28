OXID eShop 6.5.0
================

Veröffentlichungstermin: 02.08.2022

OXID eShop 6.5.0

* unterstützt unter anderem zwei unserer neuen Zahlungsmodule
  |br|
  Siehe :ref:`releases/releases-65/oxid-eshop-650:Neue oder aktualisierte Komponenten`.
* behebt Bugs
  |br|
  Siehe :ref:`releases/releases-65/oxid-eshop-650:Korrekturen`.
* unterstützt PHP 8.1
  |br|
  Siehe unter :ref:`installation/neu-installation/server-und-systemvoraussetzungen:Server und Systemvoraussetzungen` Abschnitt :ref:`installation/neu-installation/server-und-systemvoraussetzungen:PHP`.
* verwendet `Symfony 5.4 <https://symfony.com/releases/5.4>`_ statt Symfony 3.4
  |br|
  Hintergrund: Symfony 3.4 wird nicht mehr mit (Sicherheits-) Updates unterstützt und ist nicht mit PHP 8.1 kompatibel.

  .. attention::

     **Breaking Changes**

     Prüfen Sie, ob Sie alle Module in OXID eShop 6.5 weiterhin verwenden können.

     * Drittanbieter-Module

       Wenn Sie Drittanbieter-Module verwenden, fragen Sie die Hersteller, ob Ihre Drittanbieter-Module mit Symfony 5.4 kompatibel sind.

     * Amazon Pay

       :productname:`Amazon Pay` wird nicht mehr von OXID eShop unterstützt.

       Hintergrund: Wir ersetzen :productname:`Amazon Pay` durch unser neues Modul :productname:`Amazon Pay für OXID`.

       Abhilfe: Folgen Sie den Anweisungen für ein Workaround unter :ref:`releases/releases-65/oxid-eshop-650:Breaking Changes`.


Verbesserungen und Anpassungen
------------------------------

Sehen Sie Änderungen in der Compilation im Metapackage ein: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.4.3…v6.5.0>`_.

Breaking Changes
^^^^^^^^^^^^^^^^

Die Komponente Amazon Pay können Sie in OXID eShop 6.5 nicht mehr verwenden.

Hintergrund: Wir ersetzen :productname:`Amazon Pay` durch unser neues Zahlungsmodul :productname:`Amazon Pay für OXID`.

.. todo: Was bedeutet genau:
    Das bisherige Amazon Pay Modul ist nicht mehr Teil der Compilation, -- funzt es unter 6.5 oder nicht?
     sondern wird durch ein neues Modul für den Zahlungsverkehr und Checkout mit Amazon ersetzt.
    Bitte beachten Sie dies beim Update und testen Sie vorab das neue Modul ausgiebig,
    um anschließend eine reibungslose Umstellung im Live-Betrieb zu gewährleisten.

Workaround: Wenn Sie :productname:`Amazon Pay` verwenden, machen Sie kein Update auf OXID eShop 6.5.

Wenn Sie :productname:`Amazon Pay` verwenden, betreiben Sie :productname:`Amazon Pay` und :productname:`Amazon Pay für OXID` vorübergehend im parallel, bevor Sie das Update auf OXID eShop 6.5 machen.
|br|
Der Parallelbetrieb ist so lange nötig, bis alle alten Bestellungen abgeschlossen sind, die noch mit :productname:`Amazon Pay` erfolgt sind.

Tun Sie Folgendes:

1. Wenn Sie OXID 6.1 oder früher haben, machen Sie ein Update auf OXID eShop Version 6.2 oder 6.3.
   |br|
   Hintergrund: Der Parallelbetrieb ist nur in den Versionen OXID 6.2 und OXID 6.3 möglich.

   .. todo: #ML klären: Aussage falsch: "Installieren Sie Amazon Pay für den OXID eShop ab Version 6.1." ?

#. Installieren und konfigurieren Sie :productname:`Amazon Pay für OXID`.
   |br|
   Weitere Informationen finden Sie unter https://docs.oxid-esales.com/modules/amazon-pay/de/latest/index.html.
#. Planen Sie eine Downtime für Ihren OXID eShop ein und tun Sie Folgendes:

   * Schalten Sie :productname:`Amazon Pay für OXID` für den Live-Betrieb frei.
   * Deaktivieren Sie alle Zahlungsarten, die zu :productname:`Amazon Pay` gehören.

   .. todo: #ML: klären: woran kann ich die leicht erkennen?

   Resultat: Ihre Kunden wickeln künftige Zahlungen mit :productname:`Amazon Pay für OXID` ab.
   |br|
   Zahlungen für alte Bestellungen können Sie weiterhin mit :productname:`Amazon Pay` überwachen.
#. Sobald alle alten Bestellungen abgewickelt sind, tun Sie Folgendes:

   * Deaktivieren Sie :productname:`Amazon Pay`.
   * Führen Sie das Update auf OXID eShop 6.5 durch.


Neue oder aktualisierte Komponenten
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Folgende Komponenten wurden aktualisiert oder sind neu hinzugekommen:

.. todo: #VL: Verifizieren: weitere Komponenten aktualisiert?
.. todo: #VL: Ist Makaira oxid-connect richtig?

* OXID eShop CE (Update von 6.10.3 zu 6.11.0) `Changelog 6.11.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.11.0/CHANGELOG.md>`_

.. todo: #VL: warum hatten wir folgende Komponenten bisher nicht, lassen wir sie weg?
* OXID eShop composer plugin (Update von 5.2.1 zu 5.2.2): `Changelog 5.2.2 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.2.2/CHANGELOG.md>`_
* OXID eShop DemoData installer
* OXID eShop doctrine migration integration
* OXID eShop facts
* Unified Namespace Generator
* PayPal - The OXID eFire extension
* Visual CMS 3.6.1
* OXID eShop EE

.. todo: #VL: wo sind folgende Komponenen in composer.json?
* Geo blocking 1.1.0
* Country VAT Administration 1.0.3
* OXID Econda Analytics (EE) 1.3.0
* GraphQL 6.0.1



* Theme "Flow" (Update von 3.8.0 zu 3.8.1):  `Changelog 3.8.1 <https://github.com/OXID-eSales/flow_theme/blob/v3.8.1/CHANGELOG.md>`_
* Theme "Wave" (Update von 1.6.1 zu 1.6.2):  `Changelog 1.6.2 <https://github.com/OXID-eSales/wave-theme/blob/v1.6.2/CHANGELOG.md>`_
* PayPal 6.5.0 (Update 6.4.1 zu 6.5.0): `Changelog 6.5.0 <https://github.com/OXID-eSales/paypal/blob/v6.5.0/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics (Update von 1.2.0 zu 1.2.1) `Changelog 1.2.1 <https://github.com/OXID-eSales/usercentrics/blob/v1.2.1/CHANGELOG.md>`_
* PAYONE (Update von 1.6.2 zu 1.7.0) `Changelog 1.7.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.7.0/Changelog.txt>`_
* Klarna (Update von 5.5.2 zu 5.5.3) `Changelog 5.5.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.3/CHANGELOG.md>`_

* Neu: Makaira (2.11.0) `Changelog 2.11.0 <https://github.com/MakairaIO/oxid-connect/blob/stable/CHANGELOG.md>`_
* Neu: Unzer (Version 1.0 als Release Candidate): `Changelog 1.0 <https://github.com/OXID-eSales/unzer-module/blob/b-6.3.x/CHANGELOG.md>`_
  |br|
  Weitere Informationen über unser neues Zahlungs-Modul finden Sie unter https://docs.oxid-esales.com/modules/unzer/de/latest/index.html.
* Neu: Amazon Pay für OXID (Version 1.2.0) `Changelog 1.2.0 <https://github.com/OXID-eSales/amazon-pay-module/blob/b-6.2.x/CHANGELOG.md>`_
  |br|
  Weitere Informationen über unser neues Zahlungs-Modul finden Sie unter https://docs.oxid-esales.com/modules/amazon-pay/de/latest/.

Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #VL: Komponenten verifizieren; Was ist der use case für die Liste? Warum fühen wir nicht alle Komponenten auf?

Die Compilation enthält folgende Komponenten:

* OXID eShop CE 6.11.0: `Changelog 6.11.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.11.0/CHANGELOG.md>`_
* OXID eShop composer plugin 5.2.2) `Changelog 5.2.2 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.2.2/CHANGELOG.md>`_

* Theme "Flow" 3.8.1: `Changelog 3.8.1 <https://github.com/OXID-eSales/flow_theme/blob/v3.8.1/CHANGELOG.md>`_
* Theme "Wave" 1.6.2: `Changelog 1.6.2 <https://github.com/OXID-eSales/wave-theme/blob/v1.6.2/CHANGELOG.md>`_
* GDPR Opt-In 2.3.3: `Changelog 2.3.3 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* Klarna 5.5.3: `Changelog 5.5.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.3/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics 1.2.1: `Changelog 1.2.1 <https://github.com/OXID-eSales/usercentrics/blob/v1.2.1/CHANGELOG.md>`_
* PAYONE 1.7.0: `Changelog 1.7.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.7.0/Changelog.txt>`_
* PayPal 6.5.0: `Changelog 6.5.0 <https://github.com/OXID-eSales/paypal/blob/v6.5.0/CHANGELOG.md>`_
* WYSIWYG Editor + Mediathek 2.4.1: `Changelog 2.4.1 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v2.4.1/CHANGELOG.md>`_
* Geo blocking 1.1.0: `Changelog 1.1.0 <https://github.com/OXID-eSales/geo-blocking-module/blob/v1.1.0/CHANGELOG.md>`_
* Country VAT Administration 1.0.3: `Changelog 1.0.3 <https://github.com/OXID-eSales/country-vat-module/blob/v1.0.3/CHANGELOG.md>`_
* OXID Econda Analytics (EE) 1.3.0: `Changelog 1.3.0 <https://github.com/OXID-eSales/econda-analytics-module/blob/v1.3.0/CHANGELOG.md>`_
* GraphQL 6.0.1: `Changelog 6.0.1 <https://github.com/OXID-eSales/graphql-base-module/blob/v6.0.1/CHANGELOG-v6.md>`_
* Makaira (2.11.0) `Changelog 2.11.0 <https://github.com/MakairaIO/oxid-connect/blob/stable/CHANGELOG.md>`_
* Unzer (RC Version 1.0): `Changelog 1.0 <https://github.com/OXID-eSales/unzer-module/blob/b-6.3.x/CHANGELOG.md>`_
* Amazon Pay für OXID (Version 1.2.0): `Changelog 1.2.0 <https://github.com/OXID-eSales/amazon-pay-module/blob/b-6.2.x/CHANGELOG.md>`_

Korrekturen
-----------

Korrekturen finden Sie in unserem Bugtracking-System unter https://bugs.oxid-esales.com/changelog_page.php?version_id=670.


Installation
------------

Zum Installieren oder Aktualisieren folgen Sie den Anleitungen im Abschnitt *Installation*:


:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Minor Update installieren <../../installation/update/minor-update>` |br|
:doc:`Patch-Update installieren <../../installation/update/patch-update>`

.. Intern: , Status:
