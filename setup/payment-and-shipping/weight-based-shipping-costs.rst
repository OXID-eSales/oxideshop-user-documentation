Defining weight-based shipping costs
====================================

Take the weight of the products into account when calculating shipping costs.

To do this, create shipping cost rules where the condition is based on the product weight.

During the ordering process, the customer selects a shipping method. All shipping cost rules associated with this method will be processed.

The system checks whether the defined condition (weight) is met with regard to the total weight of the products in the shopping cart. The shipping cost rule is applied only if the condition is satisfied.

Procedure
---------

1. Define the weight of a product.

   a. Go to :menuselection:`Administer Products --> Products`.
   #. Select the desired product from the product list.
   #. In the :guilabel:`Extended` tab, enter the weight.

      Once the product weight is entered, it will be displayed on the product detail page below the product price.

   #. Save your settings.

#. Define the weight as a condition in a shipping cost rule.

   a. Go to :menuselection:`Shop Settings --> Shipping Cost Rules`.
   #. Select the shipping cost rule from the list of available rules.

      In the :guilabel:`Main` tab, you'll find the dropdown list :guilabel:`Condition`.

   #. Select the condition "Weight" and enter values for :guilabel:`=\>` and :guilabel:`\<=`.
   #. Complete the remaining settings for the shipping cost rule.
   #. Save your settings.

3. Assign the shipping cost rule to a shipping method.

   a. Go to :menuselection:`Shop Settings --> Shipping Methods`.
   #. Select the desired shipping method from the list.
   #. In the :guilabel:`Main` tab, click the :guilabel:`Assign Shipping Cost Rules` button.
   #. Drag & drop the shipping cost rule into the right-hand list in the assignment window.
   #. Close the assignment window.

Example
-------

In our example, we assume a product with a weight of 2 kg.

|procedure|

1. Enter a weight of 2 kilograms for the product in the :guilabel:`Extended` tab of the product management section (:ref:`oxbafv01`).

   .. _oxbafv01:

   .. figure:: ../../media/screenshots/oxbafv01.png
      :alt: Example: Product with 2 kg weight
      :width: 650
      :class: with-shadow

      Fig.: Example: Product with 2 kg weight

#. Create two shipping cost rules with weight as the condition:

   * The first applies to carts with a total weight under 3 kg, and charges €3.90.
   * The second applies to heavier carts and charges €5.50 (:ref:`oxbafv02`).

   Define the shipping cost rules to apply only once per cart.

   Assigning countries is optional.

   .. _oxbafv02:

   .. figure:: ../../media/screenshots/oxbafv02.png
      :alt: Example: Shipping cost rule for total weight from 3 kg
      :width: 650
      :class: with-shadow

      Fig.: Example: Shipping cost rule for total weight from 3 kg

#. Assign the shipping cost rules to a shipping method.

|result|

If the customer selects this shipping method during purchase, all related shipping cost rules will be evaluated.

* If the cart contains one item weighing 2 kg, the first rule applies.
* If the cart contains two or more items each weighing 2 kg, the second rule applies.

.. seealso:: :doc:`Products - Extended tab <../products/extended-tab>` | :doc:`Shipping cost rules - Main tab <../shipping-cost-rules/main-tab>` | :doc:`Shipping methods - Main tab <../shipping-methods/main-tab>`

