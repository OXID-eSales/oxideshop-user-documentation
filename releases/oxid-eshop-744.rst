OXID eShop Compilation 7.4.4
============================

Veröffentlichungsdatum: TBD

Optimierungen & Fehlerbehebungen
--------------------------------

Symfony Sicherheitsaktualisierung (CVE-2026-109449)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation 7.4.4 ist ein Wartungs-Release und behebt eine
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

* ``symfony/expression-language`` von v6.4.24 auf v6.4.48
* ``symfony/http-foundation`` von v6.4.41 auf v6.4.48
* ``symfony/yaml`` von v6.4.40 auf v6.4.48

Da die Compilation-Version über die eShop-Kernkomponente
ausgewiesen wird, wurde das CE-Paket v7.4.6 zur Bereitstellung der
Compilation-Information 7.4.4 veröffentlicht. Die PE- und EE-Pakete
wurden ebenfalls auf v7.4.6 getaggt, damit alle drei Editionen
zusammenpassen. Diese Komponenten enthalten **keine funktionalen
Änderungen**; die Aktualisierung der Symfony-Komponenten erfolgt im
Zuge dieses Releases.

.. _packages-744:

Packages
--------

Gegenüber der Compilation 7.4.3 sind die Paketstände unverändert,
mit Ausnahme des auf v7.4.6 neu getaggten eShop-Kerns (CE/PE/EE)
und der oben genannten aktualisierten Symfony-Komponenten.

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop CE Compilation enthält u. a. die folgenden
geänderten Pakete:

* OXID eShop CE von v7.4.5 auf v7.4.6

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop PE Compilation enthält zusätzlich:

* OXID eShop PE von v7.4.5 auf v7.4.6

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop EE Compilation enthält zusätzlich:

* OXID eShop EE von v7.4.5 auf v7.4.6

Kompatible OXID Erweiterungen
-----------------------------

Die kompatiblen OXID Erweiterungen entsprechen denen der Version
7.4.0, 7.4.1, 7.4.2 bzw. 7.4.3. Weitere Informationen finden Sie in
den Release Notes der OXID eShop Compilation
`7.4.0 <https://docs.oxid-esales.com/eshop/de/7.4/releases/oxid-eshop-740.html>`_,
`7.4.1 <https://docs.oxid-esales.com/eshop/de/7.4/releases/oxid-eshop-741.html>`_,
`7.4.2 <https://docs.oxid-esales.com/eshop/de/7.4/releases/oxid-eshop-742.html>`_ bzw.
`7.4.3 <https://docs.oxid-esales.com/eshop/de/7.4/releases/oxid-eshop-743.html>`_.

Update
------

Führen Sie die folgenden Befehle aus, um Ihren OXID eShop
von 7.4.3 auf 7.4.4 zu aktualisieren:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate
