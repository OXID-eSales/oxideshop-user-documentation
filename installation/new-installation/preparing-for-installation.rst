Preparing for installation
==========================

Some preparations are necessary for the new installation of OXID eShop 6.1.

.. |schritt| image:: ../../media/icons/schritt.jpg
               :class: no-shadow

|schritt| Installing Composer
-----------------------------

OXID eShop 6 is no longer installed based on packaged and downloadable installation packages but with the help of Composer. Composer is a dependency manager for PHP, a tool that takes into account the dependencies of a project’s program components while installing the files of that project in a defined directory.

Composer is required for the new installation of OXID eShop. Installation instructions can be found in the “Getting Started” section of the Composer website: http://getcomposer.org.

|schritt| Providing shop files
------------------------------

The shop files are provided by Composer. Depending on the shop edition, different commands have to be run in the shell. The shop files are stored in a subdirectory that is specified with :command:`your_project_name` in the command. This is based on the directory in which the command is run in the shell. Specify the :command:`--no-dev` parameter if the development-related files are not required.

.. hint:: For the installation of Professional and Enterprise Edition, you will also need the login data that you received in the e-mail for the current release.

Community Edition
^^^^^^^^^^^^^^^^^

:command:`composer create-project --no-dev oxid-esales/oxideshop-project your_project_name dev-b-6.2-ce`

Professional Edition
^^^^^^^^^^^^^^^^^^^^

:command:`composer create-project --no-dev oxid-esales/oxideshop-project your_project_name dev-b-6.2-pe`

Enterprise Edition
^^^^^^^^^^^^^^^^^^

:command:`composer create-project --no-dev oxid-esales/oxideshop-project your_project_name dev-b-6.2-ee`

Once Composer has finished, the new directory named with *your_project_name* will be available. This is the main (root) directory of the project that contains all the files needed to install OXID eShop.

|schritt| Configuring Apache
----------------------------

The next step is moving the main directory to a directory that the HTTP server can access. The Apache document root directory must point to the :file:`/source` directory of the main directory.

|schritt| Customising file and directory permissions
----------------------------------------------------

The HTTP server requires read and write access to the following directories and their subdirectories at runtime:

:file:`/source/export` |br|
:file:`/source/log/` |br|
:file:`/source/out/pictures/` |br|
:file:`/source/out/media/` |br|
:file:`/source/tmp/` |br|
:file:`/var/`

The CLI user (Command Line Interface) additionally requires read and write access for the directory :file:`/var/`.

For the web-based setup, the HTTP server must have write access to the following directory and files:

:file:`/source/Setup` |br|
:file:`/source/config.inc.php` |br|
:file:`/source/.htaccess`

|schritt| Creating database
---------------------------

OXID eShop requires a MySQL database to store all products, categories, customer and order data, and other information. Most web hosts offer database access through a special website, such as phpMyAdmin. If you need further assistance, please contact your OXID Hosting Partner or Internet Service Provider (ISP).

Now, you will need to create a new MySQL database. You can select any name for the database, for example, *oxid_eshop*. Make sure to remember the name of the database and the assigned login data for the database (username and password). You will need this data when running the setup.


.. Intern: oxbaad, Status: transL
