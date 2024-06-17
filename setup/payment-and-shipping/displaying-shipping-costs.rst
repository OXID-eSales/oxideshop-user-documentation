Displaying shipping costs in the shopping cart overview
=======================================================

Display the shipping costs in the shopping cart overview (:ref:`oxbaka02`, item 1).

However, do this :emphasis:`only` if it is technically possible to correctly determine the shipping costs without the customer having logged into your OXID eShop.

Example: You have a flat shipping rate for all products and delivery countries. In such cases, you know the shipping costs without knowing the customer's delivery address, for example.

|procedure|

.. attention::

   **Price Indication Ordinance**

   Make sure that you do not violate the Price Indication Ordinance or other legal framework conditions.

   Therefore, make sure that you display the actual shipping costs when you use the function.

   If this is not possible before the customer has logged in to the checkout and selected a shipping method, avoid using the function and displaying the shipping costs in the shopping cart overview.

   Instead, display a link to a page with an overview of shipping costs (:ref:`oxbaka03`, item 1), for example, so that the customer can obtain information in advance. Customize the template for this. In the demo store as of OXID eShop version, a link on the product detail page directs to the :guilabel:`Payment and delivery` page, which you can edit under :menuselection:`Customer information --> CMS pages --> Payment and delivery` (:technicalname:`oxdeliveryinfo`).

   .. _oxbaka03:

   .. figure:: /media/screenshots/oxbaka03.png
      :alt: Link to the shipping costs overview
      :width: 650
      :class: with-shadow

      Fig.: Link to the shipping costs overview

1. Under :menuselection:`Shop settings --> Shipping methods`, create a standard shipping method or several shipping methods with identical shipping costs for shipping.
#. Create the shipping rules and assign the shipping methods.
#. Choose :menuselection:`Master Settings --> Core Settings`.
#. On the :guilabel:`Settings` tab, open the :guilabel:`Other Settings` section.
#. Check the :guilabel:`Calculate default Shipping costs when ser is not logged in yet` checkbox (:ref:`oxbaka01`, item 1).

   .. _oxbaka01:

   .. figure:: /media/screenshots/oxbaka01.png
      :alt: Activating display of standard shipping costs
      :width: 650
      :class: with-shadow

      Fig.: Activating display of standard shipping costs

|result|

The shipping costs are displayed (:ref:`oxbaka02`, item 1).

.. note::

   **Multiple shipping methods**

   Technically, the shipping costs of the :emphasis:`first` shipping method that is applicable according to your shipping rules are displayed.

   Because you have configured the shipping methods so that the shipping costs are always the same, it is possible that the customer chooses a different shipping method in the checkout after registration. In any case, the correct final price will be displayed as in the checkout.

.. _oxbaka02:

.. figure:: /media/screenshots/oxbaka02.png
   :alt: Displaying shipping costs in the shopping cart overview
   :width: 650
   :class: with-shadow

   Fig.: Displaying shipping costs in the shopping cart overview


.. Intern: oxbaka, Status: