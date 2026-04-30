Update von 7.x auf 7.5
======================

Dieses Dokument beschreibt den Update-Vorgang von einer vorherigen Minor-Version der OXID eShop 7 Reihe, 7.x, auf das Minor Release 7.5. Dieses Update kann zusätzliche Schritte beinhalten, da die Möglichkeit besteht, eine von drei Versionen des vorinstallierten **Content & Medien Bundles** zu wählen.

Vorbereitung
------------

#. Überprüfen Sie, dass Sie sich mindestens auf einer 7.x Version älter als 7.5 befinden.
#. Überprüfen Sie, welche OXID eShop Edition Sie verwenden (Enterprise, Professional oder Community).
#. Erstellen Sie ein Backup Ihrer Datenbank.
#. Erstellen Sie ein Backup Ihres Dateisystems.
#. Entscheiden Sie, welches **Content & Medien Bundle** Sie nach dem Update verwenden möchten.

    OXID eShop 7.5 hat das neue **Content & Medien Bundle 10** vorinstalliert. Dieses beinhaltet die folgenden Erweiterungen:

        * Media Library 5
        * WYSIWYG Editor 7
        * Visual CMS 10 (ausschließlich Enterprise und Professional Edition)

    Alternativ können Sie beim **Content & Medien Bundle 9** bleiben:

        * Media Library 4.1.0
        * WYSIWYG Editor 6.0.2
        * Visual CMS 9.2.0 (ausschließlich Enterprise und Professional Edition)

    Oder beim **Content & Medien Bundle 8** bleiben:

        * Media Library 3.0.0
        * WYSIWYG Editor 5.0.1
        * Visual CMS 8.0.2 (ausschließlich Enterprise und Professional Edition)

    Um zu entscheiden, welche Bundle-Version Sie verwenden möchten, lesen Sie bitte unsere :doc:`Release Notes <../releases/oxid-eshop-750>`.

Vorgehen
--------

Abhängig von Ihrer Edition und Ihrer Entscheidung bezüglich des **Content & Medien Bundles** besteht der Update-Vorgang aus bis zu fünf Schritten:

* :ref:`Schritt 1: Das Content & Medien Bundle vorkonfigurieren <step-1-preconfigure-the-content-and-media-bundle>`
* :ref:`Schritt 2: Die Zielversion festlegen <step-2-set-the-target-version>`
* :ref:`Schritt 3: Den Update-Vorgang ausführen <step-3-run-the-update-process>`
* :ref:`Schritt 4: Die Rewrite-Bedingungen anpassen <step-4-adjust-the-rewrite-conditions>`
* :ref:`Schritt 5: Die Inhalte und Medien migrieren <step-5-migrate-content-and-media>`

.. _step-1-preconfigure-the-content-and-media-bundle:

Schritt 1: Das Content & Medien Bundle vorkonfigurieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Wenn Sie sich für das neue **Content & Medien Bundle 10** entscheiden, können Sie diesen Schritt überspringen und mit :ref:`Schritt 2: Die Zielversion festlegen <step-2-set-the-target-version>` fortfahren.

**Beim Content & Medien Bundle 9 bleiben**

Wenn Sie eine **OXID eShop Enterprise oder Professional Edition** verwenden, führen Sie die folgenden drei Befehle aus:

.. code:: shell

    composer require oxid-esales/media-library-module:^4.0 --no-update
    composer require ddoe/wysiwyg-editor-module:^6.0 --no-update
    composer require ddoe/visualcms-module:^9.0 --no-update

Wenn Sie eine **OXID eShop Community Edition** verwenden, führen Sie die folgenden zwei Befehle aus:

.. code:: shell

    composer require oxid-esales/media-library-module:^4.0 --no-update
    composer require ddoe/wysiwyg-editor-module:^6.0 --no-update

**Beim Content & Medien Bundle 8 bleiben**

Wenn Sie eine **OXID eShop Enterprise oder Professional Edition** verwenden, führen Sie die folgenden drei Befehle aus:

.. code:: shell

    composer require oxid-esales/media-library-module:^3.0 --no-update
    composer require ddoe/wysiwyg-editor-module:^5.0 --no-update
    composer require ddoe/visualcms-module:^8.0 --no-update

Wenn Sie eine **OXID eShop Community Edition** verwenden, führen Sie die folgenden zwei Befehle aus:

.. code:: shell

    composer require oxid-esales/media-library-module:^3.0 --no-update
    composer require ddoe/wysiwyg-editor-module:^5.0 --no-update

.. _step-2-set-the-target-version:

Schritt 2: Die Zielversion festlegen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Wenn Sie die **OXID eShop Enterprise Edition** verwenden, führen Sie den folgenden Befehl aus:

.. code:: shell

    composer require oxid-esales/oxideshop-metapackage-ee:^7.5 --no-update

Wenn Sie die **OXID eShop Professional Edition** verwenden, führen Sie den folgenden Befehl aus:

.. code:: shell

    composer require oxid-esales/oxideshop-metapackage-pe:^7.5 --no-update

Wenn Sie die **OXID eShop Community Edition** verwenden, führen Sie den folgenden Befehl aus:

.. code:: shell

    composer require oxid-esales/oxideshop-metapackage-ce:^7.5 --no-update

.. hint::
   Der Constraint ``^7.5`` installiert automatisch die
   neueste verfügbare Patch-Version. Wenn Sie eine bestimmte
   Patch-Version benötigen, geben Sie diese explizit an,
   z. B. ``v7.5.0``. Wir empfehlen, die jeweils neueste
   Patch-Version zu verwenden.

.. _step-3-run-the-update-process:

Schritt 3: Den Update-Vorgang ausführen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Führen Sie in jedem Fall die folgenden Befehle aus, um Ihren OXID eShop zu aktualisieren:

.. code:: shell

    composer update --no-plugins --no-scripts --no-dev --with-all-dependencies
    composer update --no-dev
    ./vendor/bin/oe-console oe:cache:clear
    ./vendor/bin/oe-eshop-db_migrate migrations:migrate
    ./vendor/bin/oe-eshop-db_views_generate

.. _step-4-adjust-the-rewrite-conditions:

Schritt 4: Die .htaccess-Datei anpassen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Da die **.htaccess-Datei** typischerweise dem Projekt und seiner Umgebung angepasst wird, ersetzt der OXID eShop sie beim Update nicht. Sie müssen die Datei daher manuell ändern. Mit OXID eShop 7.5 sind zwei Änderungen relevant:

**4a) Rewrite-Bedingung mit Anker**

Eine Rewrite-Bedingung in älteren OXID eShop Versionen schränkt die Verwendung bestimmter Markennamen ein. Die korrigierte Bedingung ist in der ausgelieferten **.htaccess**-Vorlage seit 7.4 enthalten — da Ihre projektspezifisch angepasste **.htaccess**-Datei beim Update nicht ersetzt wird, ist die Korrektur in vielen Bestands-Shops dennoch nicht eingespielt. Prüfen Sie daher, ob die Änderung vorhanden ist, und nehmen Sie sie gegebenenfalls vor.

#. Öffnen Sie die Datei **source/.htaccess**.
#. Suchen Sie nach der zu ändernden Rewrite-Bedingung:

    .. code::

        RewriteCond %{REQUEST_URI} !(\/admin\/|\/Core\/|\/Application\/|\/export\/|\/modules\/|\/out\/|\/Setup\/|\/tmp\/|\/views\/)

#. Ersetzen Sie das erste Vorkommnis durch die folgende Bedingung:

    .. code::

        RewriteCond %{REQUEST_URI} !^(\/admin\/|\/Core\/|\/Application\/|\/export\/|\/modules\/|\/out\/|\/Setup\/|\/tmp\/|\/views\/)

#. Wiederholen Sie dies für die zweite gefundene Stelle.
#. Speichern Sie die Datei.

**4b) Neue Regeln für den API-Entrypoint (neu in 7.5)**

OXID eShop 7.5 fügt einen neuen REST-API-Entrypoint hinzu (``api.php``). Damit Anfragen an ``https://<ihr-shop>/api/...`` korrekt an diesen Entrypoint geroutet werden und der ``Authorization``-Header (für JWT-basierte Authentifizierung) PHP erreicht, sind zwei zusätzliche Bereiche in der **.htaccess-Datei** erforderlich. Ohne diese Regeln funktionieren der API-Entrypoint und die darauf aufbauenden Funktionen (JWT-Authentifizierung, Rate-Limiting) nicht.

#. Öffnen Sie die Datei **source/.htaccess**.
#. Prüfen Sie, ob die folgenden Zeilen innerhalb des ``<IfModule mod_rewrite.c>``-Blocks bereits enthalten sind:

    .. code::

        RewriteCond %{HTTP:Authorization} .
        RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]

        RewriteRule ^api/(.*)$ api.php/$1 [QSA,NC,L]

#. Falls die Zeilen fehlen, fügen Sie sie wie folgt ein. Die ``Authorization``-Passthrough-Regel gehört direkt nach ``RewriteBase /``, die API-Rewrite-Regel direkt nach der bestehenden ``graphql``-Regel:

    .. code::

        <IfModule mod_rewrite.c>
            Options +FollowSymLinks
            RewriteEngine On
            RewriteBase /

            RewriteCond %{HTTP:Authorization} .
            RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]

            RewriteRule ^graphql/?$    widget.php?cl=graphql&skipSession=1   [QSA,NC,L]

            RewriteRule ^api/(.*)$ api.php/$1 [QSA,NC,L]

            ...

#. Speichern Sie die Datei.

.. note::
   Die ``RewriteCond``- und ``RewriteRule``-Zeilen für die ``Authorization``-Weitergabe sind notwendig, weil viele Apache- und FastCGI-Konfigurationen den ``Authorization``-Header per Default nicht an PHP weiterreichen. Die zwei Zeilen kopieren den Header in eine Umgebungsvariable, die PHP auswerten kann. Ohne sie schlägt jede JWT-Authentifizierung mit ``401 Unauthorized`` fehl.

.. _step-5-migrate-content-and-media:

Schritt 5: Die Inhalte und Medien migrieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Wenn Sie sich entschieden haben, das **Content & Medien Bundle 8** oder **9** zu behalten, können Sie diesen Schritt überspringen. Ihr Update ist abgeschlossen.

Wenn Sie sich für das neue **Content & Medien Bundle 10** entschieden haben und eine **OXID eShop Enterprise oder Professional Edition** verwenden, lesen Sie bitte den Abschnitt `Update <https://docs.oxid-esales.com/modules/vcms/de/10.0/update.html>`__ in unserer **Content & Medien Bundle**-Dokumentation, um Ihr Update abzuschließen.

Wenn Sie sich für das neue **Content & Medien Bundle 10** entschieden haben und eine **OXID eShop Community Edition** verwenden, lesen Sie bitte den Abschnitt `Einführung von Medien-IDs <https://docs.oxid-esales.com/modules/vcms/de/10.0/update.html#einfuhrung-von-medien-ids>`__ in unserer **Content & Medien Bundle**-Dokumentation, um Ihr Update abzuschließen.

.. todo:: Links zur VCMS 10.0 Dokumentation verifizieren,
   sobald diese veröffentlicht ist
