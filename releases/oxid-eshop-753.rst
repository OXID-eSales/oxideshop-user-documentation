OXID eShop Compilation 7.5.3
============================

Release date: TBD


Improvements & Bug Fixes
-------------------------

Updated Symfony Components and Twig
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The 7.5.3 compilation is a maintenance release. It updates
Symfony components and Twig. The updates contain the fixes for the
following security advisories:

* ``symfony/expression-language`` from v6.4.48 to v6.4.51:
  `CVE-2026-133760 <https://github.com/symfony/symfony/security/advisories/GHSA-fvvg-g68p-p6q9>`_
* ``symfony/html-sanitizer`` from v6.4.50 to v6.4.51:
  `CVE-2026-133756 <https://github.com/symfony/symfony/security/advisories/GHSA-wccc-v7v7-gc54>`_
* ``symfony/http-kernel`` from v6.4.50 to v6.4.51:
  `CVE-2026-133743 <https://github.com/symfony/symfony/security/advisories/GHSA-8cww-v5fg-2mf9>`_
* ``symfony/routing`` from v6.4.50 to v6.4.51:
  `CVE-2026-133746 <https://github.com/symfony/symfony/security/advisories/GHSA-cpx6-mpfq-c6cr>`_,
  `CVE-2026-133754 <https://github.com/symfony/symfony/security/advisories/GHSA-wgv4-frv7-c8c5>`_
* ``twig/twig`` from v3.27.0 to v3.31.1:
  `CVE-2026-133763 <https://github.com/twigphp/Twig/security/advisories/GHSA-567w-cx2v-jc85>`_,
  `CVE-2026-133764 <https://github.com/twigphp/Twig/security/advisories/GHSA-rc9g-xwx4-rmfh>`_,
  `CVE-2026-133765 <https://github.com/twigphp/Twig/security/advisories/GHSA-ccrc-gqhf-3cxc>`_,
  `CVE-2026-133766 <https://github.com/twigphp/Twig/security/advisories/GHSA-56wp-8m9q-4354>`_,
  `CVE-2026-133767 <https://github.com/twigphp/Twig/security/advisories/GHSA-fmp9-6wxr-cfmq>`_,
  `CVE-2026-133768 <https://github.com/twigphp/Twig/security/advisories/GHSA-p2x6-ppf3-32r3>`_,
  `CVE-2026-133770 <https://github.com/twigphp/Twig/security/advisories/GHSA-r34x-hh9h-9q9c>`_,
  `CVE-2026-133771 <https://github.com/twigphp/Twig/security/advisories/GHSA-63v2-9rx5-wjgr>`_,
  `CVE-2026-133772 <https://github.com/twigphp/Twig/security/advisories/GHSA-qr49-4294-4gmw>`_

Since the compilation version is exposed via the eShop core
component, the CE package v7.5.4 was released to provide the
7.5.3 compilation information. The PE and EE packages were tagged
v7.5.4 as well, so that all three editions stay in sync. These
components contain **no functional changes**; the update of the
Symfony components and Twig is part of this release.

.. _packages-753:

Packages
--------

Compared to the 7.5.2 compilation, the package versions are
unchanged, except for the eShop core (CE/PE/EE), newly tagged as
v7.5.4, and the updated components mentioned above as well as the further components listed below.

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop CE compilation contains, among others, the
following changed packages:

* OXID eShop CE from v7.5.3 to v7.5.4
* ``symfony/http-foundation`` from v6.4.50 to v6.4.51

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop PE compilation additionally contains:

* OXID eShop PE from v7.5.3 to v7.5.4

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop EE compilation additionally contains:

* OXID eShop EE from v7.5.3 to v7.5.4

Compatible OXID Extensions
--------------------------

The compatible OXID extensions are the same as for versions
7.5.0, 7.5.1 and 7.5.2. For more information, see the
Release Notes for OXID eShop Compilation
`7.5.0 <https://docs.oxid-esales.com/eshop/en/7.5/releases/oxid-eshop-750.html>`_,
`7.5.1 <https://docs.oxid-esales.com/eshop/en/7.5/releases/oxid-eshop-751.html>`_ and
`7.5.2 <https://docs.oxid-esales.com/eshop/en/7.5/releases/oxid-eshop-752.html>`_.

Update
------

Run the following commands to update your OXID eShop from
7.5.2 to 7.5.3:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate
