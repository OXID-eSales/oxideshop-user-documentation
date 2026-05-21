OXID eShop Core Edition
=======================

Ab OXID eShop 6.5 steht eine **Core Edition** als Alternative
zur Standard-Compilation zur Verfügung. Sie enthält den
Shop-Kern und alle seine Abhängigkeiten, jedoch ohne die
mitgelieferten Module und deren Abhängigkeiten. So behalten
Sie die volle Kontrolle darüber, welche Module Sie
installieren und aktualisieren.

Warum Core Edition?
-------------------

Die Standard-Compilation des OXID eShop wird als getesteter
Snapshot ausgeliefert: Der Shop-Kern und alle enthaltenen
Module sind auf exakte Versionen festgelegt, die gemeinsam
verifiziert wurden. Das gewährleistet Stabilität, bedeutet
aber auch, dass die Aktualisierung eines einzelnen Moduls
ein neues Compilation-Release erfordert.

OXID eShop 6.5 befindet sich im **Legacy-Support**. Der
Shop-Kern erhält weiterhin kritische Sicherheitsupdates
auf Best-Effort-Basis, die Compilation als Ganzes erhält
jedoch keine neuen Releases mehr. Dadurch kann es vorkommen,
dass einzelne Module aktualisiert werden müssen —
Sicherheitspatches, Kompatibilitätsfixes oder Ersetzungen —
die festgelegten Abhängigkeiten der Compilation dies aber
verhindern.

Die Core Edition löst dies, indem sie den Shop-Kern von
den Modulen trennt:

* **Shop-Kern**: Erhält weiterhin kritische
  Sicherheitsupdates auf Best-Effort-Basis.
* **Module**: Sie verwalten diese einzeln über Composer —
  installieren, aktualisieren, ersetzen oder entfernen
  nach Bedarf.

.. note::

   Wir empfehlen das Update auf die aktuelle OXID eShop
   Version (7.x) für vollen Support, aktive Wartung und
   Zugang zu den neuesten Funktionen und
   Sicherheitsverbesserungen.

   OXID eShop 7.x läuft auf aktuellen PHP-Versionen
   (8.3–8.5), MySQL 8.0/8.4 und MariaDB 11. Er enthält
   verbesserte Sicherheitsmaßnahmen und eine Architektur,
   in der Modul-Code nicht mehr direkt über das Web
   erreichbar ist.

   Die Core Edition für 6.5 richtet sich an Shops, die
   nicht sofort auf 7.x migrieren können, aber einzelne
   Module warten oder aktualisieren müssen.

   Informationen zum Update auf die aktuelle Version
   finden Sie in der `Update-Anleitung <https://docs.oxid-esales.com/developer/en/7.0/update/eshop_from_65_to_7/index.html>`_.

Was ist enthalten
-----------------

Die Core Edition enthält den Shop-Kern und die
Infrastruktur-Pakete — alles, was zum Betrieb des
OXID eShop ohne mitgelieferte Module benötigt wird:

* OXID eShop Kern (gleiche Version wie in der
  Standard-Compilation)
* Themes (Flow, Wave)
* Composer-Plugin, Datenbank-Views-Generator,
  Migration-Wrapper
* Alle erforderlichen Symfony- und PHP-Abhängigkeiten

Was ist nicht enthalten
-----------------------

Die folgenden Module und deren Abhängigkeiten aus der
Standard-CE-Compilation sind im Core-Edition-Metapackage
**nicht enthalten**:

* WYSIWYG Editor + Mediathek
  (``ddoe/wysiwyg-editor-module``)
* Klarna (``fatchip-gmbh/oxid-klarna-6``)
* Makaira (``makaira/oxid-connect-essential``)
* GDPR Opt-In (``oxid-esales/gdpr-optin-module``)
* PayPal (``oxid-esales/paypal-module``)
* Cookie Management powered by Usercentrics
  (``oxid-professional-services/usercentrics``)
* PAYONE (``payone-gmbh/oxid-6``)

.. warning::

   Wenn Sie das Metapackage wechseln und
   ``composer update`` ausführen, wird Composer alle
   Pakete **entfernen**, die — direkt oder transitiv —
   nicht mehr im neuen Abhängigkeitsbaum benötigt werden.
   Das betrifft auch **aktive, im Shop laufende Module**
   — nicht nur deaktivierte.

   Betroffen sind die Module und deren Abhängigkeiten,
   die über das Standard-Compilation-Metapackage
   mitgeliefert wurden. Module, die Sie oder Ihre Agentur
   separat installiert haben, sind bereits explizite
   Anforderungen in Ihrer ``composer.json`` und bleiben
   erhalten.

   Identifizieren Sie vor dem Wechsel, welche der
   mitgelieferten Module Ihr Shop tatsächlich nutzt.
   Die Migrationsanleitung in der Entwicklerdokumentation
   enthält detaillierte Anweisungen dazu.

.. note::

   PE- und EE-Compilations enthalten zusätzliche Module
   (z. B. Visual CMS für PE/EE, Unzer Payment für EE).
   Das gleiche Prinzip gilt — die Core Edition jeder
   Edition enthält nur den Shop-Kern und seine
   Abhängigkeiten. Alle Module müssen explizit
   angefordert werden.

Editionen
---------

Die Core Edition ist für alle drei OXID eShop Editionen
verfügbar:

* CE: ``oxid-esales/metapackage-ce-core``
* PE: ``oxid-esales/metapackage-pe-core``
* EE: ``oxid-esales/metapackage-ee-core``

Migration zur Core Edition
--------------------------

.. important::

   Dies ist eine kritische Änderung an der
   Abhängigkeitsstruktur Ihres Shops. **Führen Sie die
   Migration immer zuerst auf einer Entwicklungs- oder
   Staging-Umgebung durch.** Überprüfen Sie, dass der Shop
   korrekt funktioniert — einschließlich aller Module,
   Zahlungsmethoden und Checkout-Abläufe — bevor Sie die
   Änderung auf Ihr Produktivsystem übertragen.

Die Migration erfordert zwei Dinge in einem Schritt: das
Ersetzen des Metapackages **und** das explizite Anfordern
jedes Moduls, das aktuell in Ihrem Shop installiert ist —
auch Module, die Sie später entfernen möchten. Führen Sie
``composer update`` nicht aus, nachdem Sie nur das
Metapackage gewechselt haben — dies würde Ihre Module
entfernen. Nach Abschluss der Migration entfernen Sie nicht
benötigte Module sauber mit ``composer remove`` (siehe
„Module nach der Migration verwalten" unten).

Übersicht
^^^^^^^^^

1. **Sichern** Sie Ihren Shop — Datenbank, Dateien und
   ``composer.json``.
2. **Sichern** Sie Ihre ``composer.lock`` — sie ist die
   vollständige Aufzeichnung aller aktuell installierten
   Pakete und deren exakte Versionen.
3. **Bearbeiten** Sie ``composer.json``: Ersetzen Sie das
   Standard-Metapackage durch das Core-Edition-Metapackage
   und fügen Sie jedes Modul, das aktuell in Ihrem Shop
   installiert ist, als explizite Anforderung mit seiner
   aktuellen Version hinzu — auch Module, die Sie später
   entfernen möchten. Diese können Sie nach Abschluss der
   Migration sauber mit ``composer remove`` entfernen.
4. **Führen** Sie ``composer update`` auf Ihrer
   Entwicklungs- oder Staging-Umgebung aus.
5. **Überprüfen** Sie, dass alle erwarteten Pakete in den
   erwarteten Versionen vorhanden sind und der Shop
   korrekt funktioniert.
6. **Testen** Sie den Shop gründlich — Frontend, Checkout,
   Zahlung, Admin — bevor Sie das Produktivsystem
   aktualisieren.

Die detaillierte Schritt-für-Schritt-Anleitung mit exakten
Composer-Befehlen finden Sie in der `Entwicklerdokumentation <https://docs.oxid-esales.com/developer/en/6.5/update/migrate-to-core-edition.html>`_.

Module nach der Migration verwalten
------------------------------------

Nach dem Wechsel zur Core Edition sind die Module nicht
mehr durch das Compilation-Metapackage gesperrt. Sie können
sie einzeln verwalten:

**Modul aktualisieren:**

.. code:: bash

   composer update vendor/module-name

**Modul entfernen:**

.. code:: bash

   composer remove vendor/module-name

**Ersatzmodul installieren:**

.. code:: bash

   composer require vendor/new-module-name

.. important::

   Nach jeder Moduländerung den Shop-Cache leeren und
   Views neu generieren:

   .. code:: bash

      vendor/bin/oe-console oe:cache:clear
      vendor/bin/oe-console oe:module:activate module-id
      vendor/bin/oe-console oe:database:generateviews
