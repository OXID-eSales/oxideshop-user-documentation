Registerkarte Rechte
====================

Verwalten Sie in der Registerkarte :guilabel:`Rechte` die Sicht- und Kaufberechtigungen für einzelne Artikel. Die Registerkarte steht ausschließlich in der OXID eShop Enterprise Edition zur Verfügung.

Ordnen Sie dem Artikel gezielt Benutzergruppen zu, die den Artikel im Shop sehen oder kaufen dürfen. Diese Funktion ist Teil der Rechte- und Rollenverwaltung der Enterprise Edition.

.. _oxbact01:

.. figure:: ../../media/screenshots/oxbact01.png
   :alt: Artikel – Registerkarte Rechte
   :width: 650
   :class: with-shadow

   Abb.: Artikel – Registerkarte Rechte

|background|

Die exklusive Sichtbarkeit bedeutet: Nur Mitglieder der zugewiesenen Benutzergruppen sehen den Artikel nach dem Login im Shop. Alle anderen Kunden und Benutzergruppen erhalten keine Anzeige dieses Artikels.

Weisen Sie einem Artikel zusätzlich exklusive Kaufrechte zu, können nur autorisierte Kunden den Artikel in den Warenkorb legen. Für alle anderen wird lediglich die Schaltfläche :guilabel:`Mehr Informationen` angezeigt – auch auf der Artikeldetailseite fehlt dann die Schaltfläche :guilabel:`In den Warenkorb legen`.

Diese Einschränkung gilt so lange, bis sich der Kunde anmeldet **und** einer berechtigten Benutzergruppe zugeordnet ist. Weitere Informationen finden Sie unter :ref:`konfiguration/rechte-und-rollen:Kaufen von Artikeln und Kategorien einschränken`.

|prerequisites|

Um eine Benutzergruppe zuzuweisen, müssen Sie sie zuvor erstellt haben.

Um neue Benutzergruppen anzulegen, wählen Sie :menuselection:`Benutzer verwalten --> Benutzergruppen`.

|procedure|

1. Öffnen Sie im Adminbereich den gewünschten Artikel unter :menuselection:`Artikel verwalten --> Artikel`.
2. Wechseln Sie zur Registerkarte :guilabel:`Rechte`.
3. Klicken Sie auf eine der folgenden Schaltflächen, je nach gewünschter Einschränkung:

   * :guilabel:`Benutzergruppen zuordnen (Ausschließlich sichtbar)`
   * :guilabel:`Benutzergruppen zuordnen (Ausschließlich kaufbar)`

4. Wählen Sie im Zuordnungsfenster die entsprechenden Benutzergruppen aus der Liste :guilabel:`Alle Benutzergruppen`.

   .. figure:: ../../media/screenshots/oxbact02.png
      :alt: Benutzergruppen zuordnen (Ausschließlich sichtbar)
      :width: 400
      :class: with-shadow

      Abb.: Benutzergruppen zuordnen (Ausschließlich sichtbar)

5. Filtern oder sortieren Sie die Gruppen bei Bedarf.
6. Ziehen Sie die gewünschten Gruppen per Drag & Drop in die rechte Liste.

   Nutzen Sie die Strg-Taste, um mehrere Gruppen gleichzeitig auszuwählen.

8. Schließen Sie das Fenster, um die Zuordnung zu speichern.

|result|

Sobald Sie die Rechte gespeichert haben, zeigt der Shop den Artikel nur noch den berechtigten Benutzergruppen an. Für nicht berechtigte Nutzer ist der Artikel weder sichtbar noch bestellbar – abhängig von der jeweiligen Einstellung.

.. seealso:: :doc:`Rechte und Rollen <../../konfiguration/rechte-und-rollen>`

.. Intern: oxbact, Status:, F1: article_rights.html

