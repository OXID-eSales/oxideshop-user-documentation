Creating free items as a discount
=================================

In addition to the absolute and relative price discounts, the OXID eShop offers a third discount option: a free item.

If a purchase meets the conditions for the discount, the designated item is automatically added to the shopping cart as a free gift.

This allows you to create promotions for specific purchase values or quantities, enabling customers to receive free items.

When the item is added to the shopping cart as a free gift, its price is automatically set to zero, while the original price remains unchanged in the item management.

|procedure|

1. Choose :menuselection:`Shop Settings --> Discounts`.
#. Create a new discount, assign a meaningful name, and from the :guilabel:`Discount` drop-down list choose :guilabel:`itm`.
#. Choose :guilabel:`Save`.
#. On the :guilabel:`Main` tab, choose the :guilabel:`Choose product` button.
#. Drag and drop the item into the right-hand list of the assignment window, then close the window.
#. In the :guilabel:`Quantity` field, make sure that the item is added to the shopping cart at least once.
#. Optional: To make the number of free items dependent on the quantity of items purchased, activate the :guilabel:`Multiply` option.
#. Choose :guilabel:`Save`.
#. Specify where the discount should be displayed: in the item overview or detailed view or only in the shopping cart.

   Typically, you want the free item to appear in the shopping cart first.

   To implement this, under :ref:`operation/discounts/discounts:Create and manage discounts`, follow the instructions in step :ref:`Determine placement <Determine discount placement>`.

#. Make sure that the discount is active.
#. Save the settings.
#. On the :guilabel:`Products` tab, assign the products or categories for which you want to grant the discount.

|result|

The number of free items is automatically calculated in the shopping cart. The free item(s) are displayed (:ref:`oxbahi03`, item 1).

The number of free items is determined by the formula: (Purchased items / Minimum purchase quantity) × Entered quantity.

Example: A customer buys 10 items to which the discount applies.

Minimum purchase quantity: 3
|br|
Quantity of the bonus: 1
|br|
→ Calculation: (10/3) × 1 = 3 free items

If the quantity of the bonus is 2, the number of free items doubles to 6.

.. _oxbahi03:

.. figure:: ../../media/screenshots/oxbahi03.png
   :alt: Example of an item with a free item in the shopping cart
   :width: 650
   :class: with-shadow

   Fig.: Example of an item with a free item in the shopping cart


.. Intern: oxbahq, Status: