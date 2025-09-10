Scale Prices
============

Define scale prices for selected products to offer a discounted price based on the purchased quantity, either as an absolute price or as a percentage discount. Multiple quantity ranges form a scale with different product prices.

In OXID eShop, the scale prices are displayed on the product's details page when the customer clicks on the :guilabel:`Block Price` button. The system applies the corresponding scale price in the shopping cart based on the quantity entered at the time of purchase and displays it.

.. figure:: ../../media/screenshots/oxbafm01.png
   :alt: Scale prices, product's details page
   :class: with-shadow
   :height: 318
   :width: 500

   Fig.: Scale prices, product's details page

Configuring Scale Prices
------------------------

Define the scale price in the product management section.

|procedure|

1. Go to :menuselection:`Administer Products --> Products`.
#. Choose the desired product from the product list.
#. In the :guilabel:`Stock` tab, locate the :guilabel:`Quantity From`, :guilabel:`To`, and :guilabel:`Price` input fields.
#. Specify a quantity range and set a price. Determine whether the price is specified as an absolute amount or as a percentage discount.
#. Save the scale price.
#. Add additional scale prices.

.. important::

   Ensure that the :guilabel:`To` field of the highest scale contains a sufficiently large quantity (e.g., 999999).

   This prevents the original price from being applied when the maximum scale quantity is exceeded.

Using Scale Prices in Combination with Discounts
------------------------------------------------

Scale prices are similar to discounts.

The combination of scale prices with discounts depends on the type of discount. Product-specific and category-specific discounts check the minimum purchase amount, from which a discount applies, against the original price, while general discounts consider the scale-adjusted total order sum. The scale-adjusted sum refers to the total order sum after applying the scale prices, but before applying additional discounts.

Product-Specific and Category-Specific Discounts
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

When configuring discounts for products with scale prices, the minimum purchase amount defined in the :guilabel:`Purchase Price` field is compared to the original price (the product's original price without quantity discount), not to the scale price.

|example|

* You have a product with an original price of 10.00 EUR.
* The product has a scale price for quantities from 10 to 99 units at 9.00 EUR.
* You add a 50% discount that is triggered at a price sum of 100.00 EUR (the minimum purchase amount defined in the :guilabel:`Purchase Price` field, from which a discount applies).

If you add ten products to the shopping cart, the original price sum is 100.00 EUR, triggering the 50% discount. Since the quantity of ten products activates the scale price of 9.00 EUR, the total order sum is 45.00 EUR (after applying the discount to the scale-adjusted sum).

You can also add another product to your shopping cart, resulting in eleven times the same product. With the quantity discount, you reach EUR 99.00. However, the original price sum – not the scale price – is EUR 110.00, which is why the 50% discount is applied. You pay EUR 49.50.

This behavior applies to product-specific and category-specific discounts. General discounts compare the minimum purchase amount defined in the :guilabel:`Purchase Price` field to the total sum of the order, which is calculated taking into account the quantity discounts.

**Explanation of the Calculation Path (Product- or Category-Specific Discount with 10 Products):**

The system prioritizes checking the minimum purchase amount defined in the :guilabel:`Purchase Price` field, from which a discount applies, based on the original price sum to trigger the discount condition. Subsequently, the scale price is applied to the quantity, and the discount affects the scale-adjusted sum. The detailed process is as follows:

.. list-table::
   :header-rows: 1
   :widths: 10 50 25 15

   * - Step
     - Description
     - Calculation
     - Result
   * - 1
     - Determine original price sum (for discount condition)
     - 10 × 10.00 EUR
     - 100.00 EUR
   * - 2
     - Check discount condition and apply discount factor (since sum ≥ 100.00 EUR)
     - Trigger discount: 50% (factor 0.5)
     - Discount activated
   * - 3
     - Apply scale price (quantity 10 matches 10–99)
     - 10 × 9.00 EUR
     - 90.00 EUR (scale-adjusted sum)
   * - 4
     - Apply discount to scale-adjusted sum
     - 90.00 EUR × 0.5
     - 45.00 EUR (total sum)

If you add another product, resulting in a total of eleven identical products in the shopping cart. With the scale price, you reach a subtotal of 99.00 EUR. However, the original price sum (without scale price) is 110.00 EUR, which is why the 50% discount is applied. You pay 49.50 EUR.

**Explanation of the Calculation Path (Product- or Category-Specific Discount with 11 Products):**

Similar to above, the discount condition is checked on the original price sum, the scale price is applied separately, and the discount is then applied to the scale-adjusted sum:

.. list-table::
   :header-rows: 1
   :widths: 10 50 25 15

   * - Step
     - Description
     - Calculation
     - Result
   * - 1
     - Determine original price sum (for discount condition)
     - 11 × 10.00 EUR
     - 110.00 EUR
   * - 2
     - Check discount condition and apply discount factor (since sum ≥ 100.00 EUR)
     - Trigger discount: 50% (factor 0.5)
     - Discount activated
   * - 3
     - Apply scale price (quantity 11 matches 10–99)
     - 11 × 9.00 EUR
     - 99.00 EUR (scale-adjusted sum)
   * - 4
     - Apply discount to scale-adjusted sum
     - 99.00 EUR × 0.5
     - 49.50 EUR (total sum)


General Discounts
^^^^^^^^^^^^^^^^^

General discounts compare the minimum purchase amount defined in the :guilabel:`Purchase Price` field, from which a discount applies, to the total order sum, which is calculated taking into account the scale prices.

|example|

The same scenario as before, but this time with a general discount. If you add ten products to the shopping cart, the total order sum is 90.00 EUR due to the scale price (from a quantity of ten). The 50% discount is not applied because the total order sum is below 100.00 EUR.

**Explanation of the Calculation Path (General Discount with 10 Products):**

For general discounts, the condition check occurs after applying the scale prices, leading to a different logic:

.. list-table::
   :header-rows: 1
   :widths: 10 50 25 15

   * - Step
     - Description
     - Calculation
     - Result
   * - 1
     - Apply scale price (quantity 10 matches 10–99)
     - 10 × 9.00 EUR
     - 90.00 EUR (total sum)
   * - 2
     - Check discount condition (on scale-adjusted sum)
     - 90.00 EUR < 100.00 EUR
     - No discount
   * - 3
     - Final sum
     - No further adjustment
     - 90.00 EUR (total sum)

Now add another product to the shopping cart, e.g., a product with a price of 15.00 EUR. The total order sum is now 105.00 EUR. The minimum purchase amount defined in the :guilabel:`Purchase Price` field is reached, and the 50% discount is applied.

**Explanation of the Calculation Path (General Discount with 10 Products + Additional Product):**

The scale prices are first applied to the relevant products, then the total sum is checked, and the discount is applied to the entire sum:

.. list-table::
   :header-rows: 1
   :widths: 10 50 25 15

   * - Step
     - Description
     - Calculation
     - Result
   * - 1
     - Apply scale price for main product
     - 10 × 9.00 EUR
     - 90.00 EUR
   * - 2
     - Add additional product
     - 90.00 EUR + 15.00 EUR
     - 105.00 EUR (total sum)
   * - 3
     - Check and apply discount condition (since sum ≥ 100.00 EUR)
     - 105.00 EUR × 0.5
     - 52.50 EUR (total sum)


.. hint:: Discounts from coupon series are always calculated based on the total order sum, as they only use the :guilabel:`Min. Order Sum` option and no minimum purchase amount (:guilabel:`Purchase Price` field) that could conflict with scale prices.

  For more information, see :doc:`Coupon Series <../../operation/coupon-series/coupon-series>`.

.. seealso:: :doc:`Products - Stock Tab <../products/stock-tab>`

.. Intern: oxbafm, Status:

