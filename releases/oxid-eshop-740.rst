OXID eShop Compilation 7.4.0
============================

Veröffentlichungsdatum: DD.11.2025

Neuheiten
---------

Wesentliche Änderungen im Content & Medien Bundle
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

OXID eShop 7.4 bringt ein umfangreiches Update unseres **Content & Medien Bundles** auf Version 9 mit sich. Dieses enthält folgende Erweiterungen:

* Mediathek 4
* WYSIWYG-Editor 6
* Visual CMS 9 (nur Enterprise und Professional Edition)

Das Update enthält zahlreiche Funktionserweiterungen, strukturelle Änderungen und notwendige Fehlerbehebungen:

* Neue Alt-Text-Funktion: `Dokumentation <https://docs.oxid-esales.com/modules/vcms/de/9.0/mediathek.html#alt-text>`__
* Neue Konfigurationsoption zum Festlegen einer Standard-Mediendatei: `Dokumentation <https://docs.oxid-esales.com/modules/vcms/de/9.0/mediathek.html#standard-media-id>`__
* Umstellung auf Medien-IDs statt URLs: `Dokumentation <https://docs.oxid-esales.com/modules/vcms/de/9.0/update.html#einfuhrung-von-medien-ids>`__
* Neue Aktivitätseinstellungen für zeitgesteuerte Widgets: `Dokumentation <https://docs.oxid-esales.com/modules/vcms/de/9.0/funktionsbeschreibung/aktivitatszeitraum-fur-widgets.html>`__
* Neues Zeilenelement für das Layouting: `Dokumentation <https://docs.oxid-esales.com/modules/vcms/de/9.0/funktionsbeschreibung/umgang-mit-widgets.html#widget-hinzufugen>`__
* Zusätzlicher Button zum Erstellen neuer Inhalte: `Dokumentation <https://docs.oxid-esales.com/modules/vcms/de/9.0/funktionsbeschreibung/grundfunktionen.html#neuen-cms-inhalt-anlegen>`__
* Umstellung von Parse- auf Tree-Struktur: `Dokumentation <https://docs.oxid-esales.com/modules/vcms/de/9.0/update.html#geanderte-codebasis>`__, `Entwicklerinformationen [en] <https://docs.oxid-esales.com/modules/vcms/en/9.0/developer.html#preparetemplateparams-method>`__
* Zeilen- und Spaltenelemente passen ihre Höhe automatisch an.
* Bootstrap 5 für den Visual CMS Arbeitsbereich im Administrationsbereich.
* Refactoring und Aufteilung einiger großer Dateien.

Das Update auf das **Content & Medien Bundle 9** erfordert die Migration bestehender Inhalte. Wenn Sie die Vorgängerversion, **Content & Medien Bundle 8**, beibehalten möchten, können Sie dies tun, indem Sie Ihr Update vorkonfigurieren. Die erforderlichen Schritte finden Sie in unserer `Update-Anleitung <https://docs.oxid-esales.com/modules/vcms/de/9.0/update.html>`_.

Weitere Informationen zum aktualisierten **Content & Medien Bundle 9** finden Sie in unserem News-Bereich oder in den entsprechenden Dokumentationen.


.. note::
    Das umfangreiche Update unseres **Content & Medien Bundles** ist ein großer Fortschritt und bietet eine stabilere und besser wartbare Basis für zukünftige Änderungen.

    Aufgrund weiterer Architekturoptimierungen in Visual CMS empfehlen wir, stark individualisierte Anpassungen auf **OXID eShop 7.5** zu verschieben, der **Visual CMS 10** enthalten wird.

    Wir freuen uns über jedes Feedback, um die Erweiterungen kontinuierlich zu verbessern.

Besseres Nutzererlebnis
^^^^^^^^^^^^^^^^^^^^^^^

Es wurden mehrere Verbesserungen vorgenommen, um das **Nutzererlebnis** im Shop zu verbessern. Einige Beispiele sind:

* Verbesserte Sichtbarkeit der Bestätigung zum Abesenden des Kontaktformulars.
* Kein Abbruch des Bestellvorgangs bei Verwendung des Zurück-Buttons des Browsers.
* Korrekte Rückmeldung bei falschem Passwort beim Ändern der E-Mail-Adresse.
* Aktualisierte Erklärungen und Übersetzungen.

Weitere Informationen finden Sie in den Abschnitten :ref:`Fixes <fixes>` und :ref:`Packages <packages>`.

Vite für APEX
^^^^^^^^^^^^^

Das Frontend-Build-Tool Grunt wurde bereits bei Visual CMS durch `Vite <https://vite.dev/>`_ ersetzt. Das Standard-Theme des OXID eShops, APEX, verwendet absofort ebenfalls Vite.

MySQL 8.4 Unterstützung
^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop 7.4 Compilation und alle unten aufgeführten Erweiterungen wurden erfolgreich mit **MySQL 8.4 (LTS)** getestet. Es ist somit bestätigt, dass sie diese Long-Term-Support-Version von MySQL unterstützen.

.. _fixes:

Fixes
-----

* #0007848 Visual CMS Demodaten enthalten keine Designinformationen: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7848>`_
* #0007847 Übersetzungen zum Überspringen von Rabatten sind falsch: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7847>`_
* #0007846 Visual CMS Setup schlägt bei npm install und build fehl: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7846>`_
* #0007845 Visual CMS Vorschaumodus verwendet immer die Standardsprache: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7845>`_
* #0007844 Die Gutscheinoption Nur einmal berechnen gilt ausschließlich für Produkte: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7844>`_
* #0007843 Großer Abstand unter dem Menü: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7843>`_
* #0007842 YUI Bibliothek wird nicht mehr unterstützt und ist veraltet: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7842>`_
* #0007841 TemplateChainResolver ist ineffizient: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7841>`_
* #0007840 Im GraphQL products Query fehlt ein Filter für die Pagination: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7840>`_
* #0007839 Das APEX Theme verwendet weiterhin Grunt, statt Vite: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7839>`_
* #0007838 Der OE Console Befehl zum Erstellen eines Benutzers prüft nicht, ob ein Benutzer bereits vorhanden ist: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7838>`_
* #0007721 Die Bestellbemerkung ist bei fehlender Eingabe immer 1: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7721>`_
* #0007708 Das Dropdown bei Produkten funktioniert im vierten Bestellschritt nicht: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7708>`_
* #0007689 Das Visual CMS Artikel Widget ignoriert den Status aktiv/inaktiv: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7689>`_
* #0007622 Ein Text-Overflow im Visual CMS stoppt den Shop: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7622>`_
* #0007293 Merk- und Wunschlisten gehen bei aktivierter Warenkorbreservierung verloren, wenn die Reservierung abläuft: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7293>`_
* #0007205 USt-IdNr.-Prüfung funktioniert nicht für hinzugefügte Länder: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7205>`_
* #0007104 WYSIWYG-Editor stiehlt bei Initialisierung den Fokus: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7104>`_
* #0007097 Duplizierter URL-Parameter editlanguage im AJAX-Aufruf: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7097>`_
* #0007004 Der Zurück-Button des Browsers stoppt den Bestellvorgang: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=7004>`_
* #0006917 Der Haftungsausschluss für Downloads wird nicht korrekt angezeigt: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=6917>`_
* #0006144 Fehlendes Div-Element im Setup: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=6144>`_
* #0006031 Es ist schlecht ersichtlich, dass das Kontaktformular gesendet wurde: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=6031>`_
* #0006026 Ein falsches Passwort beim Ändern der E-Mail-Adresse führt zur irreführenden Meldung, die E-Mail sei inkorrekt: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=6026>`_
* #0005798 Attributerstellung in neuem Fenster funktioniert nicht: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=5798>`_
* #0005244 Die Methode getAvailableInLangs kann Datenbankfelder in Kleinbuchstaben nicht verarbeiten: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=5244>`_
* #0005242 Die Rewrite-Regeln verhindern die Nutzung mancher Markennamen: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=5242>`_
* #0002777 Beim erneuten Abonnieren des Newsletters ist der Datenbankwert falsch: `Bugtracker <https://bugs.oxid-esales.com/view.php?id=2777>`_

.. _packages:

Packages
--------

OXID eShop CE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop CE Compilation beinhaltet die folgenden Pakete:

* APEX Theme von v2.1.0 auf v3.0.1: `Changelog <https://github.com/OXID-eSales/apex-theme/blob/v3.0.1/CHANGELOG-3.x.md>`_
* Eye-Able Assist v3.0.3: `Changelog <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/blob/v3.0.3/CHANGELOG.md>`_
* GDPR Opt-In Module von v4.2.0 auf v4.3.0: `Changelog <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.3.0/CHANGELOG.md>`_
* Makaira Connect Essential von 2.1.3 auf 2.1.4: `Changelog <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.4/CHANGELOG.md>`_
* Media Library Module von v3.0.0 auf v4.0.0 (oder auf v3.0.0 bleibend): `Changelog <https://github.com/OXID-eSales/media-library-module/blob/v4.0.0/CHANGELOG.md>`_
* OXID Cookie Management powered by Usercentrics von v3.1.0 auf v3.2.1: `Changelog <https://github.com/OXID-eSales/usercentrics/blob/v3.2.1/CHANGELOG.md>`_
* OXID eShop CE von v7.3.0 auf v7.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.4.0/CHANGELOG-7.4.md>`_
* OXID eShop Composer Plugin v7.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.3.0/CHANGELOG-7.x.md>`_
* OXID eShop Demodata CE von v8.0.2 auf v8.1.0: `Changelog <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.1.0/CHANGELOG.md>`_
* OXID eShop Demodata Installer v3.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_
* OXID eShop Doctrine Migration Wrapper v5.4.0: `Changelog <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.4.0/CHANGELOG-5.x.md>`_
* OXID eShop Facts v4.3.0: `Changelog <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.3.0/CHANGELOG-4.x.md>`_
* OXID eShop Unified Namespace Generator v5.2.0: `Changelog <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.2.0/CHANGELOG.md>`_
* OXID eShop Views Generator v2.2.0: `Changelog <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* Twig Admin Theme von v2.6.1 auf v3.0.0: `Changelog <https://github.com/OXID-eSales/twig-admin-theme/blob/v3.0.0/CHANGELOG-3.x.md>`_
* Twig Component von v2.6.0 auf v2.7.0: `Changelog <https://github.com/OXID-eSales/twig-component/blob/v2.7.0/CHANGELOG-2.x.md>`_
* WYSIWYG Editor Module von v5.0.0 auf v6.0.0 (oder auf v5.0.1): `Changelog <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v6.0.0/CHANGELOG.md>`_

OXID eShop PE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop PE Compilation beinhaltet zusätzlich dazu die folgenden Pakete:

* OXID eShop Demodata PE von v8.0.2 auf v8.1.0
* OXID eShop PE von v7.3.0 auf v7.4.0
* Twig Component PE v2.5.0
* Visual CMS Module von v8.0.1 auf v9.0.0 (oder auf v8.0.2)

OXID eShop EE Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop EE Compilation beinhaltet zusätzlich dazu die folgenden Pakete:

* OXID eShop Demodata EE von v8.1.0 auf v8.2.0
* OXID eShop EE von v7.3.0 auf v7.4.0
* Twig Component EE v2.5.0

OXID eShop EE B2B Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die OXID eShop Enterprise B2B Edition 7.4 ist noch nicht veröffentlicht. Sie wird in den nächsten Wochen folgen.

..
    OXID eShop EE B2B Compilation
    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    Die OXID eShop EE B2B Compilation beinhaltet zusätzlich dazu die folgenden Pakete:

    * OXID eShop B2B Approval Procedure Module von v7.2.0 auf v7.3.0
    * OXID eShop B2B Basket Module von v7.2.0 auf v7.3.0
    * OXID eShop B2B Budget Module von v7.2.0 auf v7.3.0
    * OXID eShop B2B Bulk Orders Module von v7.2.0 auf v7.3.0
    * OXID eShop B2B Buying Agent Module von v7.2.0 auf v7.3.0
    * OXID eShop B2B Custom Prices Module von v7.2.0 auf v7.3.0
    * OXID eShop B2B Offers Module von v7.2.0 auf v7.3.0
    * OXID eShop B2B Quick Orders Module von v7.2.0 auf v7.3.0
    * OXID eShop B2B Scheduled Orders Module von v7.2.0 auf v7.3.0
    * OXID eShop B2B Service Products Module von v7.2.0 auf v7.3.0
    * OXID eShop B2B Services Module von v7.2.0 auf v7.3.0

    Für weitere Informationen zu Veröffentlichungen der B2B Edition, siehe die (passwortgeschützte) `OXID eShop Enterprise B2B Edition <https://docs.oxid-esales.com/b2b/de/7.3/releases/b2b-edition-730.html>`_ Dokumentation.

Kompatible OXID Erweiterungen
-----------------------------

* OXAPI GraphQL Base Modul 11.1: `Dokumentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/11.1/>`_
* OXAPI GraphQL Configuration Access Modul 3.0: `Dokumentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/11.1/>`_
* OXAPI GraphQL Storefront Modul 4.2: `Dokumentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/11.1/>`_
* OXAPI GraphQL Storefront Administration Modul 2.1: `Dokumentation [en] <https://docs.oxid-esales.com/interfaces/graphql/en/11.1/>`_
* OXID ERP Schnittstelle 4.3: `Dokumentation [en] (passwortgeschützt) <https://docs.oxid-esales.com/interfaces/erp/en/4.3>`_
* OXID eShop Admin Tools 1.1(?TBD): `Dokumentation <https://docs.oxid-esales.com/modules/admin-tools/de/1.1/>`_
* OXID eShop Consistency Check Tool 1.1(?TBD): `Dokumentation [en] (GitHub) <https://github.com/OXID-eSales/consistency-check-tool/blob/v1.1.0/README.md>`_
* OXID eShop Country VAT Administration 2.4(?TBD): `Dokumentation [en] (GitHub) <https://github.com/OXID-eSales/country-vat-module/blob/v2.4.0/README.md>`_
* OXID eShop Geo-Blocking Modul 2.4: `Dokumentation <https://docs.oxid-esales.com/modules/geo-blocking/de/2.4>`_
* OXID eShop Security Modul 2.1: `Dokumentation <https://docs.oxid-esales.com/modules/security/de/2.1/>`_
* OXID eShop Shipping Cost Compensation Modul 1.2(?TBD): `Dokumentation <https://docs.oxid-esales.com/modules/freeshipping-coupons/de/1.2/>`_
* OXID eShop eVAT Modul 4.3(?TBD): `Dokumentation <https://docs.oxid-esales.com/modules/vat-tbe-services/de/4.3>`_

Update
------

Der Update-Vorgang wird Schritt für Schritt in unserer :doc:`Update-Anleitung <../installation/update>` beschrieben.

Installation
------------

Wenn Sie OXID eShop 7.4 neu installieren möchten, folgen Sie bitte unserer :doc:`Installationsanleitung <../installation/neu-installation/index>`.
