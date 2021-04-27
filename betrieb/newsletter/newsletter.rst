Newsletter
==========

Newsletter stellen eine unkomplizierte und schnelle Möglichkeit dar, die Kunden des Onlineshops über aktuelle Themen zu informieren, Tipps zu geben, Aktionen anzukündigen und Artikel zu bewerben. Sie dienen damit der Kundeninformation und stellen zugleich Kundenbindung her. Kunden müssen den Newsletter abonniert haben, indem sie dies beispielsweise bei der Registrierung bestätigt oder das Newsletter-Formular ausgefüllt und abgeschickt haben. Darüber hinaus müssen die Kunden dem Versand von Newslettern an die eigene E-Mail-Adresse nochmals explizit zustimmen. Dieses Verfahren wird als Double-Opt-In bezeichnet und stellt sicher, dass kein Unbefugter jemanden für den Newsletter einträgt.

.. image:: ../../media/screenshots/oxbaie01.png
   :alt: Newsletter abonnieren
   :height: 427
   :width: 650

Benutzer, die den Newsletter abonniert haben, werden automatisch der Benutzergruppe "Newsletter-Abonnenten" zugeordnet. Sie können im Administrationsbereich unter :menuselection:`Benutzer verwalten --> Benutzergruppen` eingesehen werden. Kunden können den Newsletter abbestellen, indem sie das Newsletter-Formular ausfüllen und :guilabel:`Abmelden` wählen.

Newsletter werden in regelmäßigen oder unregelmäßigen Abständen als E-Mail an Kunden versandt. Es gibt dafür unzählige Anbieter von 
Newsletter-Diensten, cloudbasierte Newsletter-Tools oder Newsletter-Software. OXID eShop bietet die Möglichkeit, eine Liste der Newsletter-Abonnenten zu exportieren, die dann an einen externen Anbieter übergeben werden kann. Um den Export zu starten, gehen Sie im Administrationsbereich des Shops zu :menuselection:`Kundeninformation --> Newsletter`. Betätigen Sie die Schaltfläche :guilabel:`Empfänger exportieren`.

Die Datensätze werden in eine CSV-Datei geschrieben, deren Dateinamen aus :file:`Export_recipients_`, einem angehängten Datum im Format JJJJ-MM-TT und der Dateiendung :file:`.csv` besteht. Die Datei enthält Anrede, Vorname, Nachname, E-Mail-Adresse, Opt-in-Status und zugeordnete Benutzergruppen für jeden Abonnenten. Opt-in-Status kann abonniert, nicht abonniert oder nicht bestätigt sein. Die Datei kann direkt im verwendeten Browser geöffnet oder lokal auf dem Rechner gespeichert werden.


.. Intern: oxbaie, Status: