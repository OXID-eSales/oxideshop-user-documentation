Kundeninformationen
===================

Sorgen Sie dafür, dass Ihr OXID eShop rechtssicher ist. Bestimmen Sie, welche Kundendaten Sie ergeben wollen.

Um Zusammenhang mit kundenbezogenen Daten haben Sie folgende Möglichkeiten

* Pflegen Sie CMS-Seiten für die Kundeninformation
* Infomieren Sie Kunden über Cookies
* Legen Sie die Mussfelder für die Registrierung von Kunden fest
* Legen Sie die Pflichtfelder für das Kontaktformular fest

CMS-Seiten für die Kundeninformation editieren
----------------------------------------------

Stellen Sie als Shopbetreiber sicher, dass ihre Kunden beispielsweise informiert sind über

* Sie als Anbieter
* die Bedingungen für Zahlung und Versand
* den Datenschutz
* das Widerrufsrecht

Im OXID eShop sind die wichtigsten Seiten zur Kundeninformation bereits vorbereitet und standardmäßig über die Fußzeile des Shops aufrufbar (:ref:`oxbabh01`).

Füllen Sie die Seiten mit Ihren Texten.

.. _oxbabh01:

.. figure:: /media/screenshots/oxbabh01.png
   :alt: Links zu den Standard-Seiten zur Kundeninformation
   :width: 650
   :class: with-shadow

   Abb.: Links zu den Standard-Seiten zur Kundeninformation

|prerequisites|

* Um rechtliche Fallstricke und in Folge dessen Abmahnungen zu vermeiden,

  * haben Sie haben die Texte, mit denen Sie die Kunde informieren sorgfältig erstellt.
  * haben Sie sichergestellt, dass die Texte regelmäßig auf Aktualität geprüft werden.

  .. tip::

     **Dienstleister wie Trusted Shops beauftragen**
     Suchen Sie sich für korrekte Inhalte von Impressum, AGB, Datenschutz, Versand und Kosten, Widerrufsrecht\&Co Unterstützung.

     In Deutschland und einer Reihe anderer Länder bietet beispielsweise Trusted Shops entsprechendes Knowhow und zertifiziert Onlineshops.

     Das dabei vergebene Gütesiegel bescheinigt den Shops die Einhaltung von Standards, wie Seriosität, Datenschutz und Liefersicherheit.

     Auf der Website von Trusted Shops finden Sie Mustertexten für Mitglieder: `trustedshops.de <http://www.trustedshops.de/>`_.

     Einen Blog zu aktuellen Rechtsthemen finden Sie unter `shopbetreiber-blog.de <http://www.shopbetreiber-blog.de/>`_.

     Weitere Rechtsinformationen für Shopbetreiber finden Sie unter `shopbetreiber-recht.de <http://www.shopbetreiber-recht.de/>`_.


|procedure|

Bearbeiten Sie die Inhalte über das in den Shop integrierte Content Management System (CMS).

1. Wählen Sie im Administrationsbereich :menuselection:`Kundeninformation --> CMS-Seiten`.
2. Wählen Sie in der Übersicht die betreffende CMS-Seite und bearbeiten Sie deren Inhalt.
#. Wählen Sie aus der Dropdown-Liste links über der Übersicht den Eintrag :guilabel:`Kunden-Infos`.
#. Wählen Sie die betreffende CMS-Seite und editieren Sie sie auf der Registerkarte :guilabel:`Stamm`.
#. Speichern Sie Ihre Einstellungen.

   Sobald Sie Ihre Einträge gespeichert haben, ist der neue Inhalt im Shop aufrufbar.

Pflichtfelder für die Registrierung des Kunden festlegen
--------------------------------------------------------

Legen Sie fest, welche Kundendaten (inklusive abweichende Lieferadresse) erforderlich sind für die Registrierung in Ihrem OXID eShop.

|procdure|

1. Wählen Sie :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Weitere Einstellungen`.
#. Legen Sie im Feld :guilabel:`"Muss"-Felder für die Registrierung des Kunden` (:ref:`oxbabh02`, Pos. 1) die erforderlichen Arten von Daten fest.

   Wählen Sie dazu die entsprechenden ``OXIDS`` aus der Kontexthilfe (:ref:`oxbabh02`, Pos. 3).

   .. _oxbabh02:

   .. figure:: /media/screenshots/oxbabh02.png
      :alt: Pflichtfelder für die Registrierung und Kontaktformular festlegen
      :width: 650
      :class: with-shadow

      Abb.: Pflichtfelder für die Registrierung und Kontaktformular festlegen

#. Speichern Sie Ihre Einstellungen.


Pflichtfelder für das Kontaktformular festlegen
-----------------------------------------------

|procdure|

1. Wählen Sie :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Weitere Einstellungen`.
#. Aktivieren Sie die gewünschten Kontrollkästchen :guilabel:`Pflichtfelder des Kontaktformulars`(:ref:`oxbabh02`, Pos. 2).
#. Speichern Sie Ihre Einstellungen.

Cookie-Hinweis konfigurieren
----------------------------

Holen Sie die Zustimmung Ihrer Kunden für die Verwendung von Cookies ein.

* Optional: Informieren Sie Kunden über :emphasis:`technisch notwendige` Cookies
* Erforderlich: Holen Sie die das Einverständnis Ihrer Kunden für :emphasis:`Tracking- und Marketing-Cookies` ein, wenn Sie solche Cookies verwenden.

|background|

Am 1. Oktober 2019 entschied der Europäische Gerichtshof, dass Browser-Cookies nur mit der ausdrücklichen Zustimmung des Besuchers gespeichert werden dürfen. Diese Entscheidung wurde am 28. Mai 2020 vom Bundesgerichtshof bestätigt.

Technisch notwendige Cookies, wie z.B. für Warenkörbe, müssen nicht bestätigt werden, der Besucher sollte aber informiert werden, wie lange sie gültig sind und wofür sie verwendet werden.

Optional: Über technisch notwendige Cookies informieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Informieren Sie Ihre Kunden über technisch notwendige Cookies. Blenden Sie dazu optional die standardmäßige OXID eShop Cookie-Information ein (:ref:`oxbabh03`, Pos. 1).

Im OXID eShop werden :emphasis:`technisch` notwendige Cookies automatisch gesetzt und müssen standardmäßig :emphasis:`nicht` vom Besucher bestätigt werden.

Beispiele hierfür sind:

* ``sid und sid_key``: Identifizieren den Besucher während der Session.
* ``language``: Speichert die verwendete Sprache (167 Minuten Laufzeit).
* ``displayedCookiesNotification``: Speichert die Entscheidung zur Cookie-Einwilligung.

.. _oxbabh03:

.. figure:: /media/screenshots/oxbabh03.png
   :alt: Optionale OXID eShop Cookie-Information
   :width: 650
   :class: with-shadow

   Abb.: Optionale OXID eShop Cookie-Information

|background|

Wenn Sie nur die technisch notwendigen Cookies für den Betrieb einer Website setzen  (z.B. um in einem Shopsystem den Inhalt eines Warenkorbs zu speichern), ist es in Ordnung, den Besucher über den Namen des Cookies zu informieren, wie lange er gültig und wofür er da ist.

Hier ist eine Liste essentieller und technisch notwendiger Cookies, die im Frontend von OXID eShop verwendet werden:


==================================== ============= =========================== ===========================================================
Name                                 Gruppe        Wie lange gültig             Was macht der Cookie
==================================== ============= =========================== ===========================================================
``sid und sid_key``                  essentiell    bis zum Ende der Session,    Diese Cookies identifizieren Sie gegenüber dem Shop mit
                                                   wenn der Browser              einer eindeutigen Kennung, z.B. um den Warenkorb zu speichern.
                                                   geschlossen wird
``language``                         funktional    Laufzeit: 167 Minuten        Speichert die aktuell verwendete Sprache.
``displayedCookiesNotification``     funktional    Laufzeit: 167 Minuten        Speichert die Entscheidung über die Cookie-Einwilligung
                                                                                des Besuchers der Website.
``aHistoryArticles``                 funktional    bis zum Ende der Session,    Speichert eine Liste der zuletzt angesehenen Artikel.
                                                   wenn der Browser
                                                   geschlossen wird
``oxid_`` and ``oxid__autologin``    funktional    Laufzeit: 60 Minuten         Speichert Informationen zum Autologin eines Besuchers
                                                                                Deines Online-Shops.
``amazon_Login_state_cache``         funktional    Laufzeit: 60 Minuten         Speichert Informationen – ebenfalls für den Autologin,
                                                                                wenn ein Besucher Deines Online-Shops gleichzeitig bei
                                                                                Amazon eingeloggt ist. (Nur gültig, wenn das AmazonPay-Modul
                                                                                verwendet wird.)
==================================== ============= =========================== ===========================================================



.. todo: #HR: Ist die Liste vollständig, brauchen wir sie?

|procedure|

Um die standardmäßige OXID eShop Cookie-Information einzublenden, tun Sie Folgendes:

1. Wählen Sie :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Weitere Einstellungen`.
#. Aktivieren Sie das Kontrollkästchen :guilabel:`Kunden müssen der Verwendung von Cookies zustimmen`.
#. Speichern Sie Ihre Einstellungen.

.. todo: #HR: Wie ich die Cookie Note anpassen wenn ich das wil?. Beschreiben wir das in der Dev-Doku? Ist der folgende Abschnitt "Session and Cookies" relevant?

Weitere Informationen finden Sie in der Entwickler-Dokumentation unter `Configuration file config.inc.php <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/configincphp.html>`_ im Kapitel `Session and Cookies <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/configincphp.html#session-and-cookies>`_.


Erforderlich: Zustimmung für Tracking- und Marketing-Cookies einholen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Für :emphasis:`Tracking- und Marketing-Cookies` benötigen Sie die ausdrückliche Zustimmung des Besuchers.

Nutzen Sie dafür eine externe Consent Management Platform (CMP). CMPs ermöglichen die einfache Verwaltung von Cookie-Zustimmungen.

Diese Lösungen sind oft als SaaS verfügbar und bieten unterschiedliche Preismodelle, abhängig von Seitenanzahl, Sprachen und Domains.

Sie haben beispielsweise folgende Möglichkeiten:

* Empfehlung: Nutzen Sie das Modul :productname:`OXID Cookie Management-Modul powered by usercentrics` (:ref:`oxbabh04`).

  .. _oxbabh04:

  .. figure:: /media/screenshots/oxbabh04.png
     :alt: Beispiel: Cookie Note von usercentrics
     :width: 650
     :class: with-shadow

     Abb.: Beispiel: Cookie Note von usercentrics

  Weitere Informationen finden Sie unter `OXID Cookie Management <https://docs.oxid-esales.com/modules/usercentrics/de/latest/einfuehrung.html>`_.

* Alternativ: Nutzen Sie ein Modul von einem Drittanbieter im `OXID Solution Hub <https://solutionhub.oxid-esales.com/all-products/>`.

Beispiel: Google Analytics aktivieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Nutzen Sie bei Bedarf Google Analytics. Um es zu aktivieren, geben Sie Ihre Google Analytics ID ein.

|procedure|

1. Wählen Sie unter :menuselection:`Erweiterungen --> Themes` Ihr Theme.
#. Wählen Sie :menuselection:`Einstell. --> Google Analytics`.
#. Machen Sie die erforderlichen Eingaben.

   .. todo: #HR: Wieso ist GA standardmäßig aktiviert, aber ohne GA Tracking ID? Heißt das, GA ist standardmäßig aktiviert, und ich muss es z.B. mit Usercentrics abfangen?

#. Speichern Sie Ihre Einstellungen.
#. Stellen Sie sicher, dass Sie durch eine entsprechende Cookie Note den Kunden ermöglichen, Google Analytics zu deaktivieren.

   Nutzen Sie beispielsweise das Modul `OXID Cookie Management-Modul powered by usercentrics <https://docs.oxid-esales.com/modules/usercentrics/de/latest/>`_.

   .. todo: #HR: Wäre das der notwendige letzte Schritt? Angenommen ich aktiviere Google Tracking: wie implementiere ich dann eine entsprechende Cookie Note, die es dem User erlaubt, es abzuschalten? W beschreiben wir das? Siehe oben.

|result|

Der JavaScript-Code lädt Tracking-Cookies mit den Namen ``ga``, ``_gid`` und ``_gat_gtag_UA*`` nach.

Leider können wir nicht zu 100% sagen, was diese tun und wie lange sie gültig sind, da es sich um Cookies handelt, die von Google gesetzt werden und jederzeit nach Belieben geändert werden könnten.

Ihre Consent Management-Lösung erlaubt es Ihren Kunden in jedem Fall, das Tracking zu deaktivieren (:ref:`oxbabh04a`).

.. _oxbabh04a:

.. figure:: /media/screenshots/oxbabh04.png
   :alt: Beispiel: Cookie Note von usercentrics
   :width: 650
   :class: with-shadow

   Abb.: Beispiel: Cookie Note von usercentrics


.. Intern: oxbabh, Status: