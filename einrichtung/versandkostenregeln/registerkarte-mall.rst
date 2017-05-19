Registerkarte Mall
******************
Die Registerkarte :guilabel:`Mall` ist bei Versandkostenregeln nur in der OXID eShop Enterprise Edition vorhanden.

Versandkostenregeln können beim Erstellen von Shops an diese vererbt werden. Wird die Option :guilabel:`Dieser Shop erbt alle Artikel und `:guilabel:`:guilabel:`Einstellungen` vom Elternshop` gewählt, enthält ein neuer Shop auch alle Versandkostenregeln des Elternshops. Die vererbten Versandkostenregeln sind nicht änderbar und behalten auch die ursprünglichen Verknüpfungen mit Ländern, Kategorien, Artikeln, Benutzergruppen oder Benutzern bei.

Auf der Registerkarte :guilabel:`Mall` werden die Verknüpfungen der Versandkostenregel zu Subshops und Supershops verwaltet. Multishops übernehmen keine Versandkostenregeln aus anderen Shops.

.. image:: ../../media/screenshots-de/oxaadn01.png
   :alt: Versandkostenregeln - Registerkarte Mall
   :height: 306
   :width: 650

Es ist möglich, die Vererbung aller Versandkostenregeln für einen Shop rückgängig zu machen. Dazu muss in der Registerkarte :guilabel:`Mall` des Subshops oder Supershops unter :menuselection:`Stammdaten --> Grundeinstellungen` das Häkchen von :guilabel:`Alle Lieferinformationen vom Elternshop erben` entfernt werden. Dadurch wird auch die Verknüpfung zu den geerbten Versandarten aufgehoben.

:guilabel:`Verknüpft mit folg. Subshops`

Die Verknüpfung einer Versandkostenregel mit Subshops und Supershops kann hinzugefügt oder entfernt werden, indem das entsprechende Kontrollkästchen angehakt wird oder nicht. Bei nicht aktiviertem Kontrollkästchen ist die Versandkostenregel im Elternshop vorhanden, aber nicht im jeweiligen Subshop oder Supershop.

Über die Links :guilabel:`Alle auswählen` und :guilabel:`Keine auswählen` auf der rechten Seite des Fensters können alle Shops verknüpft oder alle Verknüpfungen zu den Shops entfernt werden. Vorgenommene Änderungen müssen gespeichert werden und sind für die Subshops oder Supershops sofort wirksam.

.. Intern: oxaadn, Status:, F1: delivery_mall.html