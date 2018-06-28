Von 6.0.0_* auf 6.0.0 aktualisieren
===================================

Dieses Dokument beschreibt das Update von 6.0.0 Beta 1-3 oder RC 1-3 auf das finale Release 6.0.0.

Führen Sie das Update immer erst in einer Testumgebung, einer Kopie Ihres aktuellen Shops, aus. Erstellen Sie zuvor eine Sicherung der Shopdateien und der Datenbank. Deaktivieren Sie alle Module und prüfen Sie, ob der Shop prinzipiell funktioniert. Testen Sie nach dem Update den Shop erneut und legen Sie dabei besonderen Wert auf die Funktionen des Bestellprozesses, auf Zahlungs- und Versandarten.

Bevor mit dem Update des OXID eShop als Compilation begonnen werden kann, sind einige vorbereitende Schritte für Visual CMS und den WYSIWYG-Editor + Mediathek erforderlich.

Visual CMS
----------
Das in der Professional und Enterprise Edition enthaltene Modul wird durch das Update der Compilation von Version 2.0.0 auf 3.0.0 aktualisert. Es muss dafür deaktiviert und gelöscht werden.

* Gehen Sie im Administrationsbereich des Shops zu :menuselection:`Erweiterungen --> Module`.
* Wählen Sie das Modul Visual CMS aus und deaktivieren Sie es.
* Löschen Sie das Modulverzeichnis :file:`/source/modules/ddoe/visualcms`.
* Gehen Sie im Administrationsbereich zurück zur Modulverwaltung. Sie erhalten einen Hinweis, dass für ein registriertes Modul das Modulverzeichnis fehlt. Beantworten Sie die Frage, ob alle Modulinformationen entfernt werden sollen, indem Sie die Schaltfläche :guilabel:`Ja` drücken.

Wenn Sie eigene Shortcode-Klassen erstellt haben, welche die Klasse ``ddvisualeditor_shortcode`` erweitern, ändern Sie bitte ``ddvisualeditor_shortcode`` in ``\OxidEsales\VisualCmsModule\Application\Model\VisualEditorShortcode``. Fügen Sie Ihre eigenen Shortcode-Klassen keinen Namespaces hinzu.

.. code ::

    class your_shortcode extends \OxidEsales\VisualCmsModule\Application\Model\VisualEditorShortcode
    {
    }

WYSIWYG Editor + Mediathek
--------------------------
Das Modul wird durch das Update der Compilation von Version 1.0.0 auf 2.0.0 aktualisert. Es muss zuvor deaktiviert und gelöscht werden.

* Gehen Sie im Administrationsbereich des Shops zu :menuselection:`Erweiterungen --> Module`.
* Wählen Sie das Modul WYSIWYG Editor + Mediathek aus und deaktivieren Sie es.
* Löschen Sie das Modulverzeichnis :file:`/source/modules/ddoe/wysiwyg`.
* Gehen Sie im Administrationsbereich zurück zur Modulverwaltung. Sie erhalten einen Hinweis, dass für ein registriertes Modul das Modulverzeichnis fehlt. Beantworten Sie die Frage, ob alle Modulinformationen entfernt werden sollen, indem Sie die Schaltfläche :guilabel:`Ja` drücken.

-----------------------------------------------------------------------------------------

Update OXID eShop auf 6.0.0
---------------------------

.. |schritt| image:: ../../media/icons-de/schritt.jpg

|schritt| Update-Ziel vorgeben
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In die Datei :file:`composer.json`, die sich im Hauptverzeichnis des Shops befindet, muss die Version eingetragen werden, auf welche aktualisiert werden soll. Öffnen Sie die Datei in einem Editor und tragen Sie die Version 6.0.0 für das Metapackage ein. Beispiel: ``"oxid-esales/oxideshop-metapackage-ce": "^v6.0.0",``

|schritt| Abhängigkeiten aktualisieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Öffnen Sie eine Shell im Hauptverzeichnis des Shops und führen Sie den nachstehenden Composer-Befehl aus. Dadurch werden alle benötigten Bibliotheken aktualisiert. Der Parameter :command:`--no-dev` wird angegeben, wenn die entwicklungsbezogenen Dateien nicht benötigt werden.

.. code:: bash

   composer update --no-plugins --no-scripts --no-dev

|schritt| Neue Compilation beziehen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Mit einem zweiten Composer-Befehl werden alle Scripts ausgeführt, um die neue Compilation zu beziehen. Für Shopdateien, Themes und Module muss jeweils bestätigt werden, dass das Update bestehende Dateien überschreibt.

.. code:: bash

   composer update --no-dev

|schritt| Datenbank migrieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Der dritte und letzte Composer-Befehl führt die Migration der Datenbank aus.

.. code:: bash

   vendor/bin/oe-eshop-db_migrate migrations:migrate

|schritt| Module aktivieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^
* Gehen Sie im Administrationsbereich des Shops zu :menuselection:`Erweiterungen --> Module`.
* Wählen Sie das Modul Visual CMS aus und aktivieren Sie es.
* Aktivieren Sie auch WYSIWYG Editor + Mediathek.

Damit ist das Update beendet.

.. Intern: oxbanq, Status: