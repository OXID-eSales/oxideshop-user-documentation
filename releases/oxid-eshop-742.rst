OXID eShop Compilation 7.4.2
============================

Release date: TBD

Improvements & Bug Fixes
-------------------------

Composer 2.10 Compatibility
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The 7.4.2 compilation is a pure maintenance release and
contains **no functional changes**. It solely ensures that
the installation runs without complaints from the security
audit (``composer audit``) when using current Composer
versions.

Already with the 7.4.1 compilation, ``composer/composer``
was updated to 2.9.8 to establish compatibility with the
automatic security audit of Composer 2.9. With newer
Composer releases and updated security advisories, this
version could again lead to audit warnings.

In the 7.4.2 compilation, ``composer/composer`` in the CE
metapackage is therefore updated further:

* ``composer/composer`` from 2.9.8 to 2.10.2

Since the compilation version is exposed via the eShop core
component, the CE, PE, and EE packages were re-tagged to
v7.4.4 in order to provide the 7.4.2 compilation. These
re-tags contain **no functional changes**; the update of
``composer/composer`` is part of this release.

.. _packages-742:

Packages
--------

Compared to the 7.4.1 compilation, the package versions are
unchanged — except for the eShop core (CE/PE/EE), re-tagged
to v7.4.4, and the updated ``composer/composer`` package
(see above).

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop CE compilation contains, among others, the
following changed packages:

* OXID eShop CE from v7.4.2 to v7.4.4

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop PE compilation additionally contains:

* OXID eShop PE from v7.4.2 to v7.4.4

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop EE compilation additionally contains:

* OXID eShop EE from v7.4.2 to v7.4.4

Compatible OXID Extensions
--------------------------

The compatible OXID extensions are the same as for versions
7.4.0 and 7.4.1. For more information, see the Release Notes
for OXID eShop Compilation
`7.4.0 <https://docs.oxid-esales.com/eshop/en/7.4/releases/oxid-eshop-740.html>`_ and
`7.4.1 <https://docs.oxid-esales.com/eshop/en/7.4/releases/oxid-eshop-741.html>`_.

Update
------

Run the following commands to update your OXID eShop from
7.4.1 to 7.4.2:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate
