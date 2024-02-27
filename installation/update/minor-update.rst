:orphan:
Minor Update installieren
=========================

.. todo: #tbd 7.x: evtl. reuse: Topic vorl. ausgeblendet

Aktualisieren Sie die Compilation beispielsweise von einer bestehenden Version 6.3.x auf Version 6.5.0.

.. include:: /_static/reuse/note_dataloss.rst

Kompatibilität von Drittanbieter-Modulen sicherstellen
------------------------------------------------------

Wenn Sie Module oder Themes von Drittanbietern verwenden, fragen Sie den Drittanbieter, ob diese Themes und Module mit der neuen Version des OXID eShops kompatibel sind.

Hintergrund: Normalerweise enthält ein Minor Update keine breaking changes. Alle Module von Drittanbietern funktionieren nach dem Update wie zuvor.

In Ausnahmefällen können sich Änderungen jedoch so auswirken, dass Module von Drittanbietern nicht mehr funktionieren.
|br|
Beispiele:

* Drittanbieter-Module funktionieren beim Update von OXID eShop 6.1 auf 6.2 nicht mehr.
* Das OXID eSales-Modul Amazon Pay 3.6.8 funktioniert in OXID eShop 6.5 nicht mehr (siehe :ref:`releases/releases-65/oxid-eshop-650:OXID eShop 6.5.0`).


Voraussetzungen sicherstellen
-----------------------------

Bevor Sie ein Minor Update auf die gewünschte Zielversion von OXID eShop ausführen können, stellen Sie sicher, dass Sie die technischen Voraussetzungen für das Update erfüllen.

Dazu prüfen Sie:

* Muss ich ein oder mehrere inkrementelle Updates machen?
  |br|
  Inkrementelles Update bedeutet: Sie machen ein Update nicht direkt auf die Zielversion, sondern in einem vorhergehenden Schritt ein Update auf eine Version zwischen Ihrer Ausgangs-Version und Ihrer Ziel-Version.
  |br|
  Erst in einem folgenden Update machen Sie das Update von der Zwischenversion zur Zielversion.
* Habe ich beim Update oder beim inkrementellen Update eine Version von :emphasis:`Composer`, die sowohl meine jeweilige Ausgangs- als auch die Zielversion unterstützt?
* Habe ich beim Update oder beim inkrementellen Update eine Version von :emphasis:`PHP`, die sowohl meine jeweilige Ausgangs- als auch die Zielversion unterstützt?

|procedure|

Prüfen Sie Schritt für Schritt, welches inkrementelle Update Sie machen müssen, um schließlich zur Zielversion von OXID eShop zu kommen.

Stellen Sie dabei vor jedem Update-Schritt sicher, dass Sie Versionen von Composer und PHP haben, die sowohl von der jeweiligen Ausgangs- als auch von der jeweiligen Zielversion unterstützt werden.


1. Wenn Sie OXID eShop Version 5.x oder kleiner haben, folgen Sie den Anweisungen unter `docs.oxid-esales.com/developer/en/6.0/update/eshop_from_53_to_6/index.html <https://docs.oxid-esales.com/developer/en/6.0/update/eshop_from_53_to_6/index.html>`_.
   |br|
   Alternativ: Installieren Sie die aktuelle Version von OXID eShop und portieren Sie nur die wichtigen Daten.

   .. note::

      **Module portieren**

      Ihre Module funktionieren nicht mehr unter OXID eShop Version 6.

      Wie Sie Ihre Module in OXID eShop Version 6 portieren können, erfahren Sie unter https://docs.oxid-esales.com/developer/en/6.0/modules/tutorials/porting_tool.html.

   .. note::

      **Azure-Theme obsolet**

      Das Azure-Theme wird in OXID eShop Version 6 noch unterstützt, aber nicht mehr gepflegt.

#. Wenn Sie OXID eShop Version :emphasis:`6.0.x` haben, tun Sie Folgendes:

   a. Stellen Sie sicher, dass Sie Composer Version 1 haben.
   #. Stellen Sie sicher, dass Sie PHP Version 7.0 haben.
   #. Machen Sie ein erstes Update von Version 6.0.x auf Version 6.1.x.
      |br|
      Weitere Informationen finden Sie unter https://docs.oxid-esales.com/eshop/de/6.1/installation/update-installation/update-installation.html

#. Wenn Sie OXID eShop Version :emphasis:`6.1.x` haben, tun Sie Folgendes:

   a. Stellen Sie sicher, dass Sie Composer Version 1 haben.
   #. Stellen Sie sicher, dass Sie PHP Version 7.1 haben.
   #. Machen Sie ein Update von Version 6.1.x auf Version 6.2.4.
      |br|
      Weitere Informationen finden Sie unter https://docs.oxid-esales.com/eshop/de/6.2/installation/update/von-6.1.x-auf-6.2.0-aktualisieren.html

#. Wenn Sie OXID eShop Version :emphasis:`6.2.0`, :emphasis:`6.2.1` oder :emphasis:`6.2.2` haben, tun Sie Folgendes:

   a. Machen Sie ein Patch-Update auf OXID eShop Version :emphasis:`6.2.4`.
   #. Optional: Machen Sie ein Update auf von PHP Version 7.1 auf Version 7.4.
      |br|
      Alternativ: Machen Sie das Update auf PHP Version 7.4 bei den folgenden OXID eShop-Updates.
   #. Machen Sie ein Update von Composer Version 1 auf Composer Version 2.

#. Wenn Sie OXID eShop Version :emphasis:`6.2.3` oder :emphasis:`6.2.4` haben, tun Sie Folgendes:

   a. Stellen Sie sicher, dass Sie Composer Version 2.2.23 haben.

      .. attention::

         Composer Version 2.3.x wird nicht unterstützt.

         Wenn Sie Composer Version 2.3.x haben, installieren Sie beispielsweise Composer Version 2.2.23 wie folgt:

         .. code:: bash

            composer selfupdate 2.2.23

   #. Stellen Sie sicher, dass Sie PHP Version 7.4 haben.
   #. Machen Sie ohne weitere Zwischenschritte das Update auf die gewünschte Zielversion.

#. Wenn Sie OXID eShop Version 6.2.5 oder höher haben, machen Sie das Update auf die aktuelle Version direkt, wie im Folgenden beschrieben unter :ref:`installation/update/minor-update:Update ausführen`.


Update ausführen
----------------

Aktualisieren Sie Ihren OXID eShop auf die aktuelle Version.

|prerequisites|

Sie haben die nötigen inkrementellen Updates ausgeführt (siehe :ref:`installation/update/minor-update:Voraussetzungen sicherstellen`).

|procedure|

1. Aktualisieren Sie Composer auf Version 2.7.

   Installieren Sie Composer 2.7 beispielsweise wie folgt:

   .. code:: bash

      sudo composer selfupdate 2.7.1

#. Aktualisieren Sie in der Datei :file:`composer.json` die Version des Metapackage.
   |br|
   Passen Sie dazu wie im folgenden Beispiel den Namen des Metapackage der gewünschten Shop-Edition an.
   |br|
   Beispiel für ein Update einer Community Edition mit dem Metapackage-Namen ``6.4.2``:

   .. code:: bash

      composer require --no-update oxid-esales/oxideshop-metapackage-ce:v6.4.2

#. Aktualisieren Sie die Abhängigkeiten.
   |br|
   Öffnen Sie eine Shell im Hauptverzeichnis des Shops und führen Sie den nachstehenden Composer-Befehl aus.
   |br|
   Dadurch werden alle benötigten Bibliotheken aktualisiert.
   |br|
   Den Parameter :command:`--no-dev` geben Sie an, wenn Sie die entwicklungsbezogenen Dateien nicht brauchen.

   .. code:: bash

      composer update --no-plugins --no-scripts --no-dev

#. Um die neue Compilation zu beziehen und das Update auszuführen, führen Sie die Skripte aus.
   |br|
   Führen Sie dazu den folgenden Befehl aus.
   |br|


   .. note::

      Durch das Update werden mögliche Änderungen überschrieben, die Sie im Verzeichnis :file:`source` an Modulen oder Themes vorgenommen haben.

      Hintergrund: Bei einem Shop-Update lädt Composer die neuen Daten zunächst ins Verzeichnis :file:`vendor`. Anschließend werden die Daten ins Verzeichnis :file:`source` kopiert. Damit werden die Dateien des Shops, der Module und der Themes ersetzt.

      Ihre individuellen Anpassungen des OXID Shops oder Änderungen an Modulen von Fremdherstellern sind nur dann vorm Überschreiben durch das Update sicher, wenn Sie die Änderungen durch eine der Erweiterungsmöglichkeiten des OXID eShops (Component, Modul, Child-Theme) vorgenommen haben.

      Weitere Informationen finden Sie in der Entwickler-Dokumentation unter

      * `Module skeleton: metadata, composer, and structure <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/skeleton/index.html>`_
      * `How to create a theme installable via composer? <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/theme/theme_via_composer.html>`_


   .. attention::

      **Abfragen bestätigen**

      Während des Updates werden Sie gefragt, welche Pakete überschrieben werden dürfen.

      Damit nur kompatible und getestete Pakete installiert werden und es nicht zu Inkonsistenzen und Fehlfunktionen durch fehlerhaft implementierte Module oder Themes kommen kann, müssen Sie die Abfragen mit :technicalname:`Ja` bestätigen.


      Empfehlungen:

      * Wenn Sie die Erweiterungsmöglichkeiten des OXID eShops nutzen, folgen Sie den Anweisungen in der `Entwickler-Dokumentation <https://docs.oxid-esales.com/developer/en/latest/>`_.
      * Holen Sie zum Erstellen von Modulen oder Child-Themes die Unterstützung einer OXID-Partner-Agentur ein. Dies erleichtert Ihnen alle künftigen Updates.
        |br|
        Eine Liste der von OXID zertifizierten Partneragenturen finden Sie unter `oxid-esales.com/partner/partner-finden/ <https://www.oxid-esales.com/partner/partner-finden/>`_.
      * Wenn Sie Module oder Themes von Drittanbietern verwenden, fragen Sie den Drittanbieter, ob diese Themes und Module mit der neuen Version des OXID eShops kompatibel sind.
        |br|
        Hintergrund: Normalerweise enthält ein Minor Update keine breaking changes. Alle Module von Drittanbietern funktionieren nach dem Update wie zuvor.
        |br|
        In Ausnahmefällen (beispielsweise beim Update von OXID eShop 6.1 auf 6.2) können sich Änderungen jedoch so auswirken, dass Module von Drittanbietern nicht mehr funktionieren.

   .. code:: bash

      composer update --no-dev

#. Um sicherzustellen, dass die zwischengespeicherten Elemente keine Inkompatibilitäten enthalten, leeren Sie das Verzeichnis :file:`tmp`.
   |br|
   Führen Sie dazu den folgenden Befehl aus.

   .. code:: bash

      rm -rf source/tmp/*

#. Migrieren Sie die Datenbank.
   |br|
   Führen Sie dazu den folgenden Befehl aus.

   .. code:: bash

      vendor/bin/oe-eshop-db_migrate migrations:migrate

#. Generieren Sie die Datenbank-Views neu.
   |br|
   Hintergrund: Je nach Änderungen und Shop-Edition kann es sein, dass der Shop nach dem Update in den Wartungsmodus geht.
   |br|
   Um dem vorzubeugen, generieren Sie die Datenbank-Views mit folgendem Befehl neu:

   .. code:: bash

      vendor/bin/oe-eshop-db_views_generate

.. Intern: oxbajz, Status:
