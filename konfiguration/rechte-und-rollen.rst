Rechte und Rollen
=================

Ein Feature der Enterprise Edition ist die Rechte- und Rollenverwaltung.

Steuern Sie mit Rechten und Rollen den Zugriff auf anzuzeigende Elemente und verfügbare Funktionen des OXID eShop für einzelne Benutzer und Benutzergruppen.

Dabei unterscheiden wir zwischen den Rechten und den Rollen für den eigentlichen Shop, hier auch als :emphasis:`Frontend bezeichnet, und dem Administrationsbereich, dem :emphasis:`Backend`.

Ein :emphasis:`Recht` regelt den Zugriff auf bestimmte Funktionen, wie den Zugriff auf Artikel und Kategorien oder die Anzeige bestimmter Bereiche der Detailseite von Artikeln.

In :emphasis:`Rollen` werden mehrere Rechte zusammengefasst und Benutzern und Benutzergruppen zugeordnet.

Konfigurieren Sie die Rechte- und Rollenverwaltung in der Konfigurationsdatei :file:`config.inc.php` über den Parameter ``$this->blUseRightsRoles``.

Sie haben folgende Optionen:

* 0 - Rechteverwaltung deaktiviert
* 1 - nur um Backend
* 2 - nur um Frontend
* 3 - in Backend und Frontend

.. todo: #SP: Einstellung ``$this->blUseRightsRoles = 3`` Ist das standardmäßig aktiviert?

Rechte und Rollen für den Shop (Frontend)
-----------------------------------------
Für den Shop können verschiedene Berechtigungen erteilt werden. Die Definition erfolgt im Administrationsbereich in der Artikel- und Kategorienverwaltung sowie unter :menuselection:`Benutzer verwalten --> Shop Rollen`.

Anzeigen von Artikeln und Kategorien
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #SP: Was ist der typische Anwendungsfall?

Sie können festlegen, dass nur bestimmte Benutzergruppen ausgewählte Artikel und Kategorien sehen dürfen.

Die Definition erfolgt auf der Registerkarte :guilabel:`Rechte` von Artikeln und Kategorien, indem eine oder mehrere Benutzergruppen zugewiesen werden.

Es handelt sich dabei um ein ausschließliches Recht. Nur für Benutzer, die den zugewiesenen Benutzergruppen angehören, sind die jeweiligen Artikel und Kategorien nach Anmeldung am Shop sichtbar. Allen übrigen Benutzern und Benutzergruppen werden diese Bestandteile des Warenkatalogs niemals angezeigt.

Kaufen von Artikeln und Kategorien
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #SP: Was ist der typische Anwendungsfall?

Definieren Sie für Artikel und Kategorien, dass sie ausschließlich für bestimmte Benutzergruppen kaufbar sein sollen.

Auch hier erfolgt die Definition durch Zuweisung der jeweiligen Benutzergruppen auf der Registerkarte :guilabel:`Rechte` von Artikeln oder Kategorien (siehe :ref:`einrichtung/artikel/registerkarte-rechte:Registerkarte Rechte`).

Bei Benutzern ohne Berechtigung fehlt in der Artikelübersicht die Schaltfläche :guilabel:`In den Warenkorb` (:ref:`oxbaev01`).

Mit der Schaltfläche :guilabel:`Mehr Informationen` können diese Benutzer lediglich die Detailseite des Artikels aufrufen.

.. todo: EN: Schaltfläche :guilabel:`To cart`, Schaltfläche :guilabel:`Details`

.. _oxbaev01:

.. figure:: ../media/screenshots/oxbaev01.png
   :alt: Artikelübersicht ohne Warenkorb
   :width: 650
   :class: with-shadow

   Abb.: Artikelübersicht ohne Warenkorb

Auch in der Detailansicht fehlt die Schaltfläche :guilabel:`In den Warenkorb legen`, wenn der Kunde nicht am Shop angemeldet ist und der berechtigten Benutzergruppe angehört (:ref:`oxbaev02`).

.. _oxbaev02:

.. figure:: ../media/screenshots/oxbaev02.png
   :alt: Detailansicht Artikel ohne Warenkorb
   :width: 650
   :class: with-shadow

   Abb.: Detailansicht mit Artikel ohne Warenkorb

Zugriff auf Funktionen und Bereiche der Detailseite
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Rechte und Rollen können auch auf den gesamten Warenkatalog bezogen vergeben werden.

Beispiel: Zeigen Sie nur angemeldeten Kunden Preise an.

.. todo: #SP: Was ist der typische Anwendungsfall? "Zeigen Sie nur angemeldeten Kunden Preise an."?

Der Shop wird mit folgenden Rechten für den Shop ausgeliefert, die zu Rollen zusammengefasst den gewünschten Benutzergruppen zugeordnet werden können (:ref:`oxbaev03`):

* Artikel in den Warenkorb legen (TOBASKET)
* Artikelpreis anzeigen (SHOWARTICLEPRICE)
* Kurzbeschreibung des Artikels anzeigen (SHOWSHORTDESCRIPTION)
* Langbeschreibung des Artikels anzeigen (SHOWLONGDESCRIPTION)

Diese Rechte und Rollen werden unter :menuselection:`Benutzer verwalten --> Shop Rollen` definiert.

Verschiedene Rechtekombinationen können in Rollen zusammengefasst und Benutzergruppen zugeordnet werden. Sobald für eine Benutzergruppe ein Recht erteilt wurde, gilt für alle anderen Benutzergruppen dieses Recht nicht mehr.

.. hint:: Initial haben alle Nutzer alle Rechte. Ein Recht wird erst eingeschränkt, sobald mindestens eine Rolle dieses Recht explizit erhält und dieser Rolle mindestens eine Benutzergruppe zugewiesen ist. Der zugewiesenen Benutzergruppe müssen keine Benutzer angehören. Es kann also beispielsweise eine Benutzergruppe *Vollzugriff* eingerichtet werden, die der passenden Rolle *Vollzugriff* zugeordnet wird, bei welcher wiederum alle Rechte aktiv sind. Somit werden im ersten Schritt alle Rechte eingeschränkt und können anschließend im zweiten Schritt für einzelne Benutzergruppen durch geeignete Rollen wieder aktiviert werden.

.. todo: SB: Wie geht das folgende?

Es ist möglich, eigene Rechte zu definieren, die auf View-Klassen und deren Methoden basieren. Über einen vergebenen Ident lässt sich in Templates eine rechteabhängige Anzeige realisieren.

.. _oxbaev03:

.. figure:: ../media/screenshots/oxbaev03.png
   :alt: Rechte für Detailansicht (Rechte und Rollen)
   :width: 650
   :class: with-shadow

   Abb.: Rechte für Detailansicht (Rechte und Rollen)

Auf der Detailseite, auf dem Screenshot als Beispiel zu sehen, und auch in den Artikelübersichten werden keine Preise für nicht berechtigte Benutzer angezeigt (:ref:`oxbaev04`).

.. _oxbaev04:

.. figure:: ../media/screenshots/oxbaev04.png
   :alt: Detailansicht Artikel (Rechte und Rollen)
   :width: 650
   :class: with-shadow

   Abb.: Detailansicht Artikel (Rechte und Rollen)

Rechte und Rollen für den Administrationsbereich (Backend)
----------------------------------------------------------
Für den Administrationsbereich lassen sich ebenfalls Rollen definieren, um die verschiedenen Aufgabenbereiche bei der Administration des OXID eShop abbilden zu können.

Zugriff auf Menüs, Untermenüs, Registerkarten
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Die Rollen erlauben unterschiedliche Zugriffe auf Menüs und Untermenüs der Navigation und auch auf einzelne Registerkarten des Eingabebereiches. Damit erhält jeder Bearbeiter seinen benutzerdefinierten Administrationsbereich. Diese Rechte und Rollen werden unter :menuselection:`Benutzer verwalten --> Admin Rollen` definiert und den jeweiligen Benutzern zugeordnet.

.. image:: ../media/screenshots/oxbaev05.png
   :alt: Zugriff im Administrationsbereich
   :height: 335
   :width: 650

Zugriff auf Artikel und Kategorien
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Für die Bearbeitung von Artikeln und Kategorien können die Rechte sehr differenziert definiert werden. Sie regeln beispielsweise das Anlegen, Ändern und Löschen von Artikeln und Kategorien insgesamt und wenn nötig den Zugriff auf jedes einzelne Steuerelement (Feld, Kontrollkästchen oder Option) des jeweiligen Eingabebereiches.

.. image:: ../media/screenshots/oxbaev06.png
   :alt: Zugriff im Administrationsbereich
   :height: 335
   :width: 650


.. Intern: oxbaev, Status: