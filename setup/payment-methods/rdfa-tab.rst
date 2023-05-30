.. _rdfa-payment-methods:

RDFa tab
========

.. note::
   For technical reasons, the following function cannot be executed at the moment.

Specify which RDFa data are to be embedded for each payment type of your OXID eShop.

|background|

OXID eShop provides information well prepared for search engines, portals and other systems. This information can be presented, for example, as so-called Rich Snippets -- detailed information about a search result. The data is prepared on the basis of the Resource Description Framework (RDFa) and the GoodReleations description language optimized for e-commerce.

On the :guilabel:`RDFa` tab, a logical link is created between the payment type and the values predefined in GoodReleations for payment.

For more information on embedding RDFa data also of your :emphasis:`shipping` methods, see :menuselection:`Shop Settings --> Shipping Methods`, :ref:`RDFa tab <rdfa-shipping-methods>`.

|prerequisites|

* For the store to use RDFa integration, you have enabled and configured the feature under :menuselection:`Master Settings --> Core Settings --> RDFa`.

|procedure|

On the :guilabel:`RDFa` tab, do the following for each payment type you have configured:

1. Chooose the payment type you want to embed in RDFa format (:ref:`oxdale01`, item 1).
#. Mark the corresponding payment type that GoodRelations offers for embedding (:ref:`oxdale01`, item 2).
#. Save your settings (:ref:`oxdale01`, item 3).

.. _oxdale01:

.. figure:: ../../media/screenshots/oxbadc01.png
   :alt: Embedding payment method information
   :width: 650
   :class: with-shadow

   Fig.: Embedding payment method information


.. Intern: oxbadc, Status:, F1: payment_rdfa.html
.. ToDo note line is incorrect: %s and two points