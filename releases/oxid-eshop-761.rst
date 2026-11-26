OXID eShop Compilation 7.6.1
============================

Release date: TBD


Improvements & Bug Fixes
-------------------------

Updated Symfony Components and Twig
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The 7.6.1 compilation is a maintenance release. It updates
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
* ``twig/twig`` from v3.30.0 to v3.31.1:
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
component, the CE package v7.6.1 was released to provide the
7.6.1 compilation information. The PE and EE packages were tagged
v7.6.1 as well, so that all three editions stay in sync. These
components contain **no functional changes**; the update of the
Symfony components and Twig is part of this release.

.. _packages-761:

Packages
--------

Compared to the 7.6.0 compilation, the package versions are
unchanged, except for the eShop core (CE/PE/EE), newly tagged as
v7.6.1, and the updated components mentioned above as well as the further components listed below.

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop CE compilation contains, among others, the
following changed packages:

* OXID eShop CE from v7.6.0 to v7.6.1
* ``symfony/http-foundation`` from v6.4.50 to v6.4.51

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop PE compilation additionally contains:

* OXID eShop PE from v7.6.0 to v7.6.1

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop EE compilation additionally contains:

* OXID eShop EE from v7.6.0 to v7.6.1

Compatible OXID Extensions
--------------------------

The compatible OXID extensions are the same as for version
7.6.0. For more information, see the
Release Notes for OXID eShop Compilation
`7.6.0 <https://docs.oxid-esales.com/eshop/en/7.6/releases/oxid-eshop-760.html>`_.

Update
------

Run the following commands to update your OXID eShop from
7.6.0 to 7.6.1:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-console oe:database:migrate
    ./vendor/bin/oe-eshop-db_views_generate
