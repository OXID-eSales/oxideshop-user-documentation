OXID eShop 7.1.0
================

Release date: 09-04-2024

The changes at a glance
-----------------------

* Security & reliability

  * PHP 8.2 support
  * Symfony 6.4 update
  * PHPUnit 10 implementation

* Accessibility

  * APEX theme WCAG (Level AA) compliant
  * Eye-Able Assist visual help for users
  * Eye-Able Assist dashboard for developers

* Visual CMS & Media Library

  * Control of allowed formats
  * Carousel widget extended
  * Syntax check for CSS/LESS
  * CSS classes for image previews
  * Simplified shortcode integration
  * English-language WYSIWYG editor
  * Support for additional file formats (SVG, AVIF, PDF, ZIP)
  * Folder function & file renaming in media library

* Improvement in the shop administration area

  * Timed-controlled products visualized

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

Barrier-free access
-------------------

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

Visual CMS & Mediathek
----------------------

Visual CMS
^^^^^^^^^^

**Improvements for editors & designers**

* Add a link for each image in the carousel widget that the visitor can click on.

  For more information, see the Visual CMS documentation under `Karussell/Slider (German) <https://docs.oxid-esales.com/modules/vcms/de/latest/funktionsbeschreibung/widgets-im-lieferumfang.html#karussell-slider>`_.

* Control the display of your thumbnails by using CSS classes.

  For more information, see the Visual CMS documentation under `Vorschaubilder (German) <https://docs.oxid-esales.com/modules/vcms/de/5.0/konfiguration.html#vorschaubilder>`_.

* Avoid possible syntax errors by using a check function when saving your CMS content.
* Use the WYSIWYG editor as an English-speaking user with English localization.

**Improvements for developers & administrators**

* Simplify the integration, decoration and extension of your shortcodes with our redesigned, clearer interface (4 methods instead of 12).

  For more information, see the Visual CMS developer documentation under `Extending the shortcode <https://docs.oxid-esales.com/modules/vcms/en/5.0/developer.html#extending-the-shortcode>`_.

  You can also use our `Example module <https://github.com/OXID-eSales/vcms-examples/blob/b-7.1.x/src/DecorationExample.php>`_ to familiarize yourself with the interface for shortcodes.

* Specify which file formats editors are allowed to upload to the media library.

  To do so, adjust the parameter :code:`aAllowedUploadTypes` in the file :file:`config.inc.php`.

  For more information, see the Visual CMS documentation under `Weitere Dateiformate zum Upload in die Mediathek erlauben (German) <https://docs.oxid-esales.com/modules/vcms/de/5.0/konfiguration.html#weitere-dateiformate-zum-upload-in-die-mediathek-erlauben>`_.

Media library
^^^^^^^^^^^^^

* Benefit from the extended support of the following moving image and vector formats:

  * AVIF:

    * Speed up the loading of your web pages by reducing the file size by 20-30% compared to WebP, while maintaining the same quality.
    * Integrate animated images into your pages via image widgets thanks to the open-source AV1 video codec.

      Compared to other formats for animated images such as GIF, APNG and WebP as well as video formats such as H.264/AVC and H.265/HEVC, AVIF generally offers improved performance and smaller file sizes.

    * Use the AVIF image format for more advanced features such as HDR and layers to improve the quality and resolution of the decoded image and provide independent layers for specific purposes.

* SVG:

  * Use images that can be scaled to any size without loss of quality.
  * Use interactive elements such as links, animations and JavaScript interactions directly within the graphic with SVG.

    In this way, create interactive diagrams, maps, infographics and other graphic elements that enable user actions.

  * Create accessible content with SVG files.

    Background: SVG files are text-based. Therefore, they can be easily interpreted by screen readers and other assistive technologies.

* To provide your customers with data sheets, technical drawings or advertising material, for example, manage PDF and ZIP file formats in addition to images.

  For more information, see the Visual CMS documentation under `Mediathek (German) <https://docs.oxid-esales.com/modules/vcms/de/5.0/funktionsbeschreibung/mediathek.html#mediathek>`_.

* Thanks to the improved generation of image previews, retain the original file format and thus also the transparency of graphics.
* Bring order to your media library with the following functions:

  * Create folders to sort media files clearly using drag-and-drop (:ref:`oxid-eshop-710-03`, item 1).
  * Change file names as required (:ref:`oxid-eshop-710-03`, item 2).

  .. _oxid-eshop-710-03:

  .. figure:: ../../media/screenshots/oxid-eshop-710-03.png
     :alt: Managing media in the media library
     :width: 650
     :class: with-shadow

     Managing media in the media library

  For more information, see the Visual CMS documentation under `Mediathek (German) <https://docs.oxid-esales.com/modules/vcms/de/5.0/funktionsbeschreibung/mediathek.html#mediathek>`_.

**More information**

For more information on changes, see the following changelogs:

* VCMS: https://github.com/OXID-eSales/visual_cms_module/blob/v5.0.0/CHANGELOG.md
* WYSIWYG editor: https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.0.0/CHANGELOG.md
* Media Library: https://github.com/OXID-eSales/media-library-module/blob/v1.0.0/CHANGELOG.md

Improvements in the OXID eShop administration area
--------------------------------------------------

Recognize time-controlled products in the product list by a separate status icon.

For more information, see the instructions about :ref:`activating time-controlled products <zeitaktivierung>` (:ref:`oxbaci02`, item 1).

New functions for developers
----------------------------

Defining dependencies between modules
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #04

We develop module packages, for example OXAPI, B2B and VisualCMS, in which modules build on each other and are dependent on provided services.

* If you as an administrator try to activate a module without fulfilled dependencies, it is displayed which modules must be activated first.

  Similarly, you cannot deactivate a module that is required by others.

* To avoid unintentional incorrect activations by administrators, as a module developer, define dependencies between modules, if necessary.

  Use this option if you have a base module with core functions that must be active for other modules to work.

  For more information see the developer documentation under `Defining dependencies between modules <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/module_dependencies.html>`_.

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