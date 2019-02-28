Completing installation
=======================

Setup directory
---------------
After successful installation, the :file:`/setup` directory will be deleted automatically. This should prevent the setup process from being invoked again at a later time. Make sure that the directory has been successfully deleted.

File and directory permissions
------------------------------
To ensure error-free operation, the shop needs write permissions for some directories (file permissions for 777 or 775). Please make sure that the write permissions for the directories :file:`/out/pictures`, :file:`/out/media`, :file:`/log`, :file:`/export` and :file:`/tmp` are set, if necessary also recursively in all subdirectories.

The files :file:`.htaccess` and :file:`config.inc.php` from the main directory must be read-only after the setup has been completed (file permissions for 444).

.. Intern: oxbaag, Status: