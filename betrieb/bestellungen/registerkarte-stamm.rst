Registerkarte Stamm
===================

Auf der Registerkarte :guilabel:`Stamm` können Sie Bestellinformationen hinzufügen oder ändern.

Das betrifft Bestell- und Rechnungsnummern ebenso wie Bezahl- und Versandinformationen.

Handelt es sich bei den bestellten Artikeln um Download-Artikel, können Sie eine E-Mail mit den Downloadlinks an den Kunden senden.

.. image:: ../../media/screenshots/oxbaed01.png
   :alt: Bestellungen - Registerkarte Stamm
   :height: 334
   :width: 650

:guilabel:`IP-Adresse`
   Zeigen Sie die IP-Adresse an, von der aus der Kunde die Bestellung abgeschlossen hat.

   .. attention::

      **Datenschutz**

      Das Anzeigen der IP-Adresse kann illegal sein.

      In Deutschland verstoßen gegen die Datenschutzbestimmungen, wenn Sie die IP-Adresse eines Kunden zusammen mit dessen Bestelldaten speichern.

      In anderen Ländern hingegen, beispielsweise in den Vereinigten Staaten, dürfen Sie IP-Adressen erfassen.

      Aktivieren Sie die Funktion nur, wenn Sie sicher sind, nicht gegen Gesetze zu verstoßen.

      Sie tun das unter :menuselection:`Stammdaten --> Grundeinstellungen` auf der Registerkarte :guilabel:`System`. Wählen Sie unter :guilabel:`Bestellungen` die Einstellung :guilabel:`IP-Adressen speichern`. :guilabel:`Dies ist u.U. ein Verstoß gegen den Datenschutz`.

      Siehe auch: `Datenschutz: Dürfen Online-Händler IP-Adressen ihrer Kunden speichern? <http://shop.trustedshops.com/de/rechtstipps/datenschutz-duerfen-online-haendler-ip-adressen-ihrer-kunden-speichern>`_ (Trusted Shops)


:guilabel:`Bestellnr.`
   Der Shop vergibt bei jeder Bestellung eine fortlaufende Bestellnummer. Ändern Sie sie, wenn der Shop ab der nächsten Bestellung mit der darauffolgenden Bestellnummer weiterzählen soll.

:guilabel:`Rechnungsnr.`
   Tragen Sie Ihre benutzerdefinierte Rechnungsnummer ein.

   Wenn Sie nichts eintragen, ist die Bestellnummer auch gleichzeitig die Rechnungsnummer.

:guilabel:`Rabatt` ... :guilabel:`(EUR)`
   Wurde für die bestellten Artikel ein Rabatt wirksam, wird dieser hier angezeigt.

   Sie können einen Rabatt nachträglich ändert oder gewähren. Tragen Sie den Wert in das Eingabefeld ein und speichern Sie die Änderungen. Der Gesamtpreis der Bestellung wird neu berechnet.

:guilabel:`Bezahlinformationen`
   Dokumentieren Sie den Zahlungseingang zur Bestellung.

   Dazu setzen Sie im Feld :guilabel:`Bezahlt am` das Bezahldatum im Format :code:`JJJJ-MM-TT HH:MM:SS`.

   Nach dem Speichern erscheint eine neue Zeile mit dem Hinweis :guilabel:`Bestellung wurde bezahlt` und der Datums- und Zeitangabe.

   Soll für die Bestellungen das aktuelle Datum verwendet werden, genügt ein Klick auf den gleichnamigen Link und es wird in das Eingabefeld eingetragen.

:guilabel:`Bezahlung mit`
   In der Dropdown-Liste ist ausgewählt, mit welcher Zahlungsart der Kunde die Bestellung abgeschlossen hat.

   Falls notwendig, können Sie dieser Bestellung eine andere aktive Zahlungsart zuordnen. Wählen Sie dazu eine andere Zahlungsart aus der Dropdown-Liste aus und speichern Sie die Änderung.

:guilabel:`Versandinformationen`
   Bei der Bestellung hat der Kunde eine Versandart gewählt, die zusammen mit den Versandkosten angezeigt wird.

   Sie können diese Angaben bei Bedarf ändern.

   Die Schaltflächen :guilabel:`Jetzt versenden` und :guilabel:`Versanddatum zurücksetzen`, ebenso wie das Kontrollkästchen :guilabel:`E-Mail schicken?` erfüllen die gleiche Funktion, wie auf der Registerkarte :guilabel:`Übersicht`. Das Versanddatum kann gesetzt und der Kunde per E-Mail über den Versand der Ware informiert werden.

   Es wird die Zeile :guilabel:`Versandt am` mit der Datums- und Zeitangabe vervollständigt.

.. _tracking-url-orders:

:guilabel:`Tracking-Code`
   Tragen Sie die Paket-ID der Bestellung (je nach Versanddienstleister Tracking Code, Paketscheinnummer, Paketreferenz usw.) ein.

   Der Tracking-Link, bestehend aus der Tracking-URL und der Paket-ID der Bestellung, wird generiert und Ihrem Kunden zur Sendungsverfolgung mit der E-Mail zugeschickt, mit der ihm der Versand der Ware mitgeteilt wird.

   In der Bestellhistorie des Kunden im Frontend wird der Tracking-Link ebenfalls angezeigt.

   Die Tracking-URL können Sie für jede einzelne Versandart separat definieren.
   |br|
   Wie das geht, finden Sie unter :ref:`Tracking-URL <tracking-url-shipping-method>`.

   Wenn Sie für eine Versandart keine spezielle Tracking-URL festgelegt haben, verwendet das System die Tracking-URL, die Sie im Administrationsbereich unter :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Weitere Einstellungen` festgelegt haben.


   .. todo: #tbd 7.x: create Ref zu Doku, sobald angelegt für :menuselection:`Stammdaten --> Grundeinstellungen --> Einstell. --> Weitere Einstellungen` / :menuselection:`Master Settings --> Core Settings --> Settings --> Other Settings`, :guilabel:`Standard shipping provider tracking URL`



:guilabel:`Bestellte Downloadlinks`
   Bieten Sie mit Download-Artikeln beispielsweise Software, Fotos, Musikdateien oder Dokumentvorlagen an.

   Legt der Kunde einen Download-Artikel in den Warenkorb, erwirbt er alle dazugehörigen Dateien, die er sich im Shop herunterladen kann.

   Um eine E-Mail mit den Download-Links an den Kunden zu senden, wählen Sie die Schaltfläche :guilabel:`Senden`.

.. Intern: oxbaed, Status:, F1: order_main.html