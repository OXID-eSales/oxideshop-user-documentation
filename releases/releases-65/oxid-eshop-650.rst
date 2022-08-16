OXID eShop 6.5.0
================

Veröffentlichungstermin: 16.08.2022

OXID eShop 6.5.0

* unterstützt unter anderem zwei unserer neuen Zahlungsmodule
  |br|
  Siehe :ref:`releases/releases-65/oxid-eshop-650:Neue oder aktualisierte Komponenten`.
* behebt Bugs
  |br|
  Siehe :ref:`releases/releases-65/oxid-eshop-650:Korrekturen`.
* unterstützt PHP 8.1
  |br|
  Siehe unter :ref:`installation/neu-installation/server-und-systemvoraussetzungen:Server und Systemvoraussetzungen`, Abschnitt :ref:`installation/neu-installation/server-und-systemvoraussetzungen:PHP`.
* verwendet `Symfony 5.4 <https://symfony.com/releases/5.4>`_ statt Symfony 3.4
  |br|
  Hintergrund: Symfony 3.4 wird nicht mehr mit (Sicherheits-) Updates unterstützt und ist nicht mit PHP 8.1 kompatibel.

  .. attention::

     **Breaking Changes**

     Prüfen Sie, ob Sie alle Module in OXID eShop 6.5 weiterhin verwenden können.

     * Drittanbieter- oder eigene Module

       Wenn Sie Drittanbieter- oder selbst entwickelte Module verwenden, stellen Sie sicher, dass diese Module mit Symfony 5.4 kompatibel sind.

     * Amazon Pay

       Das bisherige :productname:`Amazon Pay` (Amazon Pay & Login for OXID eShop) wird nicht mehr von OXID eShop unterstützt.

       Hintergrund: Wir ersetzen :productname:`Amazon Pay` durch unser neues Modul :productname:`Amazon Pay für OXID`.

       Abhilfe: Um Ihren OXID eShop reibungslos auf das neue Modul umzustellen, folgen Sie den Anweisungen unter :ref:`releases/releases-65/oxid-eshop-650:Breaking Changes`.

.. important::

  **Neue OXID eShop Community Edition-Lizenz**

  Mit der OXID eShop Version 6.5.0 ist die Community Edition ausschließlich für den nichtkommerziellen Einsatz bestimmt.

  Wir stellen Ihnen die OXID eShop Community Edition ab dem 15.08.2022 zum Evaluieren, Testen und für Proof of Concepts zur Verfügung.

  Weitere Informationen über die OXID eShop Community Edition-Lizenz 2022 finden Sie unter https://github.com/OXID-eSales/oxideshop_ce/blob/b-6.5.x/LICENSE.

  Um die OXID eShop Software kommerziell zu nutzen, wenden Sie sich an OXID eSales unter sales@oxid-esales.com.


Verbesserungen und Anpassungen
------------------------------

Sehen Sie Änderungen in der Compilation im Metapackage ein: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.4.3…v6.5.0>`_.

Breaking Changes
^^^^^^^^^^^^^^^^

Das bisherige Amazon Pay-Modul :productname:`Amazon Pay & Login for OXID eShop` (siehe https://github.com/bestit/amazon-pay-oxid) ist nicht mehr Teil der Compilation.

Wir ersetzen es durch ein neues Modul :productname:`Amazon Pay für OXID` für den Zahlungsverkehr und Checkout mit Amazon.

Wenn Sie :productname:`Amazon Pay & Login for OXID eShop` verwenden, betreiben Sie es zusammen mit :productname:`Amazon Pay für OXID` vorübergehend  parallel, bevor Sie das Update auf OXID eShop 6.5 machen.
|br|
Der Parallelbetrieb ist so lange nötig, bis alle alten Bestellungen abgeschlossen sind, die noch mit :productname:`Amazon Pay & Login for OXID eShop` erfolgt sind.

Tun Sie Folgendes:

1. Wenn Sie OXID 6.0 oder früher haben, machen Sie ein Update auf OXID eShop Version 6.1, 6.2 oder 6.3.
   |br|
   Hintergrund: Der Parallelbetrieb ist nur in den Versionen OXID 6.1 bis OXID 6.3 möglich.

#. Installieren und konfigurieren Sie :productname:`Amazon Pay für OXID`.
   |br|
   Weitere Informationen finden Sie unter https://docs.oxid-esales.com/modules/amazon-pay/de/latest/index.html.
#. Planen Sie eine Downtime für Ihren OXID eShop ein und tun Sie Folgendes:

   * Schalten Sie :productname:`Amazon Pay für OXID` für den Live-Betrieb frei.
   * Deaktivieren Sie Zahlungsarten, die zu :productname:`Amazon Pay & Login for OXID eShop` gehören.

   Resultat: Ihre Kunden wickeln künftige Zahlungen mit :productname:`Amazon Pay für OXID` ab.
   |br|
   Zahlungen für alte Bestellungen können Sie weiterhin mit :productname:`Amazon Pay & Login for OXID eShop` überwachen.
#. Sobald alle alten Bestellungen abgewickelt sind, tun Sie Folgendes:

   1. Deaktivieren Sie :productname:`Amazon Pay & Login for OXID eShop`.
   #. Führen Sie das Update auf OXID eShop 6.5 durch.


Neue oder aktualisierte Komponenten
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Folgende Komponenten und Module wurden aktualisiert oder sind neu hinzugekommen:

* OXID eShop CE (Update von 6.10.3 zu 6.12.0) `Changelog 6.12.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.12.0/CHANGELOG.md>`_
* Theme "Flow" (Update von 3.8.0 zu 3.8.1):  `Changelog 3.8.1 <https://github.com/OXID-eSales/flow_theme/blob/v3.8.1/CHANGELOG.md>`_
* Theme "Wave" (Update von 1.6.1 zu 1.6.2):  `Changelog 1.6.2 <https://github.com/OXID-eSales/wave-theme/blob/v1.6.2/CHANGELOG.md>`_
* PayPal 6.5.0 (Update von 6.4.1 zu 6.5.0): `Changelog 6.5.0 <https://github.com/OXID-eSales/paypal/blob/v6.5.0/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics (Update von 1.2.0 zu 1.2.1) `Changelog 1.2.1 <https://github.com/OXID-eSales/usercentrics/blob/v1.2.1/CHANGELOG.md>`_
* PAYONE (Update von 1.6.2 zu 1.7.0) `Changelog 1.7.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.7.0/Changelog.txt>`_
* Klarna (Update von 5.5.2 zu 5.5.3) `Changelog 5.5.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.3/CHANGELOG.md>`_
* Neu: Makaira (1.4.2) `Changelog 1.4.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/1.4.2/CHANGELOG.md>`_
* Neu: Unzer Payment für OXID (Version 1.0.0 für die Enterprise Edition): `Changelog 1.0.0 <https://github.com/OXID-eSales/unzer-module/blob/v1.0.0/CHANGELOG.md>`_
  |br|
  Weitere Informationen über unser neues Zahlungs-Modul finden Sie unter https://docs.oxid-esales.com/modules/unzer/de/latest/index.html.


Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält folgende Komponenten:

* OXID eShop CE 6.12.0: `Changelog 6.12.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.12.0/CHANGELOG.md>`_
* OXID eShop composer plugin 5.2.2: `Changelog 5.2.2 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.2.2/CHANGELOG.md>`_
* Theme "Flow" 3.8.1: `Changelog 3.8.1 <https://github.com/OXID-eSales/flow_theme/blob/v3.8.1/CHANGELOG.md>`_
* Theme "Wave" 1.6.2: `Changelog 1.6.2 <https://github.com/OXID-eSales/wave-theme/blob/v1.6.2/CHANGELOG.md>`_
* GDPR Opt-In 2.3.3: `Changelog 2.3.3 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* Klarna 5.5.3: `Changelog 5.5.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.3/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics 1.2.1: `Changelog 1.2.1 <https://github.com/OXID-eSales/usercentrics/blob/v1.2.1/CHANGELOG.md>`_
* PAYONE 1.7.0: `Changelog 1.7.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.7.0/Changelog.txt>`_
* PayPal 6.5.0: `Changelog 6.5.0 <https://github.com/OXID-eSales/paypal/blob/v6.5.0/CHANGELOG.md>`_
* WYSIWYG Editor + Mediathek 2.4.1: `Changelog 2.4.1 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v2.4.1/CHANGELOG.md>`_
* Makaira 1.4.2: `Changelog 1.4.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/1.4.2/CHANGELOG.md>`_
* Unzer Payment für OXID 1.0.0 (EE): `Changelog 1.0.0 <https://github.com/OXID-eSales/unzer-module/blob/v1.0.0/CHANGELOG.md>`_


Sonstige Module
^^^^^^^^^^^^^^^

Installieren Sie die folgenden Module bei Bedarf manuell.

* OXID Econda Analytics (EE) 1.3.0: `Changelog 1.3.0 <https://github.com/OXID-eSales/econda-analytics-module/blob/v1.3.0/CHANGELOG.md>`_
* Geo blocking 1.1.0: `Changelog 1.1.0 <https://github.com/OXID-eSales/geo-blocking-module/blob/v1.1.0/CHANGELOG.md>`_
* Country VAT Administration 1.0.3: `Changelog 1.0.3 <https://github.com/OXID-eSales/country-vat-module/blob/v1.0.3/CHANGELOG.md>`_
* GraphQL 7.0.2: `Changelog 7.0.2 <https://github.com/OXID-eSales/graphql-base-module/blob/v7.0.2/CHANGELOG-v7.md>`_

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
