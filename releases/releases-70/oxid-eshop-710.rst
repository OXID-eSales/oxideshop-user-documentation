OXID eShop 7.1.0
================

Release-Datum: 26.03.2024

Die wichtigsten Änderungen im Überblick
---------------------------------------


.. todo: https://oxidesalesag-my.sharepoint.com/:p:/g/personal/heike_reuter_oxid-esales_com/EX0qy6fbpnBDvo5AU_xO8ZMBbf_DXJpk6tpfUr6AGu4OAA?e=jpN2of
  .. todo: #SB: HR Was ist das wichtigste an 7.1?: Barrierefreiheit; --> #SB fragen: eye able assist Modul, Apay- und Demodaten
    VCMS Bundle: #MF Mikkel fragen: was ist neu
    neue PHP-Version
    Modulabhängigkeiten
    Subshop-Services
    Bugfixes, s.Changelog CE

Sicherheit und Zuverlässigkeit
------------------------------

Wir haben die Kompatibilität des OXID eShop verbessert, um sowohl die Sicherheit als auch die Performance zu gewährleisten. Zu den Maßnahmen zählen:

* Die Unterstützung für PHP Version 8.2, um aktuelle und sichere Software-Umgebungen zu garantieren.

  Weitere Informationen zum Lebenszyklus von PHP-Versionen finden Sie unter https://www.php.net/supported-versions.php.

  Anmerkung: Der :productname:`OXID eShop` 7.1 unterstützt PHP 8.1/8.2.

* Ein Update auf Symfony 6.3 gewährleistet die Kompatibilität mit PHP 8.2 und sorgt für eine zukunftssichere Basis unseres Systems.

* Die Implementierung von PHPUnit Version 10 ermöglicht modernes Testing und Qualitätssicherung, um die Zuverlässigkeit des :productname:`OXID eShop` weiter zu erhöhen.


Neue Funktionen für Anwender
----------------------------

Visual CMS
^^^^^^^^^^

Formatieren Sie Ihre Texte komfortabel. Das :productname:`Visual CMS`-Modul ist jetzt standardmäßig in der Professional Edition enthalten.

.. todo: #SB: D.h. nicht mehr bezahlpflichtig?
.. todo: #MF: so korrekt und vollständig?:

Mit der :productname:`OXID eShop` Version 7.1 haben wir zudem den Code verbessert, um das Modul leistungsfähiger für zukünftige Anforderungen zu machen:

* Legen Sie sofort los: Um Ihnen den Einstieg zu erleichtern, haben wir unsere Dokumentation mit praktischen Beispielen angereichert.
* Hinterlegen Sie für jedes Bild im Karussell einen Link, den der Besucher anklicken kann: Wir haben das Karussell-Widget entsprechend erweitert.

  .. todo: #MF: Link auf Doku-Kapitel ergänzen: "Weitere Informationen finden Sie unter <URL>."

* Erzeugen Sie Bilder in besserer Qualität und auf einfachere Weise:

  * Löschen Sie den Thumbnail-Ordner, dann werden die Thumbnails automatisch neu generiert.
  * Generieren Sie Thumbnails für Ihre Bilder im SVG Format
  * Generieren Sie Thumbnails für Ihre Bilder mit Transparenz
  * Beeinflussen Sie die Darstellung Ihre Bilder über CSS-Klassen

  .. todo: #MF: Link auf Doku-Kapitel ergänzen: "Weitere Informationen finden Sie unter <URL>."
  .. todo: #SB/#MF: Was heißt bedarfsorientiert?: "Wir haben das bedarfsorientierte Erstellen von Thumbnails verbessert."
  .. todo: #SB/#MF Klären: Erwähnen wir folgendes? Auch das Hochladen und Verlinken von Dateien wie PDFs in Ihrem WYSIWYG-Editor ist nun möglich. Beachten Sie, dass diese Funktion noch experimentell und nicht vollständig ausgereift ist.
  .. todo: #SB/#MF: Brauchen wir das: "- bei Speicherung von Inhalten werden nun Fehler im individuellen CSS/LESS gemeldet - erleichterte Kontrolle über Alt-Attributes für Bilder (wird vermutlich nicht mehr für 7.1 kommen)"

* Die Sicherheit beim Hochladen von Bildern habe wir erhöht, indem wir über die :file:`config.inc.php`-Datei die erlaubten Formate strikt definieren.

 .. todo: #SB/#MF: Kann/soll der Shopbetreiber die :file:`config.inc.php`-Datei  evtl. anpassen?

* Nutzen Sie folgende neuen Dateiformate:

  * AVIF: Beschleunigen Sie das Laden Ihrer Webseiten durch die höhere Kompression im Vergleich zu WebP. Binden Sie über Widgets Animationen ein.
  * PDF
  * ZIP

  .. todo: #SB/#MF: Was ist der use case für für PDF und ZIP?

* Profitieren Sie von der verbesserten Unterstützung folgender Dateiformate:
  * GIF
  * SVG
  * WebP

  .. todo: #SB/#MF: Was haben wir verbessert?

* Erweitern Sie Shortcodes leichter. Damit Sie sie leichter einbinden, haben wir die Schnittstelle zum Einbinden neuer Shortcodes übersichtlicher und einfacher gestaltet.

  .. todo: #MF: Link auf Doku-Kapitel ergänzen: "Weitere Informationen finden Sie unter <URL>."

* Erstellen Sie Ordner, um Ihre Dateien besser zu organisieren.

  Dazu haben wir das MediaLibrary-Modul zu einem eigenständigen Modul weiterentwickelt.

  .. todo: #HB/#MF: Erwähnen wir Folgendes? Ist das Umbenennen fertig? "Benennen Sie Dateien und Ordner bei Bedarf um. Das erfordert jedoch vorerst noch etwas Arbeit, weil wir einfache Dateipfade verwenden. Das heißt, die Beziehungen im VisualCMS und WYSIWYG-Editor werden nicht automatisch aktualisiert."
  .. todo: #MF: Link auf Doku-Kapitel ergänzen: "Weitere Informationen finden Sie unter <URL>."

* Profitieren Sie von einer verbesserten Bedienfreundlichkeit. Dazu haben wir Parsing-Fehler weiter verringert.

Barrierefreien Zugang ermöglichen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Sorgen Sie durch erhöhte digitale Barrierefreiheit dafür, dass mehr Kunden Ihr :productname:`OXID eShop` nutzen können.

Implementieren Sie dazu die Barrierefreiheitsrichtlinien gemäß des Behindertengleichstellungsgesetzes (BFSG) und der Web Content Accessibility Guidelines (WCAG).

Installieren Sie dazu das Eye-Able Assist-Modul als kostenlose Teaserversion.

.. todo: #SB: Wie kriege ich das Modul?

Im Administratorbereich Ihres :productname:`OXID eShop` erscheint dann ein Vorschau-Bericht.

.. todo: #SB: Wozu dient das Modul, was macht es, was ist das Ergebnis?

.. todo: Screenshot Eye Able Kurzreport (report teaser) ergänzen
.. todo: Evtl. Screenshot Eye Able Report ergänzen



.. todo: #05

Zeitgesteuerte Artikel leichter unterscheiden
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Zeitgesteuerte Artikel haben in der Artikel-Liste ein gesondertes Status-Icon.
.. todo: tbd: Screenshot, sobald Funktion verfügbar, siehe die Dokulinks unten
     Admin | core | Performance; sth time period

Weitere Informationen finden Sie

* ìn der Beschreibung, wie Sie :ref:`Artikel zeitgesteuert aktivieren <zeitaktivierung>`.
* unter :ref:einrichtung/artikel/registerkarte-stamm#

.. todo: #HR/#DK: tbd: Install 7.1, test function, add screenshot in docu where applicable




Neue Funktionen für Entwickler
------------------------------

Abhängigkeiten zwischen Modulen definieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #04

Wir entwickeln Modul-Pakete, beispielsweise OXAPI, B2B und VisualCMS, bei denen Module aufeinander aufbauen und von bereitgestellten Services abhängig sind.

* Wenn Sie als Administrator versuchen, ein Modul ohne erfüllte Abhängigkeiten zu aktivieren, wird angezeigt wird, welche Module vorher aktiviert werden müssen.

  Ebenso können Sie ein Modul nicht deaktivieren, das von anderen benötigt wird.

* Um unbeabsichtigte Fehlaktivierungen durch Administratoren zu vermeiden, definieren Sie als Modul-Entwickler Abhängigkeiten zwischen Modulen, falls erforderlich.

  Verwenden Sie diese Option, wenn Sie ein Basismodul mit Kernfunktionen haben, die zwingend aktiv sein müssen, damit andere Module funktionieren.

  Weitere Informationen finden Sie in der Entwicklerdokumentation unter `Defining dependencies between modules <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/module/module_dependencies.html>`_.

.. todo: #tbd: URL verifizieren


Symfony DI-Container nutzen
^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Services pro Subshop individuelles konfigurieren

  .. todo: #03

  Überschreiben Sie gezielt pro Subshop die vom Shop verwendeten Services.

  Der Symfony DI Container im OXID eShop ermöglicht Ihnen damit ein noch flexibleres und effizienteres Verwalten von Services.

  Weitere Informationen über Symfony DI-Container zum Anpassen und Verwalten von Services finden Sie in der Entwickler-Dokumentation unter `Use services in non-DI classes <https://docs.oxid-esales.com/development/tell_me_about/service_container.html>`_.

* Services in Non-DI-Klassen nutzen

  .. todo: #01

  Erleichtern Sie Ihre Arbeit als Modul-Entwickler, indem Sie auch in Bereichen, die nicht für Dependency Injection (DI) vorgesehen sind, auf den zentralen Symfony DI-Container zugreifen.

  Weitere Informationen finden Sie in der Entwickler-Dokumentation unter `Use services in non-DI classes <https://docs.oxid-esales.com/development/modules_components_themes/module/module_services.rst#use-services-in-non-di-classes.html>`_.

Installieren von Paketen über die Kommandozeilenschnittstelle
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #02
.. todo: SB/HR: HR so OK: jetzt regulär; Ist das ein neues Feature? So weit ich sehe, haben wir nur ein neues Kapitel in der Dev-Doku.; vorher Dev-Komponente nachzuinstalieren

Um ein Theme zu aktivieren, müssen Sie nicht die Administratoroberfläche im OXID eShop verwenden.

Nutzen Sie den Befehl :code:`bin/oe-console oe:theme:activate <theme>`.

Weitere Informationen finden Sie in der Entwickler-Dokumentation unter

* `Activation <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/theme/theme_activation_via_cli.html>`_
* `Activating the frontend theme <https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/twig_template_engine/installation.html#after-twig-engine-installation>`_

Clean Up
--------


Einladungs-Funktion
^^^^^^^^^^^^^^^^^^^

.. todo: #07
.. todo: SB Shop sendet E-mail: geht aus Datenschutz-/Spamschutzgründen nicht mehr
Öffentlicher Wunschzettel
.. todo: #SB: if Bonus points deprecated, why are they still displayed under User | :guilabel:`Erweitert` ?
.. todo: #tbd: Screenshot  DK provides information: as of 7.1 deprecated: removed in 8.0, may be refactored in the future

Um Ihren registrierten Kunden die Möglichkeit zu bieten, Freunde einzuladen und dafür Bonuspunkte zu erhalten, konnten Sie bis zur Version 7.0 des OXID eShops unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Einladungen` die Funktion Einladungen aktivieren.

Aufgrund des Risikos von Missbrauch durch Spam-Attacken haben wir uns jedoch entschieden, diese Funktion zurückzubauen.

Um eine solche Funktion sicher und effektiv zu nutzen, empfehlen wir die Entwicklung eines speziellen Moduls für den OXID eShop. Im Missbrauch vorzubeugen, integrieren Sie beispielsweise folgende Sicherheitsmaßnahmen:

* Implementieren eines Captcha-Systems: Bevor ein registrierter Kunde jemanden einladen kann, muss er ein Captcha lösen. Dies verhindert automatisierte Bots von der Nutzung des Einladungssystems.
* Begrenzung der Einladungen: Setzen Sie eine Höchstzahl an Einladungen fest, die ein Kunde innerhalb eines bestimmten Zeitraums senden kann. Dies vermindert die Wahrscheinlichkeit von Missbrauch, da es die Anzahl der möglichen Spam-Einladungen einschränkt.
* Bestätigung durch den Eingeladenen: Statt direkt Bonuspunkte für das bloße Versenden einer Einladung zu vergeben, könnten Punkte erst gutgeschrieben werden, nachdem der Eingeladene die Einladung annimmt und bestimmte Kriterien erfüllt (z.B. eine Bestellung tätigt).
* Überprüfung der E-Mail-Adressen: Implementieren Sie eine Prüfung der E-Mail-Adressen auf Gültigkeit und auf bekannte Spam-Domains, um zu verhindern, dass Einladungen an zufällig generierte oder für Spam bekannte Adressen gesendet werden.
* Benutzerfeedback und Berichterstattung: Ermöglichen Sie Ihren Nutzern, Missbrauch zu melden. Dies hilft Ihnen, potentielle Schwachstellen im System schnell zu identifizieren und zu adressieren.
* Anpassbare E-Mail-Vorlagen: Geben Sie den Nutzern die Möglichkeit, die Einladungs-E-Mails zu personalisieren, aber stellen Sie sicher, dass der Text bestimmte Richtlinien erfüllt und nicht missbräuchlich verwendet werden kann.
* Monitoring und Analyse: Überwachen Sie die Nutzung des Einladungssystems aktiv, um Anomalien oder Missbrauchsmuster frühzeitig zu erkennen. Analysieren Sie die Daten regelmäßig, um die Sicherheitsmaßnahmen entsprechend anzupassen.


To offer your registered customers the option of inviting friends and receiving bonus points in return, up to version 7.0 of the OXID eShop you could activate the Invitations function under :menuselection:`Master data --> Basic settings --> Settings --> Invitations`. --> Invitations` to activate the Invitations function.

However, due to the risk of misuse by spam attacks, we have decided to remove this function.

To use such a function safely and effectively, we recommend developing a special module for the OXID eShop. To prevent misuse, integrate the following security measures, for example:

* Implementation of a captcha system: Before a registered customer can invite someone, they must solve a captcha. This prevents automated bots from using the invitation system.
* Limitation the number of invitations: Set a maximum number of invitations that a customer can send within a certain period of time. This reduces the likelihood of abuse as it limits the number of possible spam invitations.
* Confirmation by the invitee: Instead of directly awarding bonus points for simply sending an invitation, points could be credited only after the invitee accepts the invitation and fulfills certain criteria (e.g. places an order).
* Verification of e-mail addresses: Implement email address validation and known spam domain checking to prevent invitations from being sent to randomly generated or known spam addresses.
* User feedback and reporting: Allow your users to report abuse. This helps you to quickly identify and address potential weaknesses in the system.
* Customizable email templates: Give users the ability to personalize the invitation emails, but make sure the text meets certain guidelines and cannot be misused.
* Monitoring and analysis: Actively monitor the use of the invitation system to detect anomalies or abuse patterns at an early stage. Analyze the data regularly to adjust the security measures accordingly.


Veraltete (deprecated) Konsolenklassen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. todo: #06
.. todo: #HR: prüfen

Folgende Konsolenklassen (console classes) aus dem internen Namensraum sind als veraltet markiert und werden im nächsten Major Release entfernt.

Prüfen Sie Ihren Code, um festzustellen, ob und wo Sie die als veraltet markierten Klassen verwenden.

Nachdem Sie gegebenenfalls Ihren Code aktualisiert haben, um die veralteten Klassen zu ersetzen, führen Sie Tests durch, um sicherzustellen, dass Ihre Anwendungen weiterhin wie erwartet funktionieren.

* :code:`Executor`
* :code:`ExecutorInterface`
* :code:`CommandsProvider`
* :code:`CommandsProviderInterface`

.. todo: DK: not documented, so not to be mentioned; : deprecated as of 7.1, removed as of 8.0
F       olgende zuvor als veraltet (deprecated) markierten Funktionen haben wir entfernt.
        * getContainer()
        * dispatchEvent() methods in Core classes	Dev
.. todo: Zur Info: Global function \makeReadable(); DK: not to be mentioned in docu
.. todo: Zur Info: TemplateFileResolverInterface is redundant and will be removed in the next major version, template extension resolving is already performed in TemplateRenderer
        DK: it's a leftover: will be reomoved, not to be mentioned; Smarty Überbleibsel, DK checks

Komponenten
-----------

Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält die folgenden Komponenten (aktualisierte Versionen):

.. todo: #HR:  710: Infos abwarten

* `OXID eShop CE 7.0.3 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.3/CHANGELOG-7.0.md#v703---2024-02-20>`_
* `OXID eShop PE 7.0.0 <https://github.com/OXID-eSales/oxideshop_pe/blob/v7.0.0/CHANGELOG.md>`_
* `OXID eShop EE 7.0.1 <https://github.com/OXID-eSales/oxideshop_ee/blob/v7.0.1/CHANGELOG.md>`_
* `Apex theme 1.2.0 <https://github.com/OXID-eSales/apex-theme/blob/v1.2.0/CHANGELOG.md>`_
* `Twig admin theme 2.2.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.2.0/CHANGELOG.md>`_
* `Twig component CE 2.2.0 <https://github.com/OXID-eSales/twig-component/blob/v2.2.0/CHANGELOG.md>`_
* `Twig component PE 2.2.0 <https://github.com/OXID-eSales/twig-component-pe/blob/v2.2.0/CHANGELOG.md>`_
* `Twig component EE 2.2.0 <https://github.com/OXID-eSales/twig-component-ee/blob/v2.2.0/CHANGELOG.md>`_

* `OXID eShop composer plugin 7.1.1 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.1.1/CHANGELOG.md>`_
* `OXID eShop Views Generator 2.1.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.1.0/CHANGELOG.md>`_
* `OXID eShop demo data installer 3.1.1 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.1.1/CHANGELOG.md>`_
* `OXID eShop demo data CE/PE/EE 8.0.0 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.0/CHANGELOG.md>`_
* `OXID eShop demo data EE 8.0.1 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.1/CHANGELOG.md>`_
* `OXID eShop doctrine migration integration 5.1.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.1.0/CHANGELOG.md>`_
* `OXID eShop facts 4.1.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.1.0/CHANGELOG.md>`_
* `Unified Namespace Generator 4.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v4.1.0/CHANGELOG.md>`_

* `GDPR Opt-In 3.0.1 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v3.0.1/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 2.0.2 <https://github.com/OXID-eSales/usercentrics/blob/v2.0.2/CHANGELOG.md>`_
* `Visual CMS 4.0.2 <https://github.com/OXID-eSales/visual_cms_module/blob/v4.0.2/CHANGELOG-4.0.md>`_ (PE/EE)
* `WYSIWYG Editor + Media Library 3.0.2 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v3.0.2/CHANGELOG.md>`_
* `Makaira 2.1.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.2/CHANGELOG.md>`_


Korrekturen
-----------

Die Korrekturen finden Sie im `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.1.x/CHANGELOG-7.1.md>`_.

.. todo: #08 https://github.com/OXID-eSales/oxideshop_ce/pull/918
.. todo: #09 Can't use dot character for template file names
.. todo: #10 #HR: https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.1.x/CHANGELOG-7.1.md#changed


Installation
------------

Zum Installieren oder Aktualisieren folgen Sie den Anleitungen im Abschnitt *Installation*:

:doc:`Neu-Installation <../../installation/neu-installation/neu-installation>`  |br|
:doc:`Minor-Update installieren <../../installation/update/minor-update>`

.. Intern: , Status: