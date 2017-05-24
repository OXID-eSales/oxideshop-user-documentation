Lagerverwaltung
===============
In den OXID eShop ist eine Verwaltung der Artikelbestände integriert. Dem Kunden kann so angezeigt werden, ob ein Artikel vorrätig ist. Hinsichtlich der Lieferbarkeit eines Artikels gibt es drei verschiedene Status: es sind viele, nur wenige Stück oder keine Artikel davon auf Lager. Der Status wird durch ein farbiges Symbol und einen Hinweistext in den Artikeldetails angezeigt.

Artikel mit ausreichend großer Stückzahl
----------------------------------------
Unterhalb des Preises informiert ein grünes Symbol und der Standardtext :guilabel:`Sofort lieferbar` über den ausreichenden Lagerbestand.

Artikel mit geringer Stückzahl
------------------------------
Das Symbol unterhalb des Artikelpreises wechselt seine Farbe auf orange. Der Standardtext :guilabel:`Wenige Exemplare auf Lager - schnell bestellen!` erscheint.

Artikel nicht vorhanden
-----------------------
Ist der Artikel ausverkauft, wird dies durch ein rotes Symbol und den Hinweis :guilabel:`Dieser Artikel ist nicht auf Lager und muss erst nachbestellt werden` dargestellt.

Damit Sie die Lagerverwaltung verwenden können, muss diese aktiviert sein. Gehen Sie dafür zu :menuselection:`Stammdaten --> Grundeinstellungen`, Registerkarte:guilabel:` Einstell.` Klicken Sie auf :guilabel:`Lager`, um die Einstellungen anzuzeigen.

Standardmäßig ist das Kontrollkästchen :guilabel:`Lagerverwaltung aktiv` angehakt. Bei jeder Bestellung eines Artikels wird die Stückzahl reduziert und der Lagerstatus aktualisiert. Ist die Lagerverwaltung inaktiv, wird in den Artikeldetails immer ein grünes Symbol angezeigt.

Für eine aktive Lagerverwaltung können Sie weitere Einstellungen vornehmen.

:guilabel:`Negative Lagerbestände erlauben`

Diese Einstellung ist nur relevant, wenn Sie die Artikel aus einem Fremdlager beziehen. Ist die Einstellung aktiv, werden negative Lagerbestände berechnet, wenn weitere Exemplare bestellt werden. Wenn die Einstellung nicht aktiv ist, fällt der Lagerbestand eines Artikels nie unter 0. Auch dann nicht, wenn der Artikel bereits ausverkauft ist und noch weitere Exemplare bestellt werden.

:guilabel:`Lagerbestand, ab dem den Benutzern angezeigt wird, dass nur noch wenige Artikel auf Lager sind`

Geben Sie hier eine Stückzahl ein, ab der ein geringer Lagerbestand angezeigt werden soll.

:guilabel:`Die \"Auf-Lager\"-Standardmeldung nutzen`

Ist das Kontrollkästchen aktiv, wird die Standardmeldung :guilabel:`Sofort lieferbar` verwendet. Sie wird immer dann angezeigt, wenn bei einem Artikel keine eigene Meldung für den Lagerstatus hinterlegt wurde. Für jeden Artikel kann eine von der Standardmeldung abweichende Meldung definiert werden.

:guilabel:`Die \"Nicht-auf-Lager\"-Standardmeldung nutzen`

Auch hier wird die Standardmeldung verwendet, wenn bei einem Artikel keine davon abweichende Meldung hinterlegt ist. Ist das Kontrollkästchen angehakt, wird die Standardmeldung :guilabel:`Dieser Artikel ist nicht auf Lager und muss erst nachbestellt werden` angezeigt.

Speichern Sie Ihre Einstellungen.

.. Intern: oxbaaw, Status: