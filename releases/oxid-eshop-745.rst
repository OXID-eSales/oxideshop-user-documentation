OXID eShop Compilation 7.4.5
============================

Release date: TBD


Improvements & Bug Fixes
-------------------------

Updated Symfony Components
^^^^^^^^^^^^^^^^^^^^^^^^^^

The 7.4.5 compilation is a maintenance release. It updates five
Symfony components. The updates contain the fixes for the following
Symfony security advisories:

* ``symfony/config`` from v6.4.26 to v6.4.50:
  `GHSA-5jff-8h8q-r5qx <https://github.com/symfony/symfony/security/advisories/GHSA-5jff-8h8q-r5qx>`_
* ``symfony/filesystem`` from v6.4.24 to v6.4.50:
  `GHSA-6prc-h956-hxjq <https://github.com/symfony/symfony/security/advisories/GHSA-6prc-h956-hxjq>`_
* ``symfony/http-foundation`` from v6.4.48 to v6.4.50:
  `CVE-2026-118514 <https://symfony.com/cve-2026-118514>`_,
  `GHSA-3h27-hjv7-fqjx <https://github.com/symfony/symfony/security/advisories/GHSA-3h27-hjv7-fqjx>`_,
  `GHSA-5mx8-mwrp-5693 <https://github.com/symfony/symfony/security/advisories/GHSA-5mx8-mwrp-5693>`_
* ``symfony/mime`` from v6.4.40 to v6.4.49:
  `CVE-2026-45070 <https://symfony.com/cve-2026-45070>`_
* ``symfony/yaml`` from v6.4.48 to v6.4.50:
  `GHSA-hwfg-qwvh-2wfx <https://github.com/symfony/symfony/security/advisories/GHSA-hwfg-qwvh-2wfx>`_

Since the compilation version is exposed via the eShop core
component, the CE package v7.4.7 was released to provide the
7.4.5 compilation information. The PE and EE packages were tagged
v7.4.7 as well, so that all three editions stay in sync. These
components contain **no functional changes**; the update of the
Symfony components is part of this release.

.. _packages-745:

Packages
--------

Compared to the 7.4.4 compilation, the package versions are
unchanged, except for the eShop core (CE/PE/EE), newly tagged as
v7.4.7, and the updated Symfony components mentioned above.

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop CE compilation contains, among others, the
following changed packages:

* OXID eShop CE from v7.4.6 to v7.4.7

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop PE compilation additionally contains:

* OXID eShop PE from v7.4.6 to v7.4.7

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop EE compilation additionally contains:

* OXID eShop EE from v7.4.6 to v7.4.7

Compatible OXID Extensions
--------------------------

The compatible OXID extensions are the same as for versions
7.4.0, 7.4.1, 7.4.2, 7.4.3 and 7.4.4. For more information, see the
Release Notes for OXID eShop Compilation
`7.4.0 <https://docs.oxid-esales.com/eshop/en/7.4/releases/oxid-eshop-740.html>`_,
`7.4.1 <https://docs.oxid-esales.com/eshop/en/7.4/releases/oxid-eshop-741.html>`_,
`7.4.2 <https://docs.oxid-esales.com/eshop/en/7.4/releases/oxid-eshop-742.html>`_,
`7.4.3 <https://docs.oxid-esales.com/eshop/en/7.4/releases/oxid-eshop-743.html>`_ and
`7.4.4 <https://docs.oxid-esales.com/eshop/en/7.4/releases/oxid-eshop-744.html>`_.

Update
------

Run the following commands to update your OXID eShop from
7.4.4 to 7.4.5:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate
