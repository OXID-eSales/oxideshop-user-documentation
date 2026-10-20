OXID eShop Compilation 7.4.4
============================

Release date: October 20, 2026


Improvements & Bug Fixes
-------------------------

Updated Symfony Components
^^^^^^^^^^^^^^^^^^^^^^^^^^

The 7.4.4 compilation is a maintenance release. It updates three
Symfony components to version v6.4.48 each. The updates contain the
fixes for the following Symfony security advisories:

* ``symfony/expression-language`` from v6.4.24 to v6.4.48:
  `CVE-2026-109449 <https://symfony.com/cve-2026-109449>`_
* ``symfony/http-foundation`` from v6.4.41 to v6.4.48:
  `CVE-2026-108082 <https://symfony.com/cve-2026-108082>`_
* ``symfony/yaml`` from v6.4.40 to v6.4.48:
  `CVE-2026-109413 <https://symfony.com/cve-2026-109413>`_

Since the compilation version is exposed via the eShop core
component, the CE package v7.4.6 was released to provide the
7.4.4 compilation information. The PE and EE packages were tagged
v7.4.6 as well, so that all three editions stay in sync. These
components contain **no functional changes**; the update of the
Symfony components is part of this release.

.. _packages-744:

Packages
--------

Compared to the 7.4.3 compilation, the package versions are
unchanged, except for the eShop core (CE/PE/EE), newly tagged as
v7.4.6, and the updated Symfony components mentioned above.

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop CE compilation contains, among others, the
following changed packages:

* OXID eShop CE from v7.4.5 to v7.4.6

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop PE compilation additionally contains:

* OXID eShop PE from v7.4.5 to v7.4.6

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop EE compilation additionally contains:

* OXID eShop EE from v7.4.5 to v7.4.6

Compatible OXID Extensions
--------------------------

The compatible OXID extensions are the same as for versions
7.4.0, 7.4.1, 7.4.2 and 7.4.3. For more information, see the
Release Notes for OXID eShop Compilation
`7.4.0 <https://docs.oxid-esales.com/eshop/en/7.4/releases/oxid-eshop-740.html>`_,
`7.4.1 <https://docs.oxid-esales.com/eshop/en/7.4/releases/oxid-eshop-741.html>`_,
`7.4.2 <https://docs.oxid-esales.com/eshop/en/7.4/releases/oxid-eshop-742.html>`_ and
`7.4.3 <https://docs.oxid-esales.com/eshop/en/7.4/releases/oxid-eshop-743.html>`_.

Update
------

Run the following commands to update your OXID eShop from
7.4.3 to 7.4.4:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate
