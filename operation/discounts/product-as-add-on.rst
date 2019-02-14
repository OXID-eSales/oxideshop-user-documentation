Product as add-on
==================
In addition to the absolute and relative price reduction, OXID eShop offers a third discount option: the free product. For every purchase that meets the conditions for the discount, a special product will be added to the cart as a free add-on. This allows you to implement discount promotions for certain purchase values or quantities.

The price of the product placed into the shopping cart as an add-on will be automatically set to zero. Changing the previous price in the product management section won’t be necessary.

Defining the free product in the discount management section

* Go to :menuselection:`Shop Settings --> Discounts`.
* Select a discount from the list of discounts or create a new one.
* If the discount is new, enter a descriptive name and select :guilabel:`itm` from the :guilabel:`Discount` drop-down list.
* Click on :guilabel:`Choose product` in the :guilabel:`Main` tab.
* Drag and drop the desired product into the right-hand list of the assignment window.
* Close the assignment window.

Use the :guilabel:`Amount` field to specify how often the product will be added to the shopping cart.

* Check the :guilabel:`Multiply` box if the number of free products should depend on the number of products purchased.
* Define the remaining conditions for the discount, such as purchase quantity or value.
* Make sure that the discount is active.
* Save the settings.

The number of free add-ons will be calculated in the shopping cart. The number of discountable products will be first divided by the value of the minimum purchase quantity and then multiplied by the value entered in the :guilabel:`Amount` field.

Example: If the customer purchased 10 products on which the discount is granted, the minimum purchase quantity is 3 and the add-on quantity is 1, then the add-on will be added (10/3)*1 = 3 times to the shopping cart. If the add-on quantity is 2, the number of add-ons will increase to 6.

.. seealso:: :doc:`Discounts - Main tab <main-tab>`

.. Intern: oxbahq, Status: