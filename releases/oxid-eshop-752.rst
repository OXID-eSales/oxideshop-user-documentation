OXID eShop Compilation 7.5.2
============================

Veröffentlichungsdatum: TBD

Optimierungen & Fehlerbehebungen
--------------------------------

Aktualisierte Symfony-Komponente
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation 7.5.2 ist ein Wartungs-Release. Sie aktualisiert die
Symfony-Komponente ``symfony/mime`` auf die Version v6.4.49. Das Update enthält die
Korrektur zu dem folgenden Sicherheitshinweis von Symfony:

* ``symfony/mime`` von v6.4.40 auf v6.4.49:
  `CVE-2026-45070 <https://symfony.com/cve-2026-45070>`_

Da die Compilation-Version über die eShop-Kernkomponente
ausgewiesen wird, wurde das CE-Paket v7.5.3 zur Bereitstellung der
Compilation-Information 7.5.2 veröffentlicht. Die PE- und EE-Pakete
wurden ebenfalls auf v7.5.3 getaggt, damit alle drei Editionen
zusammenpassen. Diese Komponenten enthalten **keine funktionalen
Änderungen**; die Aktualisierung der Symfony-Komponente erfolgt im
Zuge dieses Releases.

.. _packages-752:

Packages
--------

Gegenüber der Compilation 7.5.1 sind die Paketstände unverändert,
mit Ausnahme des auf v7.5.3 neu getaggten eShop-Kerns (CE/PE/EE)
und der oben genannten aktualisierten Symfony-Komponente.

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop CE Compilation enthält u. a. die folgenden
geänderten Pakete:

* OXID eShop CE von v7.5.2 auf v7.5.3

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop PE Compilation enthält zusätzlich:

* OXID eShop PE von v7.5.2 auf v7.5.3

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop EE Compilation enthält zusätzlich:

* OXID eShop EE von v7.5.2 auf v7.5.3

Kompatible OXID Erweiterungen
-----------------------------

Die kompatiblen OXID Erweiterungen entsprechen denen der Version
7.5.0 bzw. 7.5.1. Weitere Informationen finden Sie in den Release Notes der
OXID eShop Compilation
`7.5.0 <https://docs.oxid-esales.com/eshop/de/7.5/releases/oxid-eshop-750.html>`_ bzw.
`7.5.1 <https://docs.oxid-esales.com/eshop/de/7.5/releases/oxid-eshop-751.html>`_.

Update
------

Führen Sie die folgenden Befehle aus, um Ihren OXID eShop
von 7.5.1 auf 7.5.2 zu aktualisieren:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate
