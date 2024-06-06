Rechte und Rollen
=================

Ein Merkmal der Enterprise Edition ist die Rechte- und Rollenverwaltung.

Steuern Sie mit Rechten und Rollen den Zugriff auf anzuzeigende Elemente und verfügbare Funktionen des OXID eShop für einzelne Benutzer und Benutzergruppen.

Dabei unterscheiden wir zwischen den Rechten und den Rollen für den eigentlichen Shop, hier auch als :emphasis:`Frontend bezeichnet, und dem Administrationsbereich, dem :emphasis:`Backend`.

Ein :emphasis:`Recht` regelt den Zugriff auf bestimmte Funktionen, wie den Zugriff auf Artikel und Kategorien oder die Anzeige bestimmter Bereiche der Detailseite von Artikeln.

In :emphasis:`Rollen` werden mehrere Rechte zusammengefasst und Benutzern und Benutzergruppen zugeordnet.

Anwendungsbereich für Rechte und Rollen festlegen
-------------------------------------------------

Schränken Sie bei Bedarf den Anwendungsbereich der Rechte- und Rollenverwaltung ein.

|procedure|

1. Öffnen Sie die Konfigurationsdatei :file:`config.inc.php`.
#. Konfigurieren Sie den Parameter ``$this->blUseRightsRoles``.

   Sie haben folgende Optionen:

   * 0 - Rechteverwaltung deaktiviert
   * 1 - nur im Backend
   * 2 - nur im Frontend
   * 3 - im Backend und Frontend

   Die Einstellung ``$this->blUseRightsRoles = 3`` ist standardmäßig aktiviert.

Rechte und Rollen für den Shop (Frontend) festlegen
---------------------------------------------------

Erteilen Sie verschiedene Berechtigungen für den Shop.

Sie definieren die Berechtigungen im Administrationsbereich.

* in der Artikel- und Kategorienverwaltung

  sowie

* unter :menuselection:`Benutzer verwalten --> Shop Rollen`

.. important::

  **Prinzip der selektiven Rechteeinschränkung**

  Initial haben alle Besucher Ihres OXID eShops alle Rechte.

  Ein Recht wird erst eingeschränkt, sobald mindestens eine Rolle dieses Recht explizit erhält und dieser Rolle mindestens eine Benutzergruppe zugewiesen ist.

  Der zugewiesenen Benutzergruppe müssen keine Benutzer angehören. Es kann also beispielsweise eine Benutzergruppe *Vollzugriff* eingerichtet werden, die der passenden Rolle *Vollzugriff* zugeordnet wird, bei welcher wiederum alle Rechte aktiv sind.

  Somit werden im ersten Schritt alle Rechte eingeschränkt und können anschließend im zweiten Schritt für einzelne Benutzergruppen durch geeignete Rollen wieder aktiviert werden.

Anzeigen von Artikeln und Kategorien einschränken
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #SG: Was ist der typische Anwendungsfall?

Legen Sie fest, dass nur bestimmte Benutzergruppen ausgewählte Artikel und Kategorien :emphasis:`sehen` dürfen.

|procedure|

1. Wählen Sie unter :guilabel:`Artikel verwalten` den Artikel oder die Kategorie.
#. Wählen Sie die Registerkarte :guilabel:`Rechte`.
#. Wählen Sie die Schaltfläche :guilabel:`Benutzergruppen zuordnen (Ausschließlich sichtbar)` (:ref:`oxbaev03`, Pos. 1) und ordnen Sie die gewünschten Benutzergruppen zu (:ref:`oxbaev03`, Pos. 3).

.. _oxbaev03:

.. figure:: ../media/screenshots/oxbaev03.png
   :alt: Anzeigen oder Kaufen von Artikeln/Kategorien einschränken
   :width: 650
   :class: with-shadow

   Abb.: Anzeigen oder Kaufen von Artikeln/Kategorien einschränken

|result|

Nur Benutzer, die den zugewiesenen Benutzergruppen angehören, können die jeweiligen Artikel und Kategorien nach der Anmeldung im Shop sehen.

Allen übrigen Benutzern und Benutzergruppen werden diese Bestandteile des Warenkatalogs nicht angezeigt.

Kaufen von Artikeln und Kategorien einschränken
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #SG: Was ist der typische Anwendungsfall?

Definieren Sie für Artikel und Kategorien, dass sie ausschließlich für bestimmte Benutzergruppen kaufbar sein sollen.

Auch hier erfolgt die Definition durch Zuweisung der jeweiligen Benutzergruppen auf der Registerkarte :guilabel:`Rechte` von Artikeln oder Kategorien (siehe :ref:`einrichtung/artikel/registerkarte-rechte:Registerkarte Rechte`).

|procedure|

1. Wählen Sie unter :guilabel:`Artikel verwalten` den Artikel oder die Kategorie.
#. Wählen Sie die Registerkarte :guilabel:`Rechte`.
#. Wählen Sie die Schaltfläche :guilabel:`Benutzergruppen zuordnen (Ausschließlich kaufbar)` (:ref:`oxbaev03`, Pos. 2) und ordnen Sie die gewünschten Benutzergruppen zu (:ref:`oxbaev03`, Pos. 3).

|result|

Bei Benutzern ohne Berechtigung :emphasis:`fehlt` in Artikelübersicht die Schaltfläche :guilabel:`In den Warenkorb` (:ref:`oxbaev01`, Pos. 2).

Mit der Schaltfläche :guilabel:`Details` (:ref:`oxbaev01`, Pos. 1) können diese Benutzer lediglich die Detailseite des Artikels aufrufen.

.. _oxbaev01:

.. figure:: ../media/screenshots/oxbaev01.png
   :alt: Artikelübersicht mit und ohne Warenkorb
   :width: 650
   :class: with-shadow

   Abb.: Artikelübersicht mit und ohne Warenkorb

Auch in der Detailansicht fehlt die Schaltfläche :guilabel:`In den Warenkorb`, wenn der Kunde nicht am Shop angemeldet ist und der berechtigten Benutzergruppe angehört (:ref:`oxbaev02`).

.. _oxbaev02:

.. figure:: ../media/screenshots/oxbaev02.png
   :alt: Detailansicht Artikel ohne Warenkorb
   :width: 650
   :class: with-shadow

   Abb.: Detailansicht mit Artikel ohne Warenkorb

Zugriff auf Funktionen und Bereiche der Detailseite steuern
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Vergeben Sie Rechte und Rollen, die sich auf den gesamten Warenkatalog beziehen.

Der Shop wird mit folgenden Rechten für den Shop ausgeliefert, die zu Rollen zusammengefasst den gewünschten Benutzergruppen zugeordnet werden können (:ref:`oxbaev10`, Pos. 1):

* Artikel in den Warenkorb legen (:code:`TOBASKET`)
* Artikelpreis anzeigen (:code:`SHOWARTICLEPRICE`)
* Kurzbeschreibung des Artikels anzeigen (:code:`SHOWSHORTDESCRIPTION`)
* Langbeschreibung des Artikels anzeigen (:code:`SHOWLONGDESCRIPTION`)

Diese Rechte und Rollen definieren Sie unter :menuselection:`Benutzer verwalten --> Shop Rollen`.

Verschiedene Rechtekombinationen können Sie in Rollen zusammenfassen und Benutzergruppen zuordnen. Sobald Sie für eine Benutzergruppe ein Recht erteilt haben, gilt für alle anderen Benutzergruppen dieses Recht nicht mehr.


.. todo: #SG: Wie geht das folgende? Was genau bedeutet der Satz?
    Es ist möglich, eigene Rechte zu definieren, die auf View-Klassen und deren Methoden basieren. Über einen vergebenen Ident können Sie in Templates eine rechteabhängige Anzeige realisieren.

.. todo: #SG:  Wie geht "Feld hinzufügen"? Beispiel: IDENT[&class1;class2;function1;function2...]
        In Template: [{ oxhasrights ident='IDENT' }] ... [{ /oxhasrights }]

Rechte: (A)usführen

Das folgende Beispiel illustriert das Prinzip der selektiven Rechteeinschränkung.

Es basiert darauf, dass Rechte standardmäßig allen Benutzern gewährt werden. Ein Recht wird erst eingeschränkt, wenn es explizit einer bestimmten Rolle zugewiesen wird. Nur Benutzergruppen, denen diese Rolle zugewiesen wurde, behalten dieses Recht.

Sie entscheiden sich in unserem Beispiel, dass die Schaltfläche :guilabel:`Warenkorb` bei nicht angemeldeten Benutzern ("Gästen") ausgeblendet ist.

|procedure|

1. Erstellen Sie eine Rolle, der Sie später alle Benutzergruppen zuordnen werden.

   Hintergrund: Benutzergruppen enthalten Benutzer. Benutzer sind Besucher Ihres OXID eShops, die eine E-MAul-Adresse haben, mit der sie sich anmelden.

   Alle anderen Besucher Ihres OXID eShops sind Gäste. Gäste sind Besucher, die sich im Gegensatz zu Benutzern nicht anmelden.

   a. Wählen Sie :menuselection:`Benutzer verwalten --> Shop Rollen`.
   #. Geben Sie im Feld :guilabel:`Titel` den Namen der Rolle ein, in unserem Beispiel :technicalname:`angemeldet`, wählen Sie :guilabel:`Aktiv`, und speichern Sie.

      .. _oxbaev10:

      .. figure:: ../media/screenshots/oxbaev10.png
         :alt: Neue Rolle anlegen
         :width: 650
         :class: with-shadow

         Abb.: Neue Rolle anlegen

      Sogenannte Ident-Parameter werden angezeigt (:ref:`oxbaev10`, Pos. 1).

   #. Markieren Sie denjenigen Ident-Parameter, den Sie steuern wollen.

      In unserem Beispiel wollen Sie steuern, dass Benutzern (angemeldeten Besuchern) der Warenkorb angezeigt wird, Gästen (nicht angemeldeten Besuchern) dagegen nicht.

      Markieren Sie deshalb das Kontrollkästchen :guilabel:`TOBASKET (tobasket;basket)` (:ref:`oxbaev10`, Pos. 2), und speichern Sie Ihre Einstellung.

      Resultat dieser Einstellung ist:

      Diejenigen Benutzergruppen, denen die Rolle :technicalname:`angemeldet` zugeordnet ist, gaben das Recht :technicalname:`TOBASKET`. Bei ihnen wird die Schaltfläche :guilabel:`Warenkorb` angezeigt.

      Allen anderen Benutzergruppen ist das Recht :technicalname:`TOBASKET` entzogen.

      Verallgemeinert: Alle Rechte gelten standardmäßig, solange sie nicht eingeschränkt sind.

      In unserem Beispiel sind das die Ident-Parameter zum Steuern von Langbeschreibung und Kurzbeschreibung und Preis, :ref:`oxbaev10`, Pos. 3). Sie sind keiner Rolle ausdrücklich zugewiesen und deshalb für alle Benutzer oder Gäste gültig.

#. Damit Ihre Einstellungen wirksam werden, ordnen Sie der Rolle Benutzergruppen zu.

   a. Wählen Sie auf der Registerkarte :guilabel:`Benutzer` die Schaltfläche :guilabel:`Benutzergruppen zuordnen`.
   #. Ordnen Sie in unserem Beispiel :emphasis:`alle` Benutzergruppen zu (:ref:`oxbaev11`).

      Hintergrund: Gäste sind keine Benutzer und deshalb in keiner Benutzergruppe enthalten.

      .. _oxbaev11:

      .. figure:: ../media/screenshots/oxbaev11.png
         :alt: Benutzergruppen der Rolle zuordnen
         :width: 650
         :class: with-shadow

         Abb.: Benutzergruppen der Rolle zuordnen

|result|

Prüfen Sie das Ergebnis, indem Sie einen Artikel in Ihrem OXID eShop anzeigen.

   * Angemeldeten Benutzern wird die Schaltfläche :guilabel:`Warenkorb` angezeigt (:ref:`oxbaev12`, Pos. 1).

     .. _oxbaev12:

     .. figure:: ../media/screenshots/oxbaev12.png
        :alt: Warenkorb-Schaltfläche bei angemeldeten Benutzern
        :width: 650
        :class: with-shadow

        Abb.: Warenkorb-Schaltfläche bei angemeldeten Benutzern

   * Nicht angemeldeten Besuchern Ihres OXID eShops wird die Schaltfläche :guilabel:`Warenkorb` nicht angezeigt (:ref:`oxbaev13`).

     .. _oxbaev13:

     .. figure:: ../media/screenshots/oxbaev13.png
        :alt: Keine Warenkorb-Schaltfläche bei nicht angemeldeten Gästen
        :width: 650
        :class: with-shadow

        Abb.: Keine Warenkorb-Schaltfläche bei nicht angemeldeten Gästen

   * Das Ergebnis ist anders als erwartet?

     Leeren Sie den Browser-Cache und versuchen Sie es erneut.

Rechte und Rollen für den Administrationsbereich (Backend) festlegen
--------------------------------------------------------------------

Für den Administrationsbereich lassen sich ebenfalls Rollen definieren.

Bilden Sie damit die verschiedenen Aufgabenbereiche bei der Administration des OXID eShop ab.

Zugriff auf Menüs, Untermenüs, Registerkarten steuern
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Rollen erlauben unterschiedliche Zugriffe auf Menüs und Untermenüs der Navigation und auch auf einzelne Registerkarten des Eingabebereichs.

Damit erhält jeder Bearbeiter seinen benutzerdefinierten Administrationsbereich.

|procedure|

1. Legen Sie unter :menuselection:`Benutzer verwalten --> Admin Rollen` eine Rolle an.
#. Aktivieren Sie die gewünschten Rechte (:ref:`oxbaev05`).

   .. _oxbaev05:

   .. figure::  ../media/screenshots/oxbaev05.png
      :alt: Zugriffsregeln für Navigationselemente festlegen
      :width: 650

      Abb.: Zugriffsregeln für den Navigationselemente festlegen

#. Legen Sie auf der Registerkarte :guilabel:`Objekte` den Zugriff auf Kategorien und Artikel fest.

   Regeln Sie beispielsweise das Anlegen, Ändern und Löschen von Artikeln und Kategorien insgesamt und wenn nötig den Zugriff auf jedes einzelne Steuerelement (Feld, Kontrollkästchen oder Option) des jeweiligen Eingabebereiches.

   Um das Auswahlmenü zu öffnen, wählen Sie das Pfeilsymbol (:ref:`oxbaev06`, Pos. 1).

   .. _oxbaev06:

   .. figure::  ../media/screenshots/oxbaev06.png
      :alt: Abb.: Zugriffsregeln für Artikel und Kategorien festlegen
      :width: 650

      Abb.: Beispiel: Zugriffsregeln für Kategorien festlegen

   Steuern Sie in unserem Beispiel (:ref:`oxbaev06`) den Zugriff auf die Steuerelemente zum Beschreiben von Kategorien (:ref:`oxbaev07`, Pos. 1)

   .. _oxbaev07:

   .. figure::  ../media/screenshots/oxbaev07.png
      :alt: Abb.: Beispiel Steuerelemente zum Beschreiben von Kategorien
      :width: 650

      Abb.: Beispiel: Steuerelemente zum Beschreiben von Kategorien

#. Ordnen Sie der Rolle auf der Registerkarte :guilabel:`Benutzer` die jeweiligen Benutzer oder die Benutzergruppe zu.


.. Intern: oxbaev, Status: