OXID eShop Compilation 7.5.3
============================

Veröffentlichungsdatum: TBD

Optimierungen & Fehlerbehebungen
--------------------------------

Aktualisierte Symfony-Komponenten und Twig
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation 7.5.3 ist ein Wartungs-Release. Sie aktualisiert
Symfony-Komponenten und Twig. Die Updates enthalten die Korrekturen zu den
folgenden Sicherheitshinweisen:

* ``symfony/expression-language`` von v6.4.48 auf v6.4.51:
  `CVE-2026-133760 <https://github.com/symfony/symfony/security/advisories/GHSA-fvvg-g68p-p6q9>`_
* ``symfony/html-sanitizer`` von v6.4.50 auf v6.4.51:
  `CVE-2026-133756 <https://github.com/symfony/symfony/security/advisories/GHSA-wccc-v7v7-gc54>`_
* ``symfony/http-kernel`` von v6.4.50 auf v6.4.51:
  `CVE-2026-133743 <https://github.com/symfony/symfony/security/advisories/GHSA-8cww-v5fg-2mf9>`_
* ``symfony/routing`` von v6.4.50 auf v6.4.51:
  `CVE-2026-133746 <https://github.com/symfony/symfony/security/advisories/GHSA-cpx6-mpfq-c6cr>`_,
  `CVE-2026-133754 <https://github.com/symfony/symfony/security/advisories/GHSA-wgv4-frv7-c8c5>`_
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
ausgewiesen wird, wurde das CE-Paket v7.5.4 zur Bereitstellung der
Compilation-Information 7.5.3 veröffentlicht. Die PE- und EE-Pakete
wurden ebenfalls auf v7.5.4 getaggt, damit alle drei Editionen
zusammenpassen. Diese Komponenten enthalten **keine funktionalen
Änderungen**; die Aktualisierung der Symfony-Komponenten und von Twig
erfolgt im Zuge dieses Releases.

.. _packages-753:

Packages
--------

Gegenüber der Compilation 7.5.2 sind die Paketstände unverändert,
mit Ausnahme des auf v7.5.4 neu getaggten eShop-Kerns (CE/PE/EE)
und der oben genannten aktualisierten Komponenten sowie der unten aufgeführten weiteren Komponenten.

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop CE Compilation enthält u. a. die folgenden
geänderten Pakete:

* OXID eShop CE von v7.5.3 auf v7.5.4
* ``symfony/http-foundation`` von v6.4.50 auf v6.4.51

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop PE Compilation enthält zusätzlich:

* OXID eShop PE von v7.5.3 auf v7.5.4

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop EE Compilation enthält zusätzlich:

* OXID eShop EE von v7.5.3 auf v7.5.4

Kompatible OXID Erweiterungen
-----------------------------

Die kompatiblen OXID Erweiterungen entsprechen denen der Versionen
7.5.0, 7.5.1 bzw. 7.5.2. Weitere Informationen finden Sie in den Release Notes der
OXID eShop Compilation
`7.5.0 <https://docs.oxid-esales.com/eshop/de/7.5/releases/oxid-eshop-750.html>`_,
`7.5.1 <https://docs.oxid-esales.com/eshop/de/7.5/releases/oxid-eshop-751.html>`_ bzw.
`7.5.2 <https://docs.oxid-esales.com/eshop/de/7.5/releases/oxid-eshop-752.html>`_.

Update
------

Führen Sie die folgenden Befehle aus, um Ihren OXID eShop
von 7.5.2 auf 7.5.3 zu aktualisieren:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate
