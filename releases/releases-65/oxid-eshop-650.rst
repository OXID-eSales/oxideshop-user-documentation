OXID eShop 6.5.0
================

Release date: 16/08/2022

OXID eShop 6.5.0

* supports, among others, two of our new payment modules
  |br|
  See :ref:`releases/releases-65/oxid-eshop-650:New or updated components`.
* fixes bugs
  |br|
  See :ref:`releases/releases-65/oxid-eshop-650:Corrections`.
* supports PHP 8.1
  |br|
  See :ref:`installation/new-installation/server-and-system-requirements:Server and system requirements`, section :ref:`installation/new-installation/server-and-system-requirements:PHP`.
* uses `Symfony 5.4 <https://symfony.com/releases/5.4>`_ instead of Symfony 3.4
  |br|
  Background: Symfony 3.4 is no longer supported with (security) updates and is not compatible with PHP 8.1.

  .. attention::

     **Breaking Changes**

     Check if you can still use all modules in OXID eShop 6.5.

     * Third party or custom modules

       If you use third-party or custom modules, make sure that these modules are compatible with Symfony 5.4.

     * Amazon Pay

       The previous :productname:`Amazon Pay` (Amazon Pay & Login for OXID eShop) is no longer supported by OXID eShop.

       Background: We replace :productname:`Amazon Pay` with our new module :productname:`Amazon Pay for OXID`.

       Workaround: To smoothly migrate your OXID eShop to the new module, follow the instructions at :ref:`releases/releases-65/oxid-eshop-650:Breaking Changes`.

.. important::

     **New OXID eShop Community Edition license**

     With OXID eShop version 6.5.0, the Community Edition is exclusively for non-commercial use.

     Starting on 15-08-2022, we provide you with the OXID eShop Community Edition for evaluation, testing and proof of concepts.

     For more information about the OXID eShop Community Edition License 2022, see https://github.com/OXID-eSales/oxideshop_ce/blob/b-6.5.x/LICENSE.

     To use the OXID eShop software commercially, contact OXID eSales at sales@oxid-esales.com.


Improvements and adjustments
------------------------------

View changes in the compilation in the metapackage: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v6.4.3...v6.5.0>`_.

Breaking Changes
^^^^^^^^^^^^^^^^

The previous Amazon Pay module :productname:`Amazon Pay & Login for OXID eShop` (see https://github.com/bestit/amazon-pay-oxid) is no longer part of the compilation.

We replace it with a new module :productname:`Amazon Pay for OXID` for payment and checkout with Amazon.

If you use :productname:`Amazon Pay & Login for OXID eShop`, run it in parallel together with :productname:`Amazon Pay for OXID` temporarily before updating to OXID eShop 6.5.
|br|
Parallel operation is necessary until all old orders are completed that were still made with :productname:`Amazon Pay & Login for OXID eShop`.

Do the following:

1. If you have OXID 6.0 or earlier, make an update to OXID eShop version 6.1, 6.2 or 6.3.
   |br|
   Background: Parallel operation is possible only in OXID 6.1 to OXID 6.3 versions.

#. Install and configure :productname:`Amazon Pay for OXID`.
   |br|
   For more information, see https://docs.oxid-esales.com/modules/amazon-pay/en/latest/index.html.
#. Schedule a downtime for your OXID eShop and do the following:

   * Enable :productname:`Amazon Pay for OXID` for live operation.
   * Disable all payment methods that belong to :productname:`Amazon Pay & Login for OXID eShop`.

   Result: Your customers will process future payments with :productname:`Amazon Pay for OXID`.
   |br|
   You can still monitor payments for old orders with :productname:`Amazon Pay & Login for OXID eShop`.
#. Once all old orders are processed, do the following:

   a. Disable :productname:`Amazon Pay & Login for OXID eShop`.
   #. Perform the update to OXID eShop 6.5.



New or updated components
^^^^^^^^^^^^^^^^^^^^^^^^^

The following components and modules have been updated or added:

* OXID eShop CE (Update from 6.10.3 to 6.11.0) `Changelog 6.11.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.11.0/CHANGELOG.md>`_
* Theme "Flow" (Update from 3.8.0 to 3.8.1):  `Changelog 3.8.1 <https://github.com/OXID-eSales/flow_theme/blob/v3.8.1/CHANGELOG.md>`_
* Theme "Wave" (Update from 1.6.1 to 1.6.2):  `Changelog 1.6.2 <https://github.com/OXID-eSales/wave-theme/blob/v1.6.2/CHANGELOG.md>`_
* PayPal 6.5.0 (Update from 6.4.1 to 6.5.0): `Changelog 6.5.0 <https://github.com/OXID-eSales/paypal/blob/v6.5.0/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics (Update from 1.2.0 to 1.2.1) `Changelog 1.2.1 <https://github.com/OXID-eSales/usercentrics/blob/v1.2.1/CHANGELOG.md>`_
* PAYONE (Update from 1.6.2 to 1.7.0) `Changelog 1.7.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.7.0/Changelog.txt>`_
* Klarna (Update from 5.5.2 to 5.5.3) `Changelog 5.5.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.3/CHANGELOG.md>`_
* New: Makaira (1.4.1) `Changelog 1.4.1 <https://github.com/MakairaIO/oxid-connect-essential/blob/stable/CHANGELOG.md>`_
* New: Unzer Payment für OXID (Version 1.0 as Release Candidate for the OXID eShop Enterprise Edition): `Changelog 1.0 <https://github.com/OXID-eSales/unzer-module/blob/b-6.3.x/CHANGELOG.md>`_
  |br|
  For more information about our new payment module, see https://docs.oxid-esales.com/modules/unzer/en/latest/index.html.
* New: Amazon Pay für OXID (Version 1.2.0) `Changelog 1.2.0 <https://github.com/OXID-eSales/amazon-pay-module/blob/b-6.2.x/CHANGELOG.md>`_
  |br|
  For more information about our new payment module, see https://docs.oxid-esales.com/modules/amazon-pay/en/latest/.

Compilation components
^^^^^^^^^^^^^^^^^^^^^^

The compilation contains the following components:

* OXID eShop CE 6.11.0: `Changelog 6.11.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.11.0/CHANGELOG.md>`_
* OXID eShop composer plugin 5.2.2) `Changelog 5.2.2 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v5.2.2/CHANGELOG.md>`_
* Theme "Flow" 3.8.1: `Changelog 3.8.1 <https://github.com/OXID-eSales/flow_theme/blob/v3.8.1/CHANGELOG.md>`_
* Theme "Wave" 1.6.2: `Changelog 1.6.2 <https://github.com/OXID-eSales/wave-theme/blob/v1.6.2/CHANGELOG.md>`_
* GDPR Opt-In 2.3.3: `Changelog 2.3.3 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.3/CHANGELOG.md>`_
* Klarna 5.5.3: `Changelog 5.5.3 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.5.3/CHANGELOG.md>`_
* OXID Cookie Management powered by usercentrics 1.2.1: `Changelog 1.2.1 <https://github.com/OXID-eSales/usercentrics/blob/v1.2.1/CHANGELOG.md>`_
* PAYONE 1.7.0: `Changelog 1.7.0 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.7.0/Changelog.txt>`_
* PayPal 6.5.0: `Changelog 6.5.0 <https://github.com/OXID-eSales/paypal/blob/v6.5.0/CHANGELOG.md>`_
* WYSIWYG Editor + Mediathek 2.4.1: `Changelog 2.4.1 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v2.4.1/CHANGELOG.md>`_
* Makaira (1.4.1) `Changelog 1.4.1 <https://github.com/MakairaIO/oxid-connect-essential/blob/stable/CHANGELOG.md>`_
* Unzer (RC Version 1.0, EE): `Changelog 1.0 <https://github.com/OXID-eSales/unzer-module/blob/b-6.3.x/CHANGELOG.md>`_
* Amazon Pay für OXID (Version 1.2.0): `Changelog 1.2.0 <https://github.com/OXID-eSales/amazon-pay-module/blob/b-6.2.x/CHANGELOG.md>`_

Other Modules
^^^^^^^^^^^^^

Install the following modules manually if required.

* OXID Econda Analytics (EE) 1.3.0: `Changelog 1.3.0 <https://github.com/OXID-eSales/econda-analytics-module/blob/v1.3.0/CHANGELOG.md>`_
* Geo blocking 1.1.0: `Changelog 1.1.0 <https://github.com/OXID-eSales/geo-blocking-module/blob/v1.1.0/CHANGELOG.md>`_
* Country VAT Administration 1.0.3: `Changelog 1.0.3 <https://github.com/OXID-eSales/country-vat-module/blob/v1.0.3/CHANGELOG.md>`_
* GraphQL 6.0.1: `Changelog 6.0.1 <https://github.com/OXID-eSales/graphql-base-module/blob/v6.0.1/CHANGELOG-v6.md>`_

Corrections
-----------

Find corrections in our bug tracking system under https://bugs.oxid-esales.com/changelog_page.php?version_id=670.


Installation
------------

To install or upgrade, follow the instructions in the *Installation* section:


:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing a minor update <../../installation/update/minor-update>` |br|
:doc:`Installing a patch update <../../installation/update/patch-update>`

.. Intern: , Status:
