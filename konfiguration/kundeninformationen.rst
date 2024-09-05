Kundeninformationen
===================

Sorgen Sie dafür, dass Ihr OXID eShop rechtssicher ist. Bestimmen Sie, welche Kundendaten Sie ergeben wollen.

Um Zusammenhang mit kundenbezogenen Daten haben Sie folgende Möglichkeiten

* Stellen Sie Informationen auf den standardisiereten Kundeninformationsseiten bereit
* Infomieren Sie Kunden über Cookies
* Legen Sie die Mussfelder für registrierte Kunden fest
* Legen Sie die Pflichtfelder für das Kontaktformular fest


CMS-Seiten für die Kundeninformation editieren
----------------------------------------------

Stellen Sie als Shopbetreiber sicher, dass ihre Kunden beispielsweise informiert sind über

* den Anbieter
* die Bedingungen für Zahlung und Versand
* den Datenschutz
* das Widerrufsrecht

Im OXID eShop sind die wichtigsten Seiten zur Kundeninformation bereits vorbereitet und standardmäßig über die Fußzeile des Shops aufrufbar.

.. _oxbabh01:

.. figure:: /media/screenshots/oxbabh01.png
   :alt: Standard-Seiten zur Kundeninformation
   :width: 650
   :class: with-shadow

   Abb.: Standard-Seiten zur Kundeninformation

|prerequisites|

* Um rechtliche Fallstricke und in Folge dessen Abmahnungen zu vermeiden,

  * haben Sie haben die Texte, mit denen Sie die Kunde informieren sorgfältig erstellt.
  * haben Sie sichergestellt, dass die Texte regelmäßig auf Aktualität geprüft werden.

  .. tip::

     **Dienstleister wie Trusted Shops beauftragen**
     Suchen Sie sich für korrekte Inhalte von Impressum, AGB, Datenschutz, Versand und Kosten, Widerrufsrecht\&Co Unterstützung.

     In Deutschland und einer Reihe anderer Länder bietet beispielsweise Trusted Shops entsprechendes Knowhow und zertifiziert Onlineshops.

     Das dabei vergebene Gütesiegel bescheinigt den Shops die Einhaltung von Standards, wie Seriosität, Datenschutz und Liefersicherheit.

     Auf der Website von Trusted Shops finden Sie Mustertexten für Mitglieder: `www.trustedshops.de <http://www.trustedshops.de/>`_.

     Einen Blog zu aktuellen Rechtsthemen finden Sie unter `www.shopbetreiber-blog.de <http://www.shopbetreiber-blog.de/>`_.

     Weitere Rechtsinformationen für Shopbetreiber finden Sie unter `www.shopbetreiber-recht.de <http://www.shopbetreiber-recht.de/>`_.


|procedure|

Bearbeiten Sie die Inhalte können über das in den Shop integrierte Content Management System (CMS).

1. Wählen Sie im Administrationsbereich :menuselection:`Kundeninformation --> CMS-Seiten`.
2. Wählen Sie in der Übersicht die betreffende CMS-Seite und bearbeiten Sie deren Inhalt.
#. Wählen Sie aus der Dropdown-Liste links über der Übersicht den Eintrag :guilabel:`Kunden-Infos`.
#. Wählen Sie die betreffende CMS-Seite und editieren Sie sie auf der Registerkarte :guilabel:`Stamm`.
#. Speichern Sie Ihre Einstellungen.

   Sobald Sie Ihre Einträge gespeichert haben, ist der neue Inhalt im Shop aufrufbar.

Pflichtfelder für die Registrierung des Kunden festlegen
--------------------------------------------------------

|procdure|

1. Wählen Sie :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Weitere Einstellungen`.
#. Legen Sie im Feld :guilabel:`"Muss"-Felder für die Registrierung des Kunden` Fest, welche Kundendaten (inklusive abweichende Lieferadresse) erforderlich sind für die Registrierung in Ihrem OXID eShop.

   Wählen Sie die entsprechenden ``OXIDS`` aus der Kontexthilfe.

   .. _oxbabh02:

   .. figure:: /media/screenshots/oxbabh02.png
      :alt: Pflichtfelder für die Registrierung festlegen
      :width: 650
      :class: with-shadow

      Abb.: Pflichtfelder für die Registrierung festlegen

#. Speichern Sie Ihre Einstellungen.


Pflichtfelder für das Kontaktformular festlegen
-----------------------------------------------

|procdure|

1. Wählen Sie :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Weitere Einstellungen`.
#. Aktivieren Sie die gewünschten Kontrollkästchen :guilabel:`Pflichtfelder des Kontaktformulars`(:ref:`oxbabh02`, Pos. 2).
#. Speichern Sie Ihre Einstellungen.

Cookie-Hinweis konfiguriren
---------------------------

Holen Sie die Zustimmung Ihrer Kunden für die Verwendung von Cookies ein.

Optional: Über technisch notwendige Cookies informieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Informieen Sie Ihre Kunden über technisch notwendige Cookies.

Im OXID eShop werden :emphasis:`technisch` notwendige Cookies automatisch gesetzt und müssen standardmäßig :emphasis:`nicht` vom Besucher bestätigt werden.

Beispiele hierfür sind:

* ``sid und sid_key``: Identifizieren den Besucher während der Session.
* ``language``: Speichert die verwendete Sprache (167 Minuten Laufzeit).
* ``displayedCookiesNotification``: Speichert die Entscheidung zur Cookie-Einwilligung.

|background|

Am 1. Oktober 2019 entschied der Europäische Gerichtshof, dass Browser-Cookies nur mit der ausdrücklichen Zustimmung des Besuchers gespeichert werden dürfen. Diese Entscheidung wurde am 28. Mai 2020 vom Bundesgerichtshof bestätigt.

Technisch notwendige Cookies, wie z.B. für Warenkörbe, müssen nicht bestätigt werden, der Besucher sollte aber informiert werden, wie lange sie gültig sind und wofür sie verwendet werden.

Tracking- und Marketing-Cookies implementieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Für :emphasis:`Tracking- und Marketing-Cookies` benötigen Sie die ausdrückliche Zustimmung des Besuchers.

Nutzen Sie dafür eine externe Consent Management-Lösung.

Sie haben beispielsweise folgende Möglichkeiten:

* Empfehlung: Nutzen Sie das Modul :productname:`OXID Cookie Management-Modul powered by usercentrics`.

   Weitere Informationen finden Sie unter `OXID Cookie Management <https://docs.oxid-esales.com/modules/usercentrics/de/latest/einfuehrung.html>`_.

* Cookie-Consent-Plattformen (CMPs): Externe Lösungen, wie CMPs (Consent Management Platforms) ermöglichen die einfache Verwaltung von Cookie-Zustimmungen.

  Diese Lösungen sind oft als SaaS verfügbar und bieten unterschiedliche Preismodelle, abhängig von Seitenanzahl, Sprachen und Domains.

* Google Analytics Integration: Mit den OXID-Themes „Flow“ und „Wave“ kann die Google Analytics ID im Admin-Panel eingegeben werden, um das Tracking zu aktivieren.

  Dabei werden Cookies wie ga, _gid und _gat_gtag_UA* von Google gesetzt.

* Nutzen Sie ein Open-Source-Plugin.

.. Intern: oxbabh, Status: