Spezial: von 6.1.x auf 6.2.0 aktualisieren
==========================================
Zwischenstand
Dieses Dokument beschreibt einige zusätzliche Arbeitsschritte beim Update von OXID eShop der Version 6.1.x auf 6.2.0. Es wird vorausgesetzt, dass zuvor das Standard-Update ausgeführt wurde. Mit den zusätzlichen Arbeitsschritten werden hauptsächlich Status und Einstellungen der zum Shop gehörenden Module aus der Datenbank in Konfigurationsdateien :file:`*.yml` transferiert. Die Module können anschließend wieder konfiguriert, aktiviert und deaktiviert werden.

Link zu Konfigurationsdateien: </project/module_configuration/modules_configuration>
Link zu Hintergrundinformationen: </modules/installation_setup/index>

.. |schritt| image:: ../../media/icons/schritt.jpg
              :class: no-shadow

|schritt| OXID eShop update component installieren
--------------------------------------------------
Install the `update component via composer <https://github.com/OXID-eSales/oxideshop-update-component#installation>`__
Es gibt eine OXID eShop update component.
Diese Komponente ist ein Helfer für das Upgrade der OXID eShop-Kompilierung von v6.1 auf v6.2.

|schritt| Standardkonfiguration für alle Module erstellen
---------------------------------------------------------
Install a default configuration for all modules which are currently inside the directory :file:`source/modules`. On the command line, execute the Konsolenkommando:

.. code:: bash

   oe-console oe:oxideshop-update-component:install-all-modules

After this step you can visit :menuselection:`Extension -->  Modules` and make sure, all modules which were previously installed, are listed. Also those modules should be found in the new module configuration :file:`.yml` files.

Link zu Konsolenkommandos: </modules/console>

|schritt| Status und Einstellungen aus der Datenbank übernehmen
---------------------------------------------------------------
Transfer the existing configuration (module setting values, class extension chain, which modules are active) from the database to the :file:`.yml` configuration files.

.. code:: bash

   oe-console oe:oxideshop-update-component:transfer-module-data

After this step, all modules which were previously active, should have set the option `configured` to `true` in the :file:`.yml` configuration files. Also settings you have done previously to your modules, should be visible in the OXID eShop admin and the :file:`.yml` configuration files.

|schritt| Status und Einstellungen aus der Datenbank entfernen
--------------------------------------------------------------
Remove modules data which already presents the yml files from the database to avoid duplications and errors during the module activation.

.. code:: bash

   oe-console oe:oxideshop-update-component:delete-module-data-from-database

After this step modules data should be removed from the database, modules functionality should not work anymore and all modules should have not active state.

|schritt| Module aktivieren
---------------------------
Activate all configured modules which were previously active. On the command line, execute the Konsolenkommando:

.. code:: bash

   oe-console oe:module:activate-configured-modules

After this step, all modules which were previously active, should be active and have the correct configuration set.

|schritt| OXID eShop update component deinstallieren
----------------------------------------------------
Uninstall the `update component via composer <https://github.com/OXID-eSales/oxideshop-update-component>`__ Wie, ist dort aber nicht beschrieben.

-----------------------------------------------------------------------------------------

Remove old files
----------------

There is a list of files that are not used anymore by OXID eShop, and those files can be removed manually. If you are not using them, its recommended to remove listed files.

* source/xd_receiver.htm

-----------------------------------------------------------------------------------------

Troubleshooting
---------------

Error message: Module directory of ModuleX could not be installed due to The variable $sMetadataVersion must be present in ModuleX/metadata.php and it must be a scalar.
   Up to OXID eShop 6.1, modules without a metadata version in the file :file:`metadata.php` were accepted. OXID eShop 6.2 requires to set a <metadata version <modules_skeleton_metadata_v21_structure> in ModuleX :file:`metadata.php`.

Error message: The metadata key constrains is not supported in metadata version 2.0.
   Up to OXID eShop 6.1, the array keys ``constraints`` and ``constrains`` were accepted in the file :file:`metadata.php`. OXID eShop 6.2 only allows the key `constraints`. Please refer to the metadata documentation of settings </modules/skeleton/metadataphp/amodule/settings>.

The extension chain in the OXID eShop admin in :menuselection:`Extension -->  Modules --> Installed Shop Modules` is partly highlighted red and crossed out.
   This must not be an error. Up to OXID eShop 6.1, only extensions of active modules were shown. OXID eShop 6.2 shows extensions of all installed modules (active and inactive). If a module is inactive, the extensions of this module are highlighted red and crossed out. This new behavior means, you can configure the extension chain of modules which are not activated yet.


.. Intern: oxbaiy, Status: