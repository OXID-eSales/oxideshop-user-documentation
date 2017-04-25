E-Mails
*******
Der OXID eShop versendet verschiedene E-Mails. Wenn Kunden bestellen, wird ihnen eine E-Mail zugeschickt, in der die Bestellung nochmals aufgeführt wird. Kunden erhalten auch eine E-Mail, wenn sie sich für Ihren OXID eShop registrieren. Sie als Shopbetreiber können Newsletter versenden, um Ihre Kunden über Neuigkeiten zu informieren.

Damit der Versand von E-Mails richtig funktioniert, müssen die SMTP-Daten korrekt eingetragen und die Mailadressen eingerichtet sein. Die dafür notwendigen Einstellungen finden Sie auf der Registerkarte :guilabel:`Stamm` unter :menuselection:`Stammdaten --> Grundeinstellungen`.

Der E-Mail-Versand erfolgt in der Regel über einen separaten Mailserver. Haben Sie in Ihrer Firma einen solchen Server, über den auch der Shop seine Mails verschicken soll, benötigen Sie die Zugangsdaten dieses Servers. Tragen Sie die Zugangsdaten in die Eingabefelder :guilabel:`SMTP-Server`, :guilabel:`SMTP-Benutzer` und :guilabel:`SMTP-Passwort` ein. Bei einem Hosting-Paket erhalten Sie die SMTP-Daten von ihrem OXID Hosting Partner oder Internet Service Provider (ISP). Häufig erfolgt dabei der Mailversand per PHP direkt über den Server, auf dem Ihr Shop installiert ist. Für den SMTP-Server wird dann der Eintrag \"localhost\" verwendet.

Definieren Sie nun die E-Mail-Adressen, an die der Shop senden soll. Diese Mailadressen müssen auf Ihrem Mailserver oder in der Mailkonfiguration Ihres Hosting-Paketes eingerichtet sein.

:guilabel:`E-Mail-Adresse für Infos`

Verwenden Kunden das Kontaktformular und schicken ihre Nachricht ab, geht eine Mail an die hier angegebene Mailadresse. Geeignete Mailadressen wären beispielsweise info@ihreshopurl.de oder kontakt@ihreshopurl.de.

:guilabel:`E-Mail-Adresse für Antworten`

Bestellt ein Kunde in Ihrem Shop, erhält er eine E-Mail, in der die Bestellung nochmals zusammengefasst ist. Es kann vorkommen, dass der Kunde auf diese E-Mail antwortet, weil er beispielsweise eine Frage oder eine Bemerkung zu seiner Bestellung hat. Die Antwort des Kunden wird an die hier eingetragene Mailadresse verschickt.

:guilabel:`E-Mail-Adresse für Bestellungen`

Bestellt ein Kunde in Ihrem Shop, wird auch an den Shopbetreiber eine E-Mail verschickt. Er erhält die Nachricht über die Bestellung im Shop an die hier hinterlegte Mailadresse.

Der Shop versendet eine Reihe E-Mails an den Kunden. Außer der Bestellbestätigung sind das Mails zur Bestätigung einer Registrierung, zur Passwortänderung und zur Information, dass die Bestellung versandt wurde. Für diese Mails kann eine individuelle Betreffzeile festgelegt werden. Der Betreff fasst den Inhalt der E-Mail kurz zusammen. Falls Ihr Shop in verschiedene Länder liefern soll, lässt sich die Betreffzeile auch in mehreren Sprachen abfassen. Zwischen den verfügbaren Sprachen kann mit einer Auswahlliste gewechselt werden.

:guilabel:`E-Mail-Betreff bei Bestellung`

Betreffzeile der E-Mail, welche Kunden erhalten, wenn sie in Ihrem Shop bestellen.

:guilabel:`E-Mail-Betreff bei Registrierung`

Betreffzeile der E-Mail, welche Kunden erhalten, wenn sie sich in Ihrem Shop registrieren.

:guilabel:`E-Mail-Betreff \"Passwort vergessen?\"`

Hat der Kunde sein Passwort vergessen, kann er sich mit der Funktion \"Passwort vergessen?\", eine E-Mail zur Passwortänderung zuschicken lassen. Legen Sie hier den Betreff dieser E-Mail fest.

:guilabel:`E-Mail-Betreff \"Jetzt versendet\"`

Sobald die Ware an den Kunden verschickt wird, kann die Bestellung im Administrationsbereich als versendet markiert werden. Optional kann der Kunde darüber per E-Mail informiert werden. Die Betreffzeile für diese E-Mail wird hier definiert.

Klicken Sie auf :guilabel:`Speichern`. Die E-Mails werden jetzt mit einer individuellen Betreffzeile, aber einem Standardtext verschickt. Wie der Standardtext dieser E-Mails angepasst wird, erfahren Sie im Abschnitt \"CMS\".