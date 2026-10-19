OXID eShop Compilation 7.5.1
============================

Veröffentlichungsdatum: TBD

Optimierungen & Fehlerbehebungen
--------------------------------

Symfony Sicherheitsaktualisierung (CVE-2026-109449)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation 7.5.1 ist ein Wartungs-Release und behebt eine
Sicherheitslücke in der Symfony-Komponente
``symfony/expression-language``.

Der Sicherheitshinweis **CVE-2026-109449** (Advisory
PKSA-vq1j-sc3k-jzzk, "Unbounded Nesting in the Expression Parser")
betrifft den Ausdrucks-Parser: nicht vertrauenswürdige Ausdrücke
mit unbegrenzter Verschachtelung können den Prozess zum Absturz
bringen.

Zur Behebung wird ``symfony/expression-language`` aktualisiert; im
Zuge dessen werden die weiteren betroffenen Symfony-Komponenten auf
denselben Stand gebracht:

* ``symfony/expression-language`` von v6.4.32 auf v6.4.48
* ``symfony/http-foundation`` von v6.4.41 auf v6.4.48
* ``symfony/yaml`` von v6.4.40 auf v6.4.48

Da die Compilation-Version über die eShop-Kernkomponente
ausgewiesen wird, wurde das CE-Paket v7.5.2 zur Bereitstellung der
Compilation-Information 7.5.1 veröffentlicht. Die PE- und EE-Pakete
wurden ebenfalls auf v7.5.2 getaggt, damit alle drei Editionen
zusammenpassen. Diese Komponenten enthalten **keine funktionalen
Änderungen**; die Aktualisierung der Symfony-Komponenten erfolgt im
Zuge dieses Releases.

.. _packages-751:

Packages
--------

Gegenüber der Compilation 7.5.0 sind die Paketstände unverändert,
mit Ausnahme des auf v7.5.2 neu getaggten eShop-Kerns (CE/PE/EE)
und der oben genannten aktualisierten Symfony-Komponenten.

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop CE Compilation enthält u. a. die folgenden
geänderten Pakete:

* OXID eShop CE von v7.5.1 auf v7.5.2

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop PE Compilation enthält zusätzlich:

* OXID eShop PE von v7.5.1 auf v7.5.2

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop EE Compilation enthält zusätzlich:

* OXID eShop EE von v7.5.1 auf v7.5.2

Kompatible OXID Erweiterungen
-----------------------------

Die kompatiblen OXID Erweiterungen entsprechen denen der Version
7.5.0. Weitere Informationen finden Sie in den Release Notes der
OXID eShop Compilation
`7.5.0 <https://docs.oxid-esales.com/eshop/de/7.5/releases/oxid-eshop-750.html>`_.

Update
------

Führen Sie die folgenden Befehle aus, um Ihren OXID eShop
von 7.5.0 auf 7.5.1 zu aktualisieren:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate
