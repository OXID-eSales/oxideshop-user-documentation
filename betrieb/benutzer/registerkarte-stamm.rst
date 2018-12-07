Registerkarte Stamm
===================
Die Registerkarte :guilabel:`Stamm` enthält die wichtigsten Informationen zum Benutzer. Sie werden gespeichert, sobald der Benutzer das erste Mal im Shop einkauft, sich im Shop registriert oder den Newsletter abonniert. Dabei müssen nicht alle Felder ausgefüllt worden sein, denn nur die E-Mail-Adresse, der Vor- und Nachname, die Anschrift und das Land sind standardmäßig Pflichtfelder bei der Registrierung. Beim Abonnieren des Newsletters ist allein die E-Mail-Adresse zwingend erforderlich.

Benutzer können auch mit der Funktion :guilabel:`Neuer Benutzer` angelegt werden. Dabei werden auf der Registerkarte :guilabel:`Stamm` alle relevanten Daten des Benutzers eingetragen. Ohne E-Mail-Adresse können die Benutzerdaten nicht gespeichert werden.

.. image:: ../../media/screenshots/oxbadr01.png
   :alt: 
   :class: with-shadow
   :height: 335
   :width: 650

:guilabel:`Aktiv` |br|
Ein aktiviertes Kontrollkästchen bedeutet, dass sich der Benutzer abhängig von seinen Rechten am Shop anmelden kann. Ein automatisch erstellter Benutzer ist sofort aktiv.

:guilabel:`Rechte` |br|
Bei den Rechten wird zwischen \"Kunde\" und \"Admin\" unterschieden. Die Auswahl erfolgt über eine Dropdown-Liste. Alle Benutzer, die im Shop einkaufen, sich registrieren oder den Newsletter abonnieren, haben das Recht \"Kunde\". Der Administrator, der während der Installation erstellt wurde, hat das Recht \"Admin\". Weitere Benutzer mit diesem Recht können nur im Administrationsbereich unter :menuselection:`Benutzer verwalten --> Benutzer` erstellt werden.

In der Enterprise Edition können auch Administratoren definiert werden, die nur Zugriff auf einen bestimmten Shop haben. Die Dropdown-Liste enthält entsprechende Einträge, sobald es mehr als den Hauptshop gibt. Benutzer mit dem Recht \"Admin\" können hingegen mit allen Shops arbeiten.

:guilabel:`E-Mail/Login` |br|
Das Feld enthält die E-Mail-Adresse des Benutzers. Bei einem manuell erstellten Benutzer kann ein beliebiges Login vergeben werden.

:guilabel:`Kundennr.` |br|
Der Shop vergibt beim Erstellen eines Benutzers eine fortlaufende Kundennummer. Standardmäßig wird mit der 1 begonnen. Ändern Sie die Kundennummer des zuletzt erstellten Benutzers, wird ab dessen Kundennummer weitergezählt. Im Feld :guilabel:`Kundennr.` sind ausschließlich numerische Werte erlaubt. Davon abweichende Eingaben führen dazu, dass die Kundennummer auf Null gesetzt wird.

:guilabel:`Anrede` |br|
Anrede des Benutzers, die während des Einkaufs oder der Registrierung gewählt wurde. Beim manuellen Anlegen oder beim Ändern des Benutzers ist die Auswahl von \"Herr\" oder \"Frau\" aus einer Dropdown-Liste möglich.

:guilabel:`Vor-/Nachname` |br|
Die beiden Felder nehmen den Vor- und Nachnamen des Benutzers auf.

:guilabel:`Firma`
Ein Geschäftskunde kann beim Einkauf oder bei der Registrierung den Namen seiner Firma angeben. Auch beim manuellen Anlegen kann der Firmenname des Benutzers eingetragen werden.

:guilabel:`Str./Hausnr.` |br|
Diese Felder nehmen den Straßennamen und die Hausnummer der Anschrift des Benutzers auf. Die Anschriftsdaten sind Teil der Rechnungs- und Liederadresse, sofern beim Kauf keine abweichende Lieferadresse verwendet wird.

:guilabel:`PLZ, Ort` |br|
Felder für die Postleitzahl und die Ortsbezeichnung der Anschrift des Benutzers.

:guilabel:`Umsatzsteuer-Identnummer` |br|
Ein Geschäftskunde kann beim Einkauf oder bei der Registrierung die Umsatzsteuer-Identnummer (USt-ID) seiner Firma angeben. Auch beim manuellen Anlegen kann die Umsatzsteuer-Identnummer eingetragen werden.

:guilabel:`zus. Info` |br|
Feld, um eine Zusatzinformation zu speichern.

:guilabel:`Bundesland` |br|
Im Feld kann das Bundesland eingetragen werden, in dem der Benutzer lebt.

:guilabel:`Land` |br|
Auch das Land, in dem der Benutzer lebt, ist aus einer Dropdown-Liste auswählbar. Diese Information beeinflusst, welche Zahlungs- und Versandarten der Benutzer im Bestellprozess nutzen kann.

:guilabel:`Telefon` |br|
Telefonnummer des Benutzers.

:guilabel:`Fax` |br|
Faxnummer des Benutzers.

:guilabel:`Geburtsdatum` |br|
Geburtsdatum des Benutzers.

:guilabel:`Hat ein Passwort?` |br|
Diese Frage wird nur bei einem bereits angelegten Benutzer angezeigt. \"Ja\" oder \"Nein\" beantwortet, ob ein Passwort vergeben wurde oder nicht. Ein Benutzer ohne Passwort hat im Shop eingekauft, ohne sich zu registrieren und damit ohne ein Kundenkonto zu eröffnen.

:guilabel:`Neues Passwort` |br|
Beim Anlegen oder Bearbeiten eines Benutzers muss ein Passwort vergeben werden, mit dem dieser sich am Shop anmelden kann. Ohne Passwort ist keine Anmeldung möglich. Beim Speichern eines Benutzers ohne Passwort wird darauf nicht explizit hingewiesen.

:guilabel:`Benutzergruppen zuordnen` |br|
Benutzer können verschiedenen Benutzergruppen angehören. Die Zusammenfassung von Benutzern zu Benutzergruppen ermöglicht eine komfortable Zuordnung von Bedingungen, wie Zahlungs- und Versandarten, und Aktionen, wie Rabatte und Gutscheine.

Die Schaltfläche :guilabel:`Benutzergruppen zuordnen` öffnet ein neues Fenster. In diesem Zuordnungsfenster werden in der linken Liste alle Benutzergruppen angezeigt. Diese können per Drag \& Drop in die rechte Liste verschoben werden. Eine Mehrfachauswahl ist bei gedrückter Strg-Taste möglich. Damit ist die Zuordnung abgeschlossen.

.. seealso:: :doc:`Benutzergruppen <../benutzergruppen/benutzergruppen>`

.. Intern: oxbadr, Status:, F1: user_main.html