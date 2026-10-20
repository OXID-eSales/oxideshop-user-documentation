OXID eShop Compilation 7.5.1
============================

Release date: TBD


Improvements & Bug Fixes
-------------------------

Updated Symfony Components
^^^^^^^^^^^^^^^^^^^^^^^^^^

The 7.5.1 compilation is a maintenance release. It updates three
Symfony components to version v6.4.48 each. The updates contain the
fixes for the following Symfony security advisories:

* ``symfony/expression-language`` from v6.4.32 to v6.4.48:
  `CVE-2026-109449 <https://symfony.com/cve-2026-109449>`_
* ``symfony/http-foundation`` from v6.4.41 to v6.4.48:
  `CVE-2026-108082 <https://symfony.com/cve-2026-108082>`_
* ``symfony/yaml`` from v6.4.40 to v6.4.48:
  `CVE-2026-109413 <https://symfony.com/cve-2026-109413>`_

Since the compilation version is exposed via the eShop core
component, the CE package v7.5.2 was released to provide the
7.5.1 compilation information. The PE and EE packages were tagged
v7.5.2 as well, so that all three editions stay in sync. These
components contain **no functional changes**; the update of the
Symfony components is part of this release.

.. _packages-751:

Packages
--------

Compared to the 7.5.0 compilation, the package versions are
unchanged, except for the eShop core (CE/PE/EE), newly tagged as
v7.5.2, and the updated Symfony components mentioned above.

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop CE compilation contains, among others, the
following changed packages:

* OXID eShop CE from v7.5.1 to v7.5.2

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop PE compilation additionally contains:

* OXID eShop PE from v7.5.1 to v7.5.2

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop EE compilation additionally contains:

* OXID eShop EE from v7.5.1 to v7.5.2

Compatible OXID Extensions
--------------------------

The compatible OXID extensions are the same as for version 7.5.0.
For more information, see the Release Notes for OXID eShop
Compilation
`7.5.0 <https://docs.oxid-esales.com/eshop/en/7.5/releases/oxid-eshop-750.html>`_.

Update
------

Run the following commands to update your OXID eShop from
7.5.0 to 7.5.1:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate
