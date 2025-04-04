Defining individual shipping costs for specific products
========================================================

Most online shops offer a wide product range. Some items incur significantly higher shipping costs—for example, if they must be shipped as bulky goods or under special conditions.

Configure shipping so that a surcharge is added to the standard shipping costs whenever specific products are placed in the shopping cart. You can achieve this by creating shipping cost rules and assigning them to the relevant products.

During the checkout process, the customer selects a shipping method. The shop processes all shipping cost rules assigned to this method. It checks whether the defined condition (assigned products) applies to the items in the cart. The rule will only be applied to the shipping calculation if the condition is met.

Procedure
---------

1. Define the products as a condition in the shipping cost rule.

   a. Go to :menuselection:`Shop Settings --> Shipping Cost Rules`.
   #. Select the relevant rule from the list of shipping cost rules.
   #. In the :guilabel:`Products` tab, click :guilabel:`Assign Products`.
   #. Use drag & drop to move the products into the right-hand list of the assignment window.
   #. Close the assignment window.
   #. In the :guilabel:`Main` tab, define a shipping surcharge.
   #. Complete the remaining settings of the shipping cost rule.
   #. Save your changes.

2. Assign the shipping cost rule to a shipping method.

   .. hint::
      You must assign at least one shipping cost rule and one payment method to the shipping method.
      For consistency, assign countries as well. If no countries are assigned, the shipping method will apply globally.

   a. Go to :menuselection:`Shop Settings --> Shipping Methods`.
   #. Select the desired shipping method from the list.
   #. In the :guilabel:`Main` tab, click :guilabel:`Assign Shipping Cost Rules`.
   #. Use drag & drop to move the shipping cost rule into the right-hand list.
   #. Close the assignment window.

Example
-------

Proceed in the same way as with product categories.

For details, see :ref:`setup/payment-and-shipping/shipping-costs-for-products-from-specific-categories:Example: Categories and shipping cost rules in the demo shop`.

.. seealso::
   :doc:`Shipping Cost Rules – Products tab <../shipping-cost-rules/products-tab>` |
   :doc:`Shipping Methods – Main tab <../shipping-methods/main-tab>`

.. Intern: oxbafy, Status: