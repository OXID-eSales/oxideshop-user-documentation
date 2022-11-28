OXID eShop 6.5.1
================

.. todo: #VL: Datum

Veröffentlichungstermin: 16.08.2022

.. todo: #SB/#VL: klären: So korrekt? Bleibt für den Shopbetreier noch was zu tun?

Mit OXID eShop 6.5.1 bindet das Theme "Wave" Google Fonts nicht mehr dynamisch ein, sondern lokal aus dem Theme-Ordner.

Hintergrund: Betreiber von Webshops, die dynamisch eingebundene Google Fonts verwenden, sind Opfer von Abmahnungen geworden.

Wenn Sie andere Google-Fonts als die im Wave-Theme verwendeten dynamisch eingebunden haben, dann stellen Sie sicher, diese Fonts ebenfalls aus einem lokalen Ordner einzubinden. Wie es geht, beschreibt Google unter https://fonts.google.com/knowledge/using_type/self_hosting_web_fonts.

Weitere Informationen finden Sie in unserem `Blogpost vom 21.09.2022 <https://www.oxid-esales.com/blog/moegliche-abmahnungen-bei-google-fonts/>`_.

Außerdem haben wir Bugs behoben. Siehe :ref:`releases/releases-65/oxid-eshop-651:Korrekturen`.



Verbesserungen und Anpassungen
------------------------------

.. todo: #VL: tbd

Sehen Sie Änderungen in der Compilation im Metapackage ein: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.5.0…v6.5.1>`_.


Aktualisierte Komponenten
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #VL: tbd

Folgende Komponenten und Module wurden aktualisiert:

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

.. todo: #VL: tbd

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


Korrekturen
-----------

Korrekturen finden Sie in unserem Bugtracking-System unter https://bugs.oxid-esales.com/changelog_page.php?version_id=712.


Installation
------------

Zum Installieren oder Aktualisieren folgen Sie den Anleitungen im Abschnitt *Installation*:


:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>` |br|
:doc:`Minor Update installieren <../../installation/update/minor-update>` |br|
:doc:`Patch-Update installieren <../../installation/update/patch-update>`

.. Intern: , Status:
