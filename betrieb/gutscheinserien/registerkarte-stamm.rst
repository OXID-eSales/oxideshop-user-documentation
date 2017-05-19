Registerkarte Stamm
*******************
Gutscheinserien fassen eine Anzahl von Gutscheinen zusammen und werden auf der Registerkarte :guilabel:`Stamm` erstellt und bearbeitet. Hier wird die Gültigkeit einer Gutscheinserie festgelegt, die gleichzeitig auch die Gültigkeit der zur Serie gehörenden Gutscheine bestimmt. Ein absoluter oder relativer Rabatt stellt den eigentlichen Wert eines Gutscheins da, der im Warenkorb angerechnet wird. Die Gutscheine einer Serie können mit einem fixen oder einem zufälligen Gutscheincode generiert und als Datei im CSV-Format exportiert werden. Eine kleine Übersicht zeigt die Anzahl aller generierten, der eingelösten und noch unbenutzten Gutscheine.

.. image:: ../../media/screenshots-de/oxaahs01.png
   :alt: Gutscheinserien - Registerkarte Stamm
   :height: 314
   :width: 650

Die Zuordnung von Benutzergruppen, Kategorien und/oder Artikeln erfolgt auf einer weiteren Registerkarte.

:guilabel:`Name`

Name der Gutscheinserie. Dieser wird ausschließlich in der Liste der Gutscheinserien angezeigt und ist dort suchbar.

:guilabel:`Beschreibung`

Mit einer kurzen Beschreibung können detailliertere Informationen zu einer Gutscheinserie hinterlegt werden

:guilabel:`Gültig von`

Damit Gutscheine nur in einer zeitlich begrenzten Marketingaktion, wie beispielsweise Sommerschlussverkauf, Weihnachtsgeschäft oder Mondscheinaktion, einsetzbar sind, kann für die Gutscheinserie ein entsprechender Zeitraum definiert werden. Dieser Zeitraum gilt auch für die einzelnen Gutscheine. Geben Sie hier den Beginn der Gültigkeit im Format JJJJ-MM-TT HH:MM:SS an. Ohne Anfangszeitpunkt ist die Gutscheinserie bis zu einem gesetzten Endezeitpunkt oder unbegrenzt gültig.

:guilabel:`Gültig bis`

Endezeitpunkt der Gutscheinserie im Format JJJJ-MM-TT HH:MM:SS. Ohne Endezeitpunkt ist die Gutscheinserie ab einem gesetzten Anfangszeitpunkt oder unbegrenzt gültig.

:guilabel:`Rabatt`

Definieren Sie hier den Gutscheinwert, der beim Einlösen des Gutscheins im Warenkorb gewährt werden soll. Dieser kann prozentual oder absolut angegeben werden. Mit der Auswahlliste hinter dem Eingabefeld wird die Art des Gutscheinwertes ausgewählt.

:guilabel:`abs`: Der Gutscheinwert ist absolut, beispielsweise 10 €.

:guilabel:`%`: Der Gutscheinwert ist prozentual, beispielsweise 10 Prozent vom Einkaufswert.

.. hint:: Wenn mehrere Gutscheine für eine Bestellung verwendet werden, vervielfältigt sich der Gutscheinwert eventuell in Abhängigkeit von den weiteren Einstellungen.

:guilabel:`Gültig ab Einkaufswert`

Ein Gutschein dieser Serie wird vom Shop erst akzeptiert, wenn ein hier definierter Einkaufswert erreicht wurde. Ohne eine Vorgabe ist es nicht relevant, welchen Einkaufswert die Artikel im Warenkorb haben.

:guilabel:`Gültig mit gleicher Serie`

Legen Sie fest, ob Ihre Kunden mehrere Gutscheine der selben Gutscheinserie bei einer Bestellung verwenden dürfen. Sind mehrere Gutscheine für eine Bestellung möglich, können diese nur eingelöst werden, solange der Gesamtbetrag der Bestellung größer 0,00 € ist. Wenn Sie :guilabel:`Nein` wählen, kann nur ein Gutschein dieser Serie pro Bestellung eingelöst werden.

:guilabel:`Gültig mit anderer Serie`

Mit dieser Option können Sie einstellen, ob Kunden Gutscheine verschiedener Gutscheinserien bei einer Bestellung kombinieren dürfen. Ist das Optionsfeld :guilabel:`Nein` aktiviert, können Gutscheine dieser Serie nicht mit Gutscheinen anderer Serien kombiniert werden. Wurde :guilabel:`Ja` ausgewählt, muss diese\Option auch bei den zu kombinierenden Gutscheinserien auf :guilabel:`Ja` gesetzt sein.

:guilabel:`Gültig mit gleicher Serie bei einer anderen Bestellung`

Soll ein Kunde Gutscheine dieser Gutscheinserie bei mehreren Bestellungen verwenden können, muss diese Option auf :guilabel:`Ja` stehen. Gutscheine dieser Serie können nur bei einer Bestellung eingelöst werden, wenn die Option auf :guilabel:`Nein` gesetzt ist.

:guilabel:`Nur einmalig berechnen (gültig nur bei zugewiesenen Gutscheinen)`

Diese Einstellung hat nur Auswirkung auf Gutscheine einer Gutscheinserie, denen Artikel und/oder Kategorien zugeordnet sind. Ist das Kontrollkästchen angehakt, wird der Gutschein für nur einen der Gutscheinserie zugewiesenen Artikel eingelöst, auch wenn mehrere solcher Artikel im Warenkorb liegen. Ist diese Einstellung nicht aktiv, wird der Gutschein auf jeden dieser Artikel angerechnet.

:guilabel:`Gutscheine - Anzahl`

Anzahl der erzeugten, zur Gutscheinserie gehörenden Gutscheine.

:guilabel:`Gutscheine - Verfügbar`

Anzahl der Gutscheine dieser Gutscheinserie, die noch nicht verbraucht wurden.

:guilabel:`Gutscheine - Benutzt`

Anzahl der eingelösten Gutscheine dieser Gutscheinserie.

:guilabel:`Neue Gutscheine anlegen (optional)`

Zu einer Gutscheinserie können beliebig viele Gutscheine erstellt werden. Es ist möglich, diese einmalig oder bei Bedarf auch mehrfach zu generieren. Beim Exportieren wird eine Datei, welche die generierten Gutscheinnummern enthält, in eine Datei geschrieben und im Verzeichnis :file:`/export` des Shops gespeichert.

:guilabel:`Zufallsnummern erzeugen`

Wurde diese Option aktiviert, werden Gutscheine mit einem 32-stelligen alphanumerischen Gutscheincode generiert. Beispiel für zufälligen Gutscheincode: f2119e0585d1c5514f6729c703f14bf0

:guilabel:`Gutscheinnummer`

Aktivieren Sie diese Option, wenn Sie Gutscheine mit identischem Gutscheincode anlegen wollen. Alle generierten Gutscheine erhalten den Gutscheincode, den Sie hier eingetragen haben. Beispiel für gleichen Gutscheincode: SALE2016

:guilabel:`Anzahl`

Legen Sie hier fest, wie viel Gutscheine der Gutscheinserie generiert werden sollen.

:guilabel:`Generieren`

Zum Erzeugen der Gutscheine betätigen Sie diese Schaltfläche. Es können bei Bedarf auch neue Gutscheine zur Gutscheinserie hinzugefügt werden. Die Gutscheine mit ihrem Gutscheincode werden in der Tabelle oxvoucher der Datenbank gespeichert.

:guilabel:`Export`

Die Schaltfläche ermöglicht es, die generierten Gutscheine mit den Gutscheincodes in eine Datei zu schreiben. Das wird vor allem dann notwendig, wenn Gutscheine mit zufälligen Gutscheincodes generiert wurden, da diese nicht im Administrationsbereich angezeigt werden. Die Datei listet alle, auch die bereits eingelösten Gutscheine auf. Sie wird im Verzeichnis :file:`/export` des Shops gespeichert und kann mit einem beliebigen Texteditor oder Tabellenkalkulationsprogramm geöffnet werden.

.. Intern: oxaahs, Status:, F1: voucherserie_main.html