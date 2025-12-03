OXID eShop Compilation 7.4.0
============================

Release date: November DD, 2025

Highlights
----------

Major Changes to the Content & Media Bundle 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

OXID eShop 7.4 introduces a major update of our **Content & Media Bundle** to version 9. This includes the following extensions:

* Media Library 4
* WYSIWYG Editor 6
* Visual CMS 9 (Enterprise and Professional Edition only)

The update contains numerous feature enhancements, structural changes, and necessary bug fixes:

* New alt text feature: `Documentation [de] <https://docs.oxid-esales.com/modules/vcms/de/9.1/mediathek.html#alt-text>`__
* New configuration option to set a default media file: `Documentation [de] <https://docs.oxid-esales.com/modules/vcms/de/9.1/mediathek.html#standard-media-id>`__
* Switch to media IDs instead of URLs: `Documentation <https://docs.oxid-esales.com/modules/vcms/en/9.1/update.html#introduction-of-media-ids>`__
* New activity settings for timed widgets: `Documentation [de] <https://docs.oxid-esales.com/modules/vcms/de/9.1/funktionsbeschreibung/aktivitatszeitraum-fur-widgets.html>`__
* New row element for layouting: `Documentation <https://docs.oxid-esales.com/modules/vcms/en/9.1/functional-description.html#adding-content>`__
* Additional button to create new content: `Documentation <https://docs.oxid-esales.com/modules/vcms/en/9.1/functional-description.html#creating-new-pages>`__
* Switch from parse- to tree-style structure: `Documentation <https://docs.oxid-esales.com/modules/vcms/en/9.1/update.html#changed-code-base>`__, `developer information <https://docs.oxid-esales.com/modules/vcms/en/9.1/developer.html#preparetemplateparams-method>`__
* Row and column elements automatically adjust their height.
* Bootstrap 5 for the Visual CMS workspace in the administration area.
* Refactoring and separation of some large files.

The update to **Content & Media Bundle 9** requires migration of existing content. If you wish to stay on the previous version, **Content & Media Bundle 8**, you can do so by preconfiguring your update. Please see our :doc:`Update Manual <../installation/update>` for the necessary steps.

For more information about the updated **Content & Media Bundle 9**, you can check out our news section or dive deeper into the corresponding documentation.

.. note::
    The major update of our **Content & Media Bundle** is a huge step forward and provides a more stable and better maintainable base for future changes.
    
    The architectural improvements in Visual CMS 9 may require adjustments to Visual CMS extensions, such as custom widgets. **Visual CMS 10** (included in **OXID eShop 7.5**) will bring further architectural changes to complete the modernization.

    We are happy to get **feedback** from you to improve the extensions continuously.

Better User Experience
^^^^^^^^^^^^^^^^^^^^^^

Several improvements were done to enhance the **user experience** for customers visiting the shop. Some examples are:

* Increased visibility for contact form submission confirmation.
* No checkout interruption when using the browser's back button.
* Correct feedback on wrong password when changing the email address.
* Updated explanations and translations.

For more details, please follow the links in the sections :ref:`Tweaks & Bugfixes <fixes>` and :ref:`Packages <packages>`.

Vite for APEX
^^^^^^^^^^^^^

The frontend build tool Grunt was already replaced with `Vite <https://vite.dev/>`_ for Visual CMS. From now on OXID eShop's standard theme, **APEX**, also uses Vite.

MySQL 8.4 Support
^^^^^^^^^^^^^^^^^

The OXID eShop 7.4 Compilation and all extensions listed below have been successfully tested with **MySQL 8.4 (LTS)**. This confirms that they support this long-term support MySQL version.

.. _fixes:

Tweaks & Bugfixes
-----------------

* #0007848 Visual CMS Demodata misses design information: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7848>`_
* #0007847 Translations for skipping discounts are incorrect: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7847>`_
* #0007846 Visual CMS setup fails during npm install and build: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7846>`_
* #0007845 Visual CMS preview mode always uses default language: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7845>`_
* #0007844 Coupon option Calculate only once is only for products: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7844>`_
* #0007843 Large space under menu: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7843>`_
* #0007842 YUI library is discontinued and outdated: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7842>`_
* #0007841 TemplateChainResolver is inefficient: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7841>`_
* #0007840 GraphQL products query is missing a pagination filter: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7840>`_
* #0007839 APEX theme still uses Grunt instead of Vite: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7839>`_
* #0007838 The OE Console command to create an admin user does not check if the user already exists: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7838>`_
* #0007721 The order comment is always 1 if no input is sent: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7721>`_
* #0007708 The product's dropdown is not working in checkout step 4: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7708>`_
* #0007689 The Visual CMS product widget ignores the active/inactive state: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7689>`_
* #0007622 A text overflow in Visual CMS breaks the shop: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7622>`_
* #0007293 Notice and wish lists are lost when the shopping cart reservation is activated and the reservation expires: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7293>`_
* #0007205 VAT-ID Check not working for added countries: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7205>`_
* #0007104 WYSIWYG Editor steals focus when initialized: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7104>`_
* #0007097 Duplicated URL param editlanguage in AJAX call: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7097>`_
* #0007004 Browser's back button stops checkout process: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7004>`_
* #0006917 The disclaimer for downloads is not displayed correctly: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=6917>`_
* #0006144 Missing div-element in setup: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=6144>`_
* #0006031 It's not clear for users that contact form has been sent: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=6031>`_
* #0006026 An incorrect password when changing the email address leads to a misleading message that the email is incorrect: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=6026>`_
* #0005798 Attribute creation in new window doesn't work: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=5798>`_
* #0005244 Method getAvailableInLangs cannot handle lowercase database fields: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=5244>`_
* #0005242 The rewrite rules prevent the use of some brand names: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=5242>`_
* #0002777 When resubscribing to the newsletter, the database value is incorrect: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=2777>`_

.. _packages:

Packages
--------

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop CE compilation includes the following packages:

* APEX Theme from v2.1.0 to v3.0.2: `Changelog <https://github.com/OXID-eSales/apex-theme/blob/v3.0.2/CHANGELOG-3.x.md>`_
* Eye-Able Assist v3.0.3: `Changelog <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/blob/v3.0.3/CHANGELOG.md>`_
* GDPR Opt-In Module from v4.2.0 to v4.3.0: `Changelog <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.3.0/CHANGELOG.md>`_
* Makaira Connect Essential from 2.1.3 to 2.1.4: `Changelog <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.4/CHANGELOG.md>`_
* Media Library Module from v3.0.0 to v4.1.0 (or stay on v3.0.0): `Changelog <https://github.com/OXID-eSales/media-library-module/blob/v4.1.0/CHANGELOG.md>`_
* OXID Cookie Management powered by Usercentrics from v3.1.0 to v3.2.1: `Changelog <https://github.com/OXID-eSales/usercentrics/blob/v3.2.1/CHANGELOG.md>`_
* OXID eShop CE from v7.3.0 to v7.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.4.0/CHANGELOG-7.4.md>`_
* OXID eShop Composer Plugin v7.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.3.0/CHANGELOG-7.x.md>`_
* OXID eShop Demodata CE from v8.0.2 to v8.1.0: `Changelog <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.1.0/CHANGELOG.md>`_
* OXID eShop Demodata Installer v3.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_
* OXID eShop Doctrine Migration Wrapper v5.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.4.0/CHANGELOG-5.x.md>`_
* OXID eShop Facts v4.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.3.0/CHANGELOG-4.x.md>`_
* OXID eShop Unified Namespace Generator v5.2.0: `Changelog <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.2.0/CHANGELOG.md>`_
* OXID eShop Views Generator v2.2.0: `Changelog <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* Twig Admin Theme from v2.6.1 to v3.0.1: `Changelog <https://github.com/OXID-eSales/twig-admin-theme/blob/v3.0.1/CHANGELOG-3.x.md>`_
* Twig Component from v2.6.0 to v2.7.0: `Changelog <https://github.com/OXID-eSales/twig-component/blob/v2.7.0/CHANGELOG-2.x.md>`_
* WYSIWYG Editor Module from v5.0.0 to v6.0.1 (or to v5.0.1): `Changelog <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v6.0.1/CHANGELOG.md>`_

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop PE compilation includes the following additional packages:

* OXID eShop Demodata PE from v8.0.2 to v8.1.0
* OXID eShop PE from v7.3.0 to v7.4.0
* Twig Component PE v2.5.0
* Visual CMS Module from v8.0.1 to v9.1.0 (or to v8.0.2)

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop EE compilation includes the following additional packages:

* OXID eShop Demodata EE from v8.1.0 to v8.2.0
* OXID eShop EE from v7.3.0 to v7.4.0
* Twig Component EE v2.5.0

OXID eShop EE B2B Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The OXID eShop EE B2B compilation includes the following additional packages:

* OXID eShop B2B Approval Procedure Module from v7.3.0 to v7.4.0
* OXID eShop B2B Basket Module from v7.3.0 to v7.4.0
* OXID eShop B2B Budget Module from v7.3.0 to v7.4.0
* OXID eShop B2B Bulk Orders Module from v7.3.0 to v7.4.0
* OXID eShop B2B Buying Agent Module from v7.3.0 to v7.4.0
* OXID eShop B2B Custom Prices Module from v7.3.0 to v7.4.0
* OXID eShop B2B Offers Module from v7.3.0 to v7.4.0
* OXID eShop B2B Quick Orders Module from v7.3.0 to v7.4.0
* OXID eShop B2B Scheduled Orders Module from v7.3.0 to v7.4.0
* OXID eShop B2B Service Products Module from v7.3.0 to v7.4.0
* OXID eShop B2B Services Module from v7.3.0 to v7.4.0

For more information about B2B edition releases, see the (password-protected) documentation `OXID eShop Enterprise B2B Edition <https://docs.oxid-esales.com/b2b/en/7.3/releases/b2b-edition-730.html>`_.

Compatible OXID Extensions
--------------------------

* OXAPI GraphQL Base Module 12.0: `Documentation <https://docs.oxid-esales.com/interfaces/graphql/en/12.0/>`_
* OXAPI GraphQL Configuration Access Module 3.0: `Documentation <https://docs.oxid-esales.com/interfaces/graphql/en/12.0/>`_
* OXAPI GraphQL Storefront Module 4.2: `Documentation <https://docs.oxid-esales.com/interfaces/graphql/en/12.0/>`_
* OXAPI GraphQL Storefront Administration Module 3.0.1: `Documentation <https://docs.oxid-esales.com/interfaces/graphql/en/12.0/>`_
* OXID ERP Interface 4.3: `Documentation (password-protected) <https://docs.oxid-esales.com/interfaces/erp/en/4.3>`_
* OXID eShop Admin Tools 1.1: `Documentation <https://docs.oxid-esales.com/modules/admin-tools/en/1.1/>`_
* OXID eShop Consistency Check Tool 1.1(?TBD): `Documentation (GitHub) <https://github.com/OXID-eSales/consistency-check-tool/blob/v1.1.0/README.md>`_
* OXID eShop Country VAT Administration 2.4: `Documentation (GitHub) <https://github.com/OXID-eSales/country-vat-module/blob/v2.4.0/README.md>`_
* OXID eShop Geo-Blocking Module 2.4: `Documentation <https://docs.oxid-esales.com/modules/geo-blocking/en/2.4>`_
* OXID eShop Security Module 2.1(?TBD): `Documentation <https://docs.oxid-esales.com/modules/security/en/2.1/>`_
* OXID eShop Shipping Cost Compensation Module 1.2: `Documentation <https://docs.oxid-esales.com/modules/freeshipping-coupons/en/1.2/>`_
* OXID eShop eVAT Module 4.3: `Documentation <https://docs.oxid-esales.com/modules/vat-tbe-services/en/4.3>`_
* OXID Module Template 5.1.0: `Documentation (GitHub) <https://github.com/OXID-eSales/module-template/blob/v5.1.0/README.md>`_
* OXID Examples Module 2.0.0: `Documentation (GitHub) <https://github.com/OXID-eSales/examples-module/blob/v2.0.0/README.md>`_

Update
------

The update procedure is described step-by-step in our :doc:`Update Manual <../installation/update>`.

Installation
------------

If you prefer to do a new installation of OXID eShop 7.4, follow our :doc:`Installation Manual <../installation/new-installation/index>`.
