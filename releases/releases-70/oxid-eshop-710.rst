OXID eShop 7.1.0
================

Release-Datum: 26.03.2024

Die wichtigsten Änderungen im Überblick
---------------------------------------


* #tbd

  .. todo: #HR Was ist das wichtigste an 7.1?

Technologien
------------

* Unterstützung für PHP Version 8.2
* Unterstützung für PHPUnit Version 10

.. todo: #SB: verifizieren: was fehlt?
.. todo: #SB: Was folgt für den Entw. daraus, dass wir folgende Versionen nicht mehr unterstützen:
        PHP v8.0 support	DEV			#SB: how to mention
        PHPUnit v9 support	Dev			#SB: how to mention

Neue Funktionen für Anwender
----------------------------

* Time activated products have different status icons in the product list

  automatic feature: Admin | core | Performance; sth time period;  actibvate producte to be activated in time range: now with icon;

  .. todo: #tbd: Install 7.1, test function, add screenshot in docu where applicable
     Weitere Informationen finden Sie unter :ref:`tbd <tbd>`.

Neue Funktionen für Entwickler
------------------------------



Services für Subshops
^^^^^^^^^^^^^^^^^^^^^

Shops can have their own service configuration (Services für Subshops)

.. todo: #tbd: Make draft: Determine benefit, provide example, how-to

OXDEV-7468 Add documentation for shop configurable services: https://github.com/OXID-eSales/developer_documentation/commit/b638ffa84e172c8066ce35a68173fbc25d041026

Feature: You can create se. Configs, not only global; e.g. logging module;

Weitere Informationen finden Sie in der Entwickler-Dokumentation unter `tbd <https://docs.oxid-esales.com/developer/en/latest/development/testing/index.html>`_.

Abhängigkeiten zwischen Modulen definieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Definieren Sie Abhängigkeiten zwischen Modulen, falls erforderlich.

Verwenden Sie diese Option, wenn Sie ein Basismodul mit Kernfunktionen haben, die zwingend aktiv sein müssen, damit andere Module funktionieren.

Weitere Informationen finden Sie in der Entwicklerdokumentation unter `Defining dependencies between modules <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/module_dependencies.html>`_.

.. todo: #tbd: URL verifizieren


ContainerFacade
^^^^^^^^^^^^^^^

Short cut: If you need a service, you can facade,

.. todo: #DK sucht Example;

Class ContainerFacade and method Base::getService() for quick access to the DI Container from the non-DI areas

Weitere Informationen finden Sie in der Entwickler-Dokumentation unter `tbd <https://docs.oxid-esales.com/developer/en/latest/development/testing/index.html>`_.

Installing packages via the Command Line Interface
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Command bin/oe-console oe:theme:activate <theme> to activate a theme from CLI

Installing packages, muss nicht in admin, geht über cli

.. todo: #DK sucht Example; define benefit

Weitere Informationen finden Sie in der Entwickler-Dokumentation unter `tbd <https://docs.oxid-esales.com/developer/en/latest/development/testing/index.html>`_.


Clean Up
--------

Folgende veraltete (deprecated) Funktionen haben wir entfernt.

.. todo: Zur Info: getContainer() and dispatchEvent() methods in Core classes	Dev
         DK: not documented, so not to be mentioned; : deprecated as of 7.1, removed as of 8.0

.. todo: Zur Info: Global function \makeReadable(); DK: not to be mentioned in docu

.. todo: Zur Info: TemplateFileResolverInterface is redundant and will be removed in the next major version, template extension resolving is already performed in TemplateRenderer
        DK: it's a leftover: will be reomoved, not to be mentioned; Smarty Überbleibsel, DK checks

Private Sales Invite functionality (User)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


.. todo: #SB: What is the practical consequence for the shopowner/user of the function being outdated? Worum geht es dabei
.. todo: #tbd: DK provides information: ask #SB about it: as of 7.1 deprecated: removed in 8.0, may be refactored in the furture



Deprecated console classes
^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #DK/HR: What is the practical consequence of the classes being deprecated? Does the developer have to ensure that he no longer uses them?
.. todo: Info: DK: will be removed as of 8.0, as of 7.1 only deprecated: mark them as such

Deprecate console classes from the Internal namespace:

* Executor
* ExecutorInterface
* CommandsProvider
* CommandsProviderInterface


Komponenten
-----------

Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält die folgenden Komponenten (aktualisierte Versionen):

.. todo: #HR: Wann haben wir die Info?

* `OXID eShop CE 7.0.3 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.3/CHANGELOG-7.0.md#v703---2024-02-20>`_
* `OXID eShop PE 7.0.0 <https://github.com/OXID-eSales/oxideshop_pe/blob/v7.0.0/CHANGELOG.md>`_
* `OXID eShop EE 7.0.1 <https://github.com/OXID-eSales/oxideshop_ee/blob/v7.0.1/CHANGELOG.md>`_
* `Apex theme 1.2.0 <https://github.com/OXID-eSales/apex-theme/blob/v1.2.0/CHANGELOG.md>`_
* `Twig admin theme 2.2.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.2.0/CHANGELOG.md>`_
* `Twig component CE 2.2.0 <https://github.com/OXID-eSales/twig-component/blob/v2.2.0/CHANGELOG.md>`_
* `Twig component PE 2.2.0 <https://github.com/OXID-eSales/twig-component-pe/blob/v2.2.0/CHANGELOG.md>`_
* `Twig component EE 2.2.0 <https://github.com/OXID-eSales/twig-component-ee/blob/v2.2.0/CHANGELOG.md>`_

* `OXID eShop composer plugin 7.1.1 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.1.1/CHANGELOG.md>`_
* `OXID eShop Views Generator 2.1.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.1.0/CHANGELOG.md>`_
* `OXID eShop demo data installer 3.1.1 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.1.1/CHANGELOG.md>`_
* `OXID eShop demo data CE/PE/EE 8.0.0 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.0/CHANGELOG.md>`_
* `OXID eShop demo data EE 8.0.1 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.1/CHANGELOG.md>`_
* `OXID eShop doctrine migration integration 5.1.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.1.0/CHANGELOG.md>`_
* `OXID eShop facts 4.1.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.1.0/CHANGELOG.md>`_
* `Unified Namespace Generator 4.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v4.1.0/CHANGELOG.md>`_

* `GDPR Opt-In 3.0.1 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v3.0.1/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 2.0.2 <https://github.com/OXID-eSales/usercentrics/blob/v2.0.2/CHANGELOG.md>`_
* `Visual CMS 4.0.2 <https://github.com/OXID-eSales/visual_cms_module/blob/v4.0.2/CHANGELOG-4.0.md>`_ (PE/EE)
* `WYSIWYG Editor + Media Library 3.0.2 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v3.0.2/CHANGELOG.md>`_
* `Makaira 2.1.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.2/CHANGELOG.md>`_


Korrekturen
-----------

.. todo: #HR: Welche Tracking ID?
        Wrong property "_oUserData" used in ContactController PR-918	RN			Bug tacking

* https://bugs.oxid-esales.com/changelog_page.php?version_id=tbd

.. todo: #HR: Welche Tracking ID?
        Can't use dot character for template file names	RN			Bug tacking

* https://bugs.oxid-esales.com/changelog_page.php?version_id=tbd

.. todo: #HR: Executing oe-console command with an invalid shop-id value will be interrupted	RN			if shop id ivalid; will just stop to work, check whether it's in the bug tracker

* https://bugs.oxid-esales.com/changelog_page.php?version_id=tbd



Installation
------------

Zum Installieren oder Aktualisieren folgen Sie den Anleitungen im Abschnitt *Installation*:

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>`  |br|
:doc:`Minor-Update installieren <../../installation/update/minor-update>`

.. Intern: , Status: