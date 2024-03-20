.. _rdfa-zahlungsarten:

Registerkarte RDFa
==================

.. note::
   Die folgende Funktion lässt sich aus technischen Gründen im Moment nicht ausführen.

Legen Sie fest, welche RDFa-Daten für jede Zahlungsart Ihres OXID eShops eingebettet werden soll.

|background|

OXID eShop stellt Informationen gut aufbereitet für Suchmaschinen, Portale und andere Systeme bereit. Diese können beispielsweise als so genannte Rich Snippets -- ausführliche Informationen zu einem Suchergebnis -- dargestellt werden. Die Aufbereitung der Daten erfolgt auf Basis des Resource Description Framework (RDFa) und der für den E-Commerce optimierten Beschreibungssprache GoodReleations.

Auf der Registerkarte :guilabel:`RDFa` wird eine logische Verknüpfung der Zahlungsart mit den in GoodReleations vordefinierten Werten für Zahlung hergestellt.

Weitere Informationen zum Einbetten von RDFa-Daten auch Ihrer :emphasis:`Versandarten` Sie unter :menuselection:`Shopeinstellungen --> Versandarten`, :ref:`Registerkarte RDFa <rdfa-versandarten>`.

|prerequisites|

* Damit der Shop die RDFa-Integration verwenden kann, haben Sie die Funktion unter :menuselection:`Stammdaten --> Grundeinstellungen --> RDFa` aktiviert und konfiguriert.

|procedure|

Tun Sie auf der Registerkarte :guilabel:`RDFa` für jede Zahlungsart, die Sie konfiguriert haben, Folgendes:

1. Markieren Sie die Zahlungsart, die Sie im RDFa-Format einbetten wollen (:ref:`oxdale01`, Pos. 1).
2. Markieren Sie die entsprechende Zahlungsart, die GoodRelations zum Einbetten anbietet (:ref:`oxdale01`, Pos. 2).
3. Speichern Sie Ihre Einstellungen (:ref:`oxdale01`, Pos. 3).

.. _oxdale01:

.. figure:: ../../media/screenshots/oxbadc01.png
   :alt: Zahlungsarten-Informationen einbetten
   :width: 650
   :class: with-shadow

   Abb.: Zahlungsarten-Informationen einbetten


.. Intern: oxbadc, Status:, F1: payment_rdfa.html

.. ToDo: #tbd 7.x: #SB: Gibts Goodrelations noch?; Vasyl gefixed,Test steht aus, SB prüft (Wirkungsweise/Bug klären (geht es automatisch?) und in EN nachziehen, Bild mit HTML-Resulat ergänzen: typeof="gr:PaymentMethod)


