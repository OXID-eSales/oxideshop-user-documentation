OXID eShop 6.2.0
================

Release date: 31/03/2020 |br|
Release date RC2: 26/02/2020 |br|
Release date RC1: 11/11/2019 |br|
Release date Beta 1: 02/08/2019

-----------------------------------------------------------------------------------------

General information
-------------------
OXID eShop 6.2.0 is provided as a compilation with the following components:

* OXID eShop CE 6.5.3
* OXID eShop PE 6.4.0
* OXID eShop EE 6.5.1
* Theme "Flow" 3.4.1
* Theme "Wave" 1.3.1
* Amazon Pay 3.6.4
* GDPR Opt-In 2.3.0
* Klarna 5.1.4
* Paymorrow 2.0.3
* PAYONE 1.3.1
* PayPal 6.1.0
* Summernote WYSIWIG editor and Media Gallery 2.2.0
* Visual CMS (PE/EE) 3.3.3

All changes to the compilation can be viewed in the following metapackage: `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/b-6.1...b-6.2>`_.

OXID eShop 6.2.0 contains a security improvement for the payment module PAYONE.

System requirements
^^^^^^^^^^^^^^^^^^^
OXID eShop 6.1.2 runs under PHP 7.1 to 7.4. The supported database is MySQL version 5.5 or 5.7 and MariaDB version 10.4. Using MySQL 5.6 is not recommended as it could cause issues with Enterprise Edition. Please refer to the blog post: `Set MySQL 5.6 optimizer setting "block_nested_loop = off" for OXID eShop Enterprise Edition <https://oxidforge.org/en/set-mysql-5-6-optimizer-setting-block_nested_loop-off-for-oxid-eshop-enterprise-edition.html>`_. Apache 2.2 or 2.4 can be used as a web server on a Linux system.

Installation
^^^^^^^^^^^^
The new installation and the update from 6.1.x to 6.2.0 are described in the section "Installation".

:doc:`New installation <../../installation/new-installation/new-installation>` |br|
:doc:`Update from 6.1.x to 6.2.0 <../../installation/update/update-from-6.1.x-to-6.2.0>`

During installation, the new directory :file:`/var` is created at the same level as :file:`/source` and :file:`/vendor`, to which the HTTP server and CLI user need read and write access.

Please run the update first in a test or development environment, or a copy of your current shop. Then, test the ordering process and payment and shipping methods. If the shopping cart software works correctly, you can replace it in the live system with the one from the test or development environment.

OXID eShop 6.0.* has now reached End-of-Life (EOL) and is no longer supported. Please consider to update if you still use a shop of this series.

-----------------------------------------------------------------------------------------

New Functions
-------------

Reverse Proxy NGINX
^^^^^^^^^^^^^^^^^^^
OXID eShop high load option is an add-on for the OXID eShop Enterprise Edition in version 6. Caching ensures the fast generation and delivery of HTML pages, especially during peak loads. Caching is handled by a reverse proxy, which processes incoming requests from web clients before the actual web server. The OXID eShop high load option now supports NGINX version 1.14.0 and higher as a reverse proxy, offering an alternative to the previously used Varnish.

OXID eShop console
^^^^^^^^^^^^^^^^^^
OXID eShop 6.2.0 uses the `Symfony Console <https://symfony.com/doc/current/console.html>`_. This allows developers to write, register and execute their own commands for components and modules. Information on this can be found in the developer documentation:  https://docs.oxid-esales.com/developer/en/6.2/development/tell_me_about/console.html.

Template engine Twig
^^^^^^^^^^^^^^^^^^^^
OXID eShop supports `Twig <https://twig.symfony.com>`_, a Symfony project, as an alternative template engine. Developers can decide if they want to use Twig instead of Smarty in the templates. Tools are provided for the conversion from Smarty to Twig.

Dependency Injection
^^^^^^^^^^^^^^^^^^^^
Dependency Injection (DI), a design pattern in object-oriented programming, can now be used in modules. DI is implemented in OXID eShop using the Symfony DI container. Dependency Injection means, in a nutshell, that an object that requires the functionality of another object may not instantiate the other object itself. The object is injected from outside. What Depency Injection means for project developers is presented in a three-part article at the OXIDforge: `Part 1: Basics <https://oxidforge.org/en/dependency-injection-for-project-developers.html>`_, `Part 2: Dependency Injection within Modules <https://oxidforge.org/en/part-2-dependency-injection-within-modules.html>`_ and `Part 3: Extending OXID eShop using the Symfony DI container <https://oxidforge.org/en/extending-oxid-eshop-using-the-symfony-di-container.html>`_.

Events
^^^^^^
With OXID eShop 6.2.0 an event handling is introduced, which is based on `Symfony Events and Event Listeners <https://symfony.com/doc/3.4/event_dispatcher.html>`_. First events, which have been implemented, allow a more reliable way to extend the functionality of the shop. Events are the better alternative to traditional inheritance within the class chain. They can be processed by the shop and modules. The developer documentation contains an introduction to event handling and an overview of the currently available events: https://docs.oxid-esales.com/developer/en/6.2/development/tell_me_about/event/index.html.

Doctrine SQL Query Builder
^^^^^^^^^^^^^^^^^^^^^^^^^^
The `Doctrine SQL Query Builder <https://www.doctrine-project.org/projects/doctrine-dbal/en/2.5/reference/query-builder.html#sql-query-builder>`_ can now be used in modules. Instructions for a database query can also be found in the developer documentation: https://docs.oxid-esales.com/developer/en/6.2/development/modules_components_themes/module/using_database.html#making-a-query.

.. _new-codeception:

Codeception
^^^^^^^^^^^
For OXID eShop, `Codeception acceptance tests <https://codeception.com>`_ are introduced, which are recommended for writing acceptance tests for modules of the "Flow" and "Wave" themes. For developers, these tests are easier to write, use and maintain. Another advantage is that newer drivers are supported. Detailed information can be found in the developer documentation: https://docs.oxid-esales.com/developer/en/6.2/development/modules_components_themes/module/testing/codeception/index.html.

New directory /var
^^^^^^^^^^^^^^^^^^
OXID eShop now has the new directory :file:`/var` on the same level as :file:`/source` and :file:`/vendor`. It contains the module configurations, structured by subdirectories. These are saved in .yaml files for each subshop (for an Enterprise Edition) and environment specific (production, staging, development). The directory requires recursive read and write access for HTTP server and CLI users during installation and at runtime.

Custom shop offline page
^^^^^^^^^^^^^^^^^^^^^^^^
The shop can display a user-defined shop offline page with customized layout and/or special features instead of the default page that indicates maintenance mode. This can be achieved by overwriting the method ``oxTriggerOfflinePageDisplay``.

Character set of the database connection
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the configuration file :file:`config.inc.php` the character set of the database connection can be defined by a new parameter. Example: ``$this->dbCharset = 'utf8';``

-----------------------------------------------------------------------------------------

Improvements and adjustments
----------------------------

Updated components of the OXID eShop compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The following components have been updated to a new version:

* OXID eShop CE (update from 6.3.6 to 6.5.3), `Changelog 6.5.3 <https://github.com/OXID-eSales/oxideshop_ce/blob/v6.5.3/CHANGELOG.md>`_
* OXID eShop PE (update from 6.2.2 to 6.4.0)
* OXID eShop EE (update from 6.2.3 to 6.5.1)
* Theme "Flow" (update from 3.3.0 to 3.4.1), `Changelog 3.4.1 <https://github.com/OXID-eSales/flow_theme/blob/v3.4.1/CHANGELOG.md>`_
* Theme "Wave" (update from 1.2.0 to 1.3.1), `Changelog 1.3.1 <https://github.com/OXID-eSales/wave-theme/blob/v1.3.1/CHANGELOG.md>`_
* Amazon Pay (update from 3.3.1 to 3.6.4), `Changelog 3.6.4 <https://github.com/bestit/amazon-pay-oxid/blob/3.6.4/CHANGELOG.md>`_
* GDPR Opt-In (update from 2.2.0 to 2.3.0), `Changelog 2.3.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v2.3.0/CHANGELOG.md>`_
* Klarna (update from 4.3.0 to 5.1.4), `Changelog 5.1.4 <https://github.com/topconcepts/OXID-Klarna-6/blob/v5.1.4/CHANGELOG.md>`_
* Paymorrow (update from 2.0.1 to 2.0.3), `Changelog 2.0.3 <https://github.com/OXID-eSales/paymorrow-module/blob/v2.0.3/CHANGELOG.md>`_
* PAYONE (update from 1.0.10 to 1.3.1), `Changelog v1.3.1 <https://github.com/PAYONE-GmbH/oxid-6/blob/v1.3.1/Changelog.txt>`_
* PayPal (update from 5.2.5 to 6.1.0), `Changelog 6.1.0 <https://github.com/OXID-eSales/paypal/blob/v6.1.0/CHANGELOG.md>`_
* Visual CMS (PE/EE) (update from 3.3.2 to 3.3.3), `Changelog 3.3.3 <https://github.com/OXID-eSales/visual_cms_module/blob/v3.3.3/CHANGELOG.md>`_

Sorting of accessories for products
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the assignment window for accessories, the order of the assigned products can be changed. After marking an product in the list on the right, it can be moved up or down using the mini buttons that are now displayed.

Changes in the module system
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Nowadays it is standard in large and medium-sized projects to operate OXID eShop in various environments such as integration, staging, and production. In order to easily configure modules instead of managing them separately in each environment, the module system was extended accordingly. It is now possible to manage the environment via YAML configuration files. These are stored in the new directory :file:`/var` and its structured subdirectories. For detailed information, see the developer documentation: https://docs.oxid-esales.com/developer/en/6.2/development/modules_components_themes/project/module_configuration/modules_configuration.html#configuring-module-20190910

The :file:`metadata.php` file will be validated more strictly. The version number is now mandatory and additional source code is not allowed.

Changes in the testing framework
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
There have been a number of changes in the testing framework.

* The PHPUnit component was updated from version 4.8.26 to 6. Information about added, changed and removed methods can be found in the PHPUnit changelogs: https://github.com/sebastianbergmann/phpunit/blob/6.0.0/ChangeLog-6.0.md and https://github.com/sebastianbergmann/phpunit/blob/6.0.0/ChangeLog-5.0.md.
* Codeception has been introduced for easier writing of acceptance tests, which has already been discussed in the section "New Functions", see: :ref:`new-codeception`.
* Changes in the OXID eShop testing library are documented in the changelog: https://github.com/OXID-eSales/testing_library/blob/v7.1.0/CHANGELOG.md.

Detailed information on testing modules can be found in the developer documentation: https://docs.oxid-esales.com/developer/en/6.2/development/modules_components_themes/module/testing/index.html.

Overview of all changes
^^^^^^^^^^^^^^^^^^^^^^^
Changes from the previous version of the OXID eShop component can be viewed in the Community Edition repository on GitHub: https://github.com/OXID-eSales/oxideshop_ce/compare/v6.3.6…v6.5.3. Switch to the :guilabel:`Files changed` tab to see the list of all changed files.

-----------------------------------------------------------------------------------------

Corrections
-----------

Corrections 6.2.0: https://bugs.oxid-esales.com/changelog_page.php?version_id=542 |br|
Corrections 6.2.0 RC 1: https://bugs.oxid-esales.com/changelog_page.php?version_id=529 |br|
Corrections 6.2.0 Beta 1: https://bugs.oxid-esales.com/changelog_page.php?version_id=459


.. Intern: oxbais, Status: transL