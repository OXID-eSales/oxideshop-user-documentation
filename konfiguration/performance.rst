:orphan:
Shop-Performance und Marketing-Funktionen
=========================================

Legen Sie Konfigurationsoptionen im OXID eShop fest, die für den Betrieb und die Anpassung Ihres Online-Shops relevant sind.

Konfigurieren Sie Bestellungen, Variantenmanagement, Bildverwaltung und Einstellungen im Administrationsbereich.

.. todo: #tbd: adjust redirect anlegen: OXID-eSales/documentation-redirect-handler at b-7.x


|procedure|

1. Wählen Sie :mensuselection:`Stanndaen --> Grundeinstellungen`.
#. Wählen Sie die Registerkarte :guilael:`Perform.`.


Template- und Artikellisten-Einstellungen
-----------------------------------------

* Überprüfen, ob Templates neu kompiliert werden müssen.

  Wenn diese Einstellung aktiv ist, überprüft der eShop bei jedem Aufruf, ob sich Templates geändert haben und berechnet die Ausgabe neu, falls Änderungen vorhanden sind. Aktivieren Sie die Einstellung, wenn Sie Templates anpassen, und deaktivieren Sie sie, wenn der eShop produktiv verwendet wird.

  .. note::
     Schalten Sie diese Einstellung aus, wenn der eShop in den Live-Betrieb geht.

* Varianten in Artikellisten laden (z. B. Suchergebnisse, Kategorieansichten).

  .. warning::
     Diese Einstellung verbraucht viel Speicher und kann zu Problemen auf schwachen Servern führen.

* Beim Laden von Artikeln "Aktiv von/bis" berücksichtigen.

Marketing- und Startseitenfunktionen
------------------------------------

* Liste der meistverkauften Artikel (Top of the Shop)

  - Einstellung: *manuell* oder *automatisch* wählbar.
  - Unter *Stammdaten → Grundeinstellungen → Performance* konfigurierbar.
  - Die Anzahl der angezeigten Bestseller kann im Template angepasst werden.
  - Siehe auch: :ref:`Aktionen und Startseite <aktionen-und-startseite>` [4][5]

* Liste der neusten Artikel (Frisch eingetroffen!)

  - Einstellung: *manuell* oder *automatisch* wählbar.
  - Unter *Stammdaten → Grundeinstellungen → Performance* konfigurierbar.
  - Die Anzahl und Sortierung kann angepasst werden.
  - Siehe auch: :ref:`Neueste Artikel <neueste-artikel>` [4][6]

* Leere Kategorien (keine Unterkategorien, keine Artikel) nicht anzeigen.

  - Einstellung im Admin-Backend aktivierbar.
  - Standardmäßig sollten leere Kategorien im OXID Shop ausgeblendet werden [7].

Cache- und Systemfunktionen
---------------------------

* Cache nur beim Ausloggen aus dem Administrationsbereich leeren.
* SEO Cache aktivieren.
* Meldungen der Systemgesundheitsprüfung auf der Startseite aktivieren.

.. _aktionen-und-startseite:

Aktionen und Startseite
-----------------------

Damit Aktionen wie „Top of the Shop“ und „Frisch eingetroffen!“ auf der Startseite angezeigt werden, muss das entsprechende Kontrollkästchen auf der Registerkarte *Perform.* unter *Stammdaten → Grundeinstellungen* aktiviert sein. Die Anzeige und Steuerung dieser Listen kann manuell oder automatisch erfolgen. Weitere Details siehe OXID Anwenderdokumentation [4].

.. _neueste-artikel:

Neueste Artikel
---------------

Neue Artikel können auf der Startseite entweder automatisch durch OXID ermittelt oder manuell zugeordnet werden. Die Auswahl und Reihenfolge ist im Backend flexibel steuerbar. Weitere Hinweise zur Einstellung und Sortierung siehe [6].




