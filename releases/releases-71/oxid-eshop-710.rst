OXID eShop 7.1.0
================

Release date: 09-04-2024

The most important changes at a glance
---------------------------------------

* Security & reliability

  * PHP 8.2 support
  * Symfony 6.4 update
  * PHPUnit 10 implementation

* Accessibility

  * APEX theme WCAG (Level AA) compliant
  * Eye-Able Assist visual help for users
  * Eye-Able Assist dashboard for developers

* New Visual CMS user functions

  * Extended Media library (SVG, AVIF, PDF, ZIP)
  * Folder function & file renaming in Media library
  * CSS classes for image control

* Visual CMS code improvements

  * Carousel widget extended
  * Configuration of allowed file formats
  * Simplified shortcode integration
  * Syntax check for CSS/LESS

* Developer functions

  * Module dependencies
  * Symfony DI container usage
  * Console command for theme activation

Safety and reliability
----------------------

We have improved the compatibility of the OXID eShop to ensure both security and performance:

* Support for PHP 8.2 ensures up-to-date and secure software environments.

  For more information on the lifecycle of PHP versions, please visit `php.net/supported-versions.php <https://www.php.net/supported-versions.php>`_.

  Note: The :productname:`OXID eShop` 7.1 supports PHP 8.1/8.2.

* An update to Symfony 6.4 ensures compatibility with PHP 8.2 and provides a future-proof basis for our system.

* The implementation of PHPUnit 10 enables modern testing and quality assurance to further increase the reliability of the :productname:`OXID eShop`.

New functions for users
----------------------------

Enabling barrier-free access
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Accessible APEX Theme**

Increase the usability and accessibility of your OXID eShop for the visually impaired with the improved APEX theme.

We have ensured that the APEX theme is accessible according to `Web Content Accessibility Guidelines (WCAG) (Level AA) <https://www.w3.org/WAI/WCAG2AA-Conformance>`_.

Our improvements include increased contrast, optimized alt attributes for more meaningful image descriptions, frames with readable names that simplify navigation, and comprehensive screen reader compatibility that ensures a smooth browsing experience for the visually impaired.

**Eye-Able Visual Aid**

Provide your customers with a visual aid to increase the readability of your eShop when needed.

To do this, activate the Eye-Able Assist module. An icon :guilabel:`Visual Help` (:ref:`oxid-eshop-710-02`, item 1) will then appear at the bottom right of the screen. This opens a menu that allows you, for example, to adjust the character size, contrast and so on.

.. _oxid-eshop-710-02:

.. figure:: ../../media/screenshots/oxid-eshop-710-02.png
   :alt: Eye-Able: Visual Help icon
   :width: 650
   :class: with-shadow

   Fig.: Eye-Able: Visual Help icon

**Using the Eye-Able short report and dashboard**

Ensure that more customers can use your :productname:`OXID eShop` by increasing digital accessibility.

To do this, implement the accessibility guidelines in accordance with the `Disability Equality Act (BFSG) <https://www.bmas.de/DE/Soziales/Teilhabe-und-Inklusion/Rehabilitation-und-Teilhabe/behindertengleichstellungsgesetz.html>`_ and the `Web Content Accessibility Guidelines (WCAG) <https://www.w3.org/WAI/WCAG2AA-Conformance>`_.

1. Determine the possible need for optimization with the free trial version of the Eye-Able Assist module.

   Eye-Able Assist establishes a connection to your eShop, determines the number of possible improvements and displays them in the administrator area of your :productname:`OXID eShop` as an Eye-Able teaser report (:ref:`oxid-eshop-710-01`, item 1).

   .. _oxid-eshop-710-01:

   .. figure:: ../../media/screenshots/oxid-eshop-710-01.png
      :alt: Eye-Able teaser report generation
      :width: 650
      :class: with-shadow

      Fig.: Eye-Able teaser report generation

2. If the Eye-Able teaser report shows that your OXID eShop has potential for optimization in terms of accessibility, do the following:

   1. License the Eye-Able Assist full version.
   #. Ensure the accessibility of your OXID eShop with the help of the Eye-Able dashboard.

   For more information, see

   * https://dashboard.eye-able.com/demo
   * https://eye-able.com/software-services/
   * https://github.com/Tobias-Eye-Able/eye-able-oxid-module

.. note::

   You can install the Eye-Able module from :productname:`OXID eShop` 6.5.

   For more information on manual installation, see the `Readme file <https://github.com/Tobias-Eye-Able/eye-able-oxid-module?tab=readme-ov-file#installation-process>`_.

Editing texts and managing media with Visual CMS
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We have developed the media library into a stand-alone module. Like the WYSIWYG editor, the module is included as standard from the :productname:`OXID eShop Community Edition`.

To make it easier for you to get started, we have enriched our documentation with practical examples.

**Media Library Module for OXID eShop**

The new media library offers you the following advantages:

* Benefit from support for the following image and moving image formats:

  * SVG
  * AVIF:

  * Speed up the loading of your web pages thanks to the higher compression compared to WebP.
    * Integrate animations via widgets.

* Create images in better quality and in a simpler way:

  * Generate thumbnails for your images in SVG format.
  * Generate thumbnails with transparency.

* Provide your customers with data sheets, technical drawings or advertising material, for example.

  To do this, manage the following files in the following formats in your media library. Then include these files in the source code:

  * PDF
  * ZIP

  For more information, see the VCMS documentation under `Mediathek (German) <https://docs.oxid-esales.com/modules/vcms/de/5.0/funktionsbeschreibung/mediathek.html#mediathek>`_.

* Keep your media library tidy. For this purpose, we have implemented the following functions:

  * Create folders to sort media files, using drag & drop (:ref:`oxid-eshop-710-03`, item 1).

  * Change file names if required (:ref:`oxid-eshop-710-03`, item 2).

  .. _oxid-eshop-710-03:

  .. figure:: ../../media/screenshots/oxid-eshop-710-03.png
     :alt: Managing media in the media library
     :width: 650
     :class: with-shadow

     Managing media in the media library

  For more information, see the VCMS documentation under `Mediathek (German) <https://docs.oxid-esales.com/modules/vcms/de/5.0/funktionsbeschreibung/mediathek.html#mediathek>`_.

**Visual CMS**

* Control the display of your images via CSS classes:

  For more information, see the VCMS documentation under `Individuelles CSS/LESS (German) <https://docs.oxid-esales.com/modules/vcms/de/5.0/funktionsbeschreibung/grundfunktionen.html#individuelles-css-less>`_.

**VCMS code improvements**

With :productname:`OXID eShop` version 7.1 we have improved the code to make the module more powerful for future requirements.

* Provide a link for each image in the carousel that the visitor can click on: We have extended the carousel widget accordingly.

  For more information, see the VCMS documentation under `Karussell/Slider (German) <https://docs.oxid-esales.com/modules/vcms/de/latest/funktionsbeschreibung/widgets-im-lieferumfang.html#karussell-slider>`_.

* Extend shortcodes more easily. To make it easier for you to integrate them, we have made the interface for integrating new shortcodes clearer and simpler (4 instead of 12 methods).

  For more information, see the VCMS developer documentation under `Extending the shortcode <https://github.com/OXID-eSales/vcms-documentation/blob/5.0-en/developer.rst#extending-the-shortcode>`_.

  Use our `Example module <https://github.com/OXID-eSales/vcms-examples/blob/b-7.1.x/src/DecorationExample.php>`_ to familiarize yourself with extending existing shortcodes.

* Increase the robustness of your eShop by specifying as administrator which formats you want to allow for uploading.

  To do this, in the :file:`config.inc.php` file, adjust the :code:`aAllowedUploadTypes` parameter.

  For more information, see the VCMS documentation under `Weitere Dateiformate zum Upload in die Mediathek erlauben (German) <https://docs.oxid-esales.com/modules/vcms/de/5.0/konfiguration.html#weitere-dateiformate-zum-upload-in-die-mediathek-erlauben>`_.

* Optimize your content seamlessly: When saving, a check function detects possible syntax errors in your CSS/LESS.
* As an English-speaking user, use the WYSIWYG editor with English localization.

**More information**

For more information about installation, see the VCMS documentation under `Neuinstallation (German) <https://docs.oxid-esales.com/modules/vcms/de/5.0/installation.html#neuinstallation>`_.

For more information on changes, see the following changelogs:

* VCMS: https://github.com/OXID-eSales/visual_cms_module/blob/v5.0.0/CHANGELOG.md
* WYSIWYG editor: https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.0.0/CHANGELOG.md
* Media Library: https://github.com/OXID-eSales/media-library-module/blob/v1.0.0/CHANGELOG.md

Distinguishing time-controlled products more easily
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Time-controlled products have a separate status icon in the product list.

For more information, see the instructions about :ref:`activating time-controlled products <zeitaktivierung>` (:ref:`oxbaci02`, item 1).

New functions for developers
------------------------------

Defining dependencies between modules
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #04

We develop module packages, for example OXAPI, B2B and VisualCMS, in which modules build on each other and are dependent on provided services.

* If you as an administrator try to activate a module without fulfilled dependencies, it is displayed which modules must be activated first.

  Similarly, you cannot deactivate a module that is required by others.

* To avoid unintentional incorrect activations by administrators, as a module developer, define dependencies between modules, if necessary.

  Use this option if you have a base module with core functions that must be active for other modules to work.

  For more informationsee the the developer documentation under `Defining dependencies between modules <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/module_dependencies.html>`_.

.. todo: #tbd: Verify URL

Using Symfony DI containers
^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Configuring services individually for each subshop

  .. todo: #03 #tbd: verify URLs when published

  Overwrite the services used by the OXID eShop  for each subshop.

  The Symfony DI container in the OXID eShop allows you to manage services even more flexibly and efficiently.

  For more information about Symfony DI containers for customizing and managing services, see the developer documentation under `Service Container <https://docs.oxid-esales.com/development/tell_me_about/service_container.html>`_.

* Using services in non-DI classes

  .. todo: #01; #tbd: verify URLs when published

  Make your work as a module developer easier by accessing the central Symfony DI container even in areas that are not intended for dependency injection (DI).

  For more information, see the developer documentation under `Use services in non-DI classes <https://docs.oxid-esales.com/development/modules_components_themes/module/module_services.rst#use-services-in-non-di-classes.html>`_.

Installing packages via the command line interface
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #02

To activate a theme, you do not need to use the administrator interface in your :productname:`OXID eShop`.

Use the :code:`./vendor/bin/oe-console oe:theme:activate <theme>` command.

For more information, see the developer documentation under

* `Activation <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/theme/theme_activation_via_cli.html>`_
* `Activating the frontend theme <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/twig_template_engine/installation.html#after-twig-engine-installation>`_

Clean Up
--------


Invite function
^^^^^^^^^^^^^^^

.. todo: #07

To offer your registered customers the option of inviting friends and receiving bonus points in return, up to version 7.0 of the OXID eShop you could activate the Invitations function under :menuselection:`Master Settings --> Core settings --> Settings --> Invitations`. --> Invitations` to activate the :guilabel:`Invitations` function.

However, due to the risk of misuse by spam attacks, we have decided to remove this function from the user interface. It's still in the 7.x code base. It will be removed as of 8.0.

Deprecated console classes
^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #06

The following console classes from the internal namespace are marked as obsolete and will be removed in the next major release.

Check your code to see if and where you are using the classes marked as obsolete.

After updating your code to replace the deprecated classes, if necessary, run tests to ensure that your applications continue to work as expected.

* :code:`Executor`
* :code:`ExecutorInterface`
* :code:`CommandsProvider`
* :code:`CommandsProviderInterface`

Components
----------

Repositories without link are private.

Changed Components of the compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We have updated the following components and modules.

* New: `Eye-Able 3.0.1 <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/tree/v3.0.1>`_
* `OXID eShop CE (update from 7.0.4 to 7.1.0) <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.1.0/CHANGELOG-7.1.md>`_
* `Twig component (update from 2.2.0 to 2.4.0) <https://github.com/OXID-eSales/twig-component/blob/v2.4.0/CHANGELOG-2.x.md>`_
* `OXID eShop composer plugin (update from 7.1.1 to 7.2.0) <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.2.0/CHANGELOG-7.x.md>`_
* `OXID eShop Views Generator (update from 2.1.0 to 2.2.0) <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* `OXID eShop DemoData installer (update from 3.1.1 to 3.2.0) <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.2.0/CHANGELOG-3.x.md>`_
* `OXID eShop demodata CE (update from 8.0.0 to 8.0.1) <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.1/CHANGELOG.md>`_
* `OXID eShop doctrine migration integration (update from 5.1.0 to 5.2.0) <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.2.0/CHANGELOG-5.x.md>`_
* `OXID eShop facts (update from 4.1.0 to 4.2.0) <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.2.0/CHANGELOG-4.x.md>`_
* `Unified Namespace Generator (update from 4.1.0 to 5.0.0) <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.0.0/CHANGELOG.md>`_

* OXID eShop PE (update from 7.0.0 to 7.1.0)
* Twig component for Professional Edition (update from 2.2.0 to 2.4.0)
* OXID eShop demodata PE (update from 8.0.0 to 8.0.1)

* OXID eShop EE (update from 7.0.1 to 7.1.0)
* Twig component for Enterprise Edition (update from 2.2.0 to 2.4.0)
* OXID eShop demodata EE (update from 8.0.1 to to 8.0.2)

* `APEX Theme (update from 1.2.1 to 1.3.0) <https://github.com/OXID-eSales/apex-theme/blob/v1.3.0/CHANGELOG-1.x.md>`_

* `WYSIWYG Editor(update from 3.0.2 to 4.0.0): ) <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.0.0/CHANGELOG.md>`_
* New (extracted from the WYSIWYG Editor): `Media Library (1.0.0) <https://github.com/OXID-eSales/media-library-module/blob/v1.0.0/CHANGELOG.md>`_
* Visual CMS (update from 4.0.2 to 5.0.1)

* `GDPR opt-in module (update from 3.0.1 to 4.0.0) <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.0.0/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics (update from 2.0.2 to 3.0.0) <https://github.com/OXID-eSales/usercentrics/blob/v3.0.0/CHANGELOG.md>`_

Components of the compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The compilation contains the following components (current versions):

* `OXID eShop CE 7.1.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.1.0/CHANGELOG-7.1.md>`_
* OXID eShop PE 7.1.0
* OXID eShop EE 7.1.1

* `Apex theme 1.3.0 <https://github.com/OXID-eSales/apex-theme/blob/v1.3.0/CHANGELOG-1.x.md>`_

* `Twig admin theme 2.2.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.2.0/CHANGELOG.md>`_
* `Twig component CE 2.4.0 <https://github.com/OXID-eSales/twig-component/blob/v2.4.0/CHANGELOG-2.x.md>`_
* Twig component PE 2.4.0
* Twig component EE 2.4.0

* `OXID eShop composer plugin 7.2.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.2.0/CHANGELOG-7.x.md>`_
* `OXID eShop Views Generator 2.2.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* `OXID eShop demo data installer 3.2.0 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.2.0/CHANGELOG-3.x.md>`_

* `OXID eShop demo data CE 8.0.1 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.1/CHANGELOG.md>`_
* OXID eShop demo data PE 8.0.1
* OXID eShop demo data EE 8.0.2

* `OXID eShop doctrine migration integration 5.2.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.2.0/CHANGELOG-5.x.md>`_
* `OXID eShop facts 4.2.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.2.0/CHANGELOG-4.x.md>`_
* `Unified Namespace Generator 5.0.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.0.0/CHANGELOG.md>`_

* `GDPR Opt-In 4.0.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.0.0/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 3.0.0 <https://github.com/OXID-eSales/usercentrics/blob/v3.0.0/CHANGELOG.md>`_
* Visual CMS 5.0.1 (PE/EE)

* `WYSIWYG Editor 4.0.0 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.0.0/CHANGELOG.md>`_
* `Media Library (1.0.0) <https://github.com/OXID-eSales/media-library-module/blob/v1.0.0/CHANGELOG.md>`_
* `Makaira 2.1.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.2/CHANGELOG.md>`_
* `Eye-Able 3.0.1 <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/tree/v3.0.1>`_


Corrections
-----------

Find the corrections in the `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.1.x/CHANGELOG-7.1.md>`_.

Installation
------------

To install or upgrade, follow the instructions in the *Installation* section:

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Installing a minor update <../../installation/update/minor-update>`

.. Intern: , Status: