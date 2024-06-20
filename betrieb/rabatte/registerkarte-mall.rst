Registerkarte Mall: Einzelne Rabatte in Subshops verwenden
==========================================================

Konfigurieren Sie Rabatte zentral in einem Eltern-Shop und steuern Sie, welche einzelnen Rabatte Sie in welchen Subshops anwenden wollen.

Diese Funktion ist (mit der Registerkarte :guilabel:`Mall`) nur in der Enterprise Edition vorhanden.

Die Funktion ist nur für Subshops verfügbar. Multishops verwenden ohne eine derartige Verknüpfung Rabatte aus :emphasis:`allen` Shops.

Rabatte an Subshops vererben
----------------------------

|procedure|

1. Legen Sie einen Subshop an.

   Unter :menuselection:`Stammdaten --> Grundeinstellungen --> Neuen Shop anlegen`  haben Sie folgende Möglichkeiten:

   .. _Rabatte-verwalten-Schritt1:

   * Vererben Sie standardmäßig alle Artikel und Rabatte an Ihre Subshops.

     Später wählen Sie diejenigen Rabatte einzeln ab, die Sie im Subshop nicht benötigen. (Oder Sie deaktivieren alle ererbten Rabatte: Siehe :ref:`betrieb/rabatte/registerkarte-mall:Ererben von Rabatten in Subshops aufheben`.)

     Markieren Sie dazu das Kontrollkästchen :guilabel:`Dieser Shop erbt alle Artikel und Einstellungen vom Elternshop` (:ref:`oxbahl02`).

   * Verzichten Sie auf das Vererben der Artikel und Rabatte und wählen Sie in Ihrem Subshop nachträglich diejenigen Rabatte einzeln, die Sie anwenden wollen.

   .. todo: EN: Shop inherits all inheritable items (products, discounts etc) from it's parent shop.

   .. _oxbahl02:

   .. figure:: ../../media/screenshots/oxbahl02.png
      :alt: Beispiel: Subshop mit ererbten Einstellungen anlegen
      :width: 650
      :class: with-shadow

      Abb.: Beispiel: Subshop mit ererbten Einstellungen anlegen

#. Konfigurieren Sie im Eltern-Shop Rabatte, die Sie zentral für alle Subshops bereitstellen wollen.
#. Wählen Sie einen Rabatt.
#. Wählen Sie die Registerkarte :guilabel:`Mall`.

   Es wird angezeigt, in welchen Subshops der Rabatt angewendet wird (:ref:`oxbahl01`).

   .. _oxbahl01:

   .. figure:: ../../media/screenshots/oxbahl01.png
      :alt: Registerkarte Mall: Verknüpfungen zu Subshops und Supershops verwalten
      :width: 650
      :class: with-shadow

      Abb.: Registerkarte Mall: Verknüpfungen zu Subshops und Supershops verwalten

#. Je nach dem, wie Sie Ihren Subshop in :ref:`Schritt 1 <Rabatte-verwalten-Schritt1>` angelegt haben, deaktivieren Sie den Rabatt oder aktivieren ihn für die gewünschten Subshops.
#. Speichern Sie Ihre Einstellungen.
#. Optional: Legen Sie unter :menuselection:`Shopeinstellungen --> Rabatte` zusätzliche Rabatte an, die nur für den Subshop gültig sind.

Ererben von Rabatten in Subshops aufheben
-----------------------------------------

Deaktivieren Sie bei Bedarf die ererbten Rabatte.

|procedure|

#. Wechseln Sie in den Subshop.
#. Wählen Sie unter :menuselection:`Stammdaten --> Grundeinstellungen` die Registerkarte :guilabel:`Mall`.
#. Deaktivieren Sie das Kontrollkästchen :guilabel:`Alle Rabatte vom Elternshop erben`.

   .. todo: EN: Inherit all discounts from parent shop

  .. _oxbahl03:

  .. figure:: ../../media/screenshots/oxbahl03.png
     :alt: Ererbte Rabatte deaktivieren
     :width: 650
     :class: with-shadow

     Abb.: Ererbte Rabatte deaktivieren

|result|

Der Rabatt ist im Elternshop vorhanden, aber nicht im jeweiligen Subshop oder Supershop.


.. Intern: oxbahl, Status:, F1: discount_mall.html