OXID eShop Compilation 7.4.2
============================

Veröffentlichungsdatum: 25.08.2026

Optimierungen & Fehlerbehebungen
--------------------------------

Composer 2.10 Kompatibilität
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation 7.4.2 ist ein reines Wartungs-Release und
enthält **keine funktionalen Änderungen**. Sie stellt
ausschließlich sicher, dass die Installation mit aktuellen
Composer-Versionen ohne Beanstandung durch den
Sicherheits-Audit (``composer audit``) durchläuft.

Bereits mit der Compilation 7.4.1 wurde ``composer/composer``
auf 2.9.8 aktualisiert, um die Kompatibilität mit dem
automatischen Sicherheits-Audit von Composer 2.9
herzustellen. Mit neueren Composer-Veröffentlichungen und
aktualisierten Sicherheitshinweisen konnte diese Version
erneut zu Audit-Warnungen führen.

In der Compilation 7.4.2 wird ``composer/composer`` im
CE-Metapackage daher weiter aktualisiert:

* ``composer/composer`` von 2.9.8 auf 2.10.2

Da die Compilation-Version über die eShop-Kernkomponente
ausgewiesen wird, wurden die CE-, PE- und EE-Pakete zur
Bereitstellung der Compilation 7.4.2 auf v7.4.4 neu getaggt.
Diese Neu-Taggings enthalten **keine funktionalen Änderungen**;
die Aktualisierung von ``composer/composer`` erfolgt im Zuge
dieses Releases.

.. _packages-742:

Packages
--------

Gegenüber der Compilation 7.4.1 sind die Paketstände
unverändert – mit Ausnahme des auf v7.4.4 neu getaggten
eShop-Kerns (CE/PE/EE) und des aktualisierten
``composer/composer``-Pakets (siehe oben).

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop CE Compilation enthält u. a. die folgenden
geänderten Pakete:

* OXID eShop CE von v7.4.2 auf v7.4.4

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop PE Compilation enthält zusätzlich:

* OXID eShop PE von v7.4.2 auf v7.4.4

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop EE Compilation enthält zusätzlich:

* OXID eShop EE von v7.4.2 auf v7.4.4

Kompatible OXID Erweiterungen
-----------------------------

Die kompatiblen OXID Erweiterungen entsprechen denen der
Version 7.4.0 bzw. 7.4.1. Weitere Informationen finden Sie in den Release Notes der
OXID eShop Compilation
`7.4.0 <https://docs.oxid-esales.com/eshop/de/7.4/releases/oxid-eshop-740.html>`_ bzw.
`7.4.1 <https://docs.oxid-esales.com/eshop/de/7.4/releases/oxid-eshop-741.html>`_.

Update
------

Führen Sie die folgenden Befehle aus, um Ihren OXID eShop
von 7.4.1 auf 7.4.2 zu aktualisieren:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate
