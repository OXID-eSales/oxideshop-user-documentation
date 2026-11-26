OXID eShop Compilation 7.4.6
============================

Veröffentlichungsdatum: TBD

Optimierungen & Fehlerbehebungen
--------------------------------

Aktualisierte Symfony-Komponenten und Twig
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation 7.4.6 ist ein Wartungs-Release. Sie aktualisiert
Symfony-Komponenten und Twig. Die Updates enthalten die Korrekturen zu den
folgenden Sicherheitshinweisen:

* ``symfony/expression-language`` von v6.4.48 auf v6.4.51:
  `CVE-2026-133760 <https://github.com/symfony/symfony/security/advisories/GHSA-fvvg-g68p-p6q9>`_
* ``twig/twig`` von v3.27.0 auf v3.31.1:
  `CVE-2026-133763 <https://github.com/twigphp/Twig/security/advisories/GHSA-567w-cx2v-jc85>`_,
  `CVE-2026-133764 <https://github.com/twigphp/Twig/security/advisories/GHSA-rc9g-xwx4-rmfh>`_,
  `CVE-2026-133765 <https://github.com/twigphp/Twig/security/advisories/GHSA-ccrc-gqhf-3cxc>`_,
  `CVE-2026-133766 <https://github.com/twigphp/Twig/security/advisories/GHSA-56wp-8m9q-4354>`_,
  `CVE-2026-133767 <https://github.com/twigphp/Twig/security/advisories/GHSA-fmp9-6wxr-cfmq>`_,
  `CVE-2026-133768 <https://github.com/twigphp/Twig/security/advisories/GHSA-p2x6-ppf3-32r3>`_,
  `CVE-2026-133770 <https://github.com/twigphp/Twig/security/advisories/GHSA-r34x-hh9h-9q9c>`_,
  `CVE-2026-133771 <https://github.com/twigphp/Twig/security/advisories/GHSA-63v2-9rx5-wjgr>`_,
  `CVE-2026-133772 <https://github.com/twigphp/Twig/security/advisories/GHSA-qr49-4294-4gmw>`_

Da die Compilation-Version über die eShop-Kernkomponente
ausgewiesen wird, wurde das CE-Paket v7.4.8 zur Bereitstellung der
Compilation-Information 7.4.6 veröffentlicht. Die PE- und EE-Pakete
wurden ebenfalls auf v7.4.8 getaggt, damit alle drei Editionen
zusammenpassen. Diese Komponenten enthalten **keine funktionalen
Änderungen**; die Aktualisierung der Symfony-Komponenten und von Twig
erfolgt im Zuge dieses Releases.

.. _packages-746:

Packages
--------

Gegenüber der Compilation 7.4.5 sind die Paketstände unverändert,
mit Ausnahme des auf v7.4.8 neu getaggten eShop-Kerns (CE/PE/EE)
und der oben genannten aktualisierten Komponenten.

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop CE Compilation enthält u. a. die folgenden
geänderten Pakete:

* OXID eShop CE von v7.4.7 auf v7.4.8

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop PE Compilation enthält zusätzlich:

* OXID eShop PE von v7.4.7 auf v7.4.8

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop EE Compilation enthält zusätzlich:

* OXID eShop EE von v7.4.7 auf v7.4.8

Kompatible OXID Erweiterungen
-----------------------------

Die kompatiblen OXID Erweiterungen entsprechen denen der Versionen
7.4.0, 7.4.1, 7.4.2, 7.4.3, 7.4.4 bzw. 7.4.5. Weitere Informationen finden Sie in den Release Notes der
OXID eShop Compilation
`7.4.0 <https://docs.oxid-esales.com/eshop/de/7.4/releases/oxid-eshop-740.html>`_,
`7.4.1 <https://docs.oxid-esales.com/eshop/de/7.4/releases/oxid-eshop-741.html>`_,
`7.4.2 <https://docs.oxid-esales.com/eshop/de/7.4/releases/oxid-eshop-742.html>`_,
`7.4.3 <https://docs.oxid-esales.com/eshop/de/7.4/releases/oxid-eshop-743.html>`_,
`7.4.4 <https://docs.oxid-esales.com/eshop/de/7.4/releases/oxid-eshop-744.html>`_ bzw.
`7.4.5 <https://docs.oxid-esales.com/eshop/de/7.4/releases/oxid-eshop-745.html>`_.

Update
------

Führen Sie die folgenden Befehle aus, um Ihren OXID eShop
von 7.4.5 auf 7.4.6 zu aktualisieren:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate
