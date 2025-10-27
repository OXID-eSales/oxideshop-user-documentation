Update von 7.x auf 7.4
======================

Dieses Dokument beschreibt den Update-Vorgang von einer vorherigen Minor-Version der OXID eShop 7 Reihe, 7.x, auf das Minor Release 7.4. Dieses Update kann zusätzliche Schritte beinhalten, da die Möglichkeit besteht, eine von zwei Versionen des vorinstallierten **Content & Medien Bundles** zu wählen.

Vorbereitung
------------

#. Überprüfen Sie, dass Sie sich mindestens auf einer 7.x Version älter als 7.4 befinden.
#. Überprüfen Sie, welche OXID eShop Edition Sie verwenden (Enterprise, Professional oder Community).
#. Erstellen Sie ein Backup Ihrer Datenbank.
#. Erstellen Sie ein Backup Ihres Dateisystems.
#. Entscheiden Sie, welches **Content & Medien Bundle** Sie nach dem Update verwenden möchten.

    OXID eShop 7.4 hat das neue **Content & Medien Bundle 9** vorinstalliert. Dieses beinhaltet die folgenden Erweiterungen:

        * Media Library 4
        * WYSIWYG Editor 6
        * Visual CMS 9 (ausschließlich Enterprise und Professional Edition)

    Die Verwendung des neuen Bundles erfordert eine Migration bestehender Inhalte. Wenn Sie die aktualisierten Erweiterungen nicht verwenden möchten, können Sie Ihr Update vorkonfigurieren, um bei der letzten Major Version des **Content & Medien Bundles** zu bleiben. Dieses beinhaltet die folgenden Erweiterungen:

        * Media Library 3.0.0
        * WYSIWYG Editor 5.0.1
        * Visual CMS 8.0.2 (ausschließlich Enterprise und Professional Edition)

    Um zu entscheiden, welche Bundle-Version Sie verwenden möchten, lesen Sie bitte unsere :doc:`Release Notes <../releases/oxid-eshop-740>`.

Vorgehen
--------

Abhängig von Ihrer Edition und Ihrer Entscheidung bezüglich des **Content & Medien Bundles** besteht der Update-Vorgang aus bis zu vier Schritten:

* :ref:`Schritt 1: Das Content & Medien Bundle vorkonfigurieren <step-1-preconfigure-the-content-and-media-bundle>`
* :ref:`Schritt 2: Die Zielversion festlegen <step-2-set-the-target-version>`
* :ref:`Schritt 3: Den Update-Vorgang ausführen <step-3-run-the-update-process>`
* :ref:`Schritt 4: Die Rewrite-Bedingungen anpassen <step-4-adjust-the-rewrite-conditions>`
* :ref:`Schritt 5: Die Inhalte und Medien migrieren <step-5-migrate-content-and-media>`

.. _step-1-preconfigure-the-content-and-media-bundle:

Schritt 1: Das Content & Medien Bundle vorkonfigurieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Wenn Sie sich für das neue **Content & Medien Bundle 9** entscheiden, können Sie diesen Schritt überspringen und mit :ref:`Schritt 2: Die Zielversion festlegen <step-2-set-the-target-version>` fortfahren.

Wenn Sie sich entscheiden, das **Content & Medien Bundle 8** zu behalten und eine **OXID eShop Enterprise oder Professional Edition** verwenden, führen Sie die folgenden drei Befehle aus:

.. code:: shell

    composer require oxid-esales/media-library-module:^3.0 --no-update
    composer require ddoe/wysiwyg-editor-module:^5.0 --no-update
    composer require ddoe/visualcms-module:^8.0 --no-update

Wenn Sie sich entscheiden, das **Content & Medien Bundle 8** zu behalten und eine **OXID eShop Community Edition** verwenden, führen Sie die folgenden zwei Befehle aus:

.. code:: shell

    composer require oxid-esales/media-library-module:^3.0 --no-update
    composer require ddoe/wysiwyg-editor-module:^5.0 --no-update

.. _step-2-set-the-target-version:

Schritt 2: Die Zielversion festlegen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Wenn Sie die **OXID eShop Enterprise Edition** verwenden, führen Sie den folgenden Befehl aus:

.. code:: shell

    composer require oxid-esales/oxideshop-metapackage-ee:v7.4.0 --no-update

Wenn Sie die **OXID eShop Professional Edition** verwenden, führen Sie den folgenden Befehl aus:

.. code:: shell

    composer require oxid-esales/oxideshop-metapackage-pe:v7.4.0 --no-update

Wenn Sie die **OXID eShop Community Edition** verwenden, führen Sie den folgenden Befehl aus:

.. code:: shell

    composer require oxid-esales/oxideshop-metapackage-ce:v7.4.0 --no-update

.. _step-3-run-the-update-process:

Schritt 3: Den Update-Vorgang ausführen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Führen Sie in jedem Fall die folgenden Befehle aus, um Ihren OXID eSho* zu aktualisieren:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate

.. _step-4-adjust-the-rewrite-conditions:

Schritt 4: Die Rewrite-Bedingungen anpassen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Eine Rewrite-Bedingung in vorherigen OXID eShop Versionen schränkt die Verwendung bestimmter Markennamen ein. Das Update-Verhalten des OXID eShops ersetzt Ihre **.htaccess**-Datei nicht durch eine neue, da diese Datei in der Regel angepasst ist. Sie müssen die Datei daher manuell ändern.

#. Öffnen Sie die Datei **source/.htaccess**.
#. Suchen Sie nach der betroffenen Rewrite-Bedingung:

    .. code::

        RewriteCond %{REQUEST_URI} !(\/admin\/|\/Core\/|\/Application\/|\/export\/|\/modules\/|\/out\/|\/Setup\/|\/tmp\/|\/views\/)

#. Ersetzen Sie die erste betroffene Bedingung durch die folgende Bedingung:

    .. code::

        RewriteCond %{REQUEST_URI} !^(\/admin\/|\/Core\/|\/Application\/|\/export\/|\/modules\/|\/out\/|\/Setup\/|\/tmp\/|\/views\/)

#. Wiederholen Sie dies für die zweite betroffene Bedingung.
#. Speichern Sie die Datei.

.. _step-5-migrate-content-and-media:

Schritt 5: Die Inhalte und Medien migrieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Wenn Sie sich entschieden haben, das **Content & Medien Bundle 8** zu behalten, können Sie diesen Schritt überspringen. Ihr Update ist abgeschlossen.

Wenn Sie sich für das neue **Content & Medien Bundle 9** entschieden haben und eine **OXID eShop Enterprise oder Professional Edition** verwenden, lesen Sie bitte den Abschnitt `Update <https://github.com/OXID-eSales/vcms-documentation/blob/9.0-de/update.rst#update>`__ in unserer **Content & Medien Bundle**-Dokumentation, um Ihr Update abzuschließen.

Wenn Sie sich für das neue **Content & Medien Bundle 9** entschieden haben und eine **OXID eShop Community Edition** verwenden, lesen Sie bitte den Abschnitt `Einführung von Medien-IDs <https://github.com/OXID-eSales/vcms-documentation/blob/9.0-de/update.rst#einf%C3%BChrung-von-medien-ids>`__ in unserer **Content & Medien Bundle**-Dokumentation, um Ihr Update abzuschließen.
