Defining Scale Prices
=====================

Use scale prices to offer quantity discounts for selected products.

Lower prices are automatically applied when a customer orders larger quantities.

For each scale, you can define either a fixed price or a percentage-based discount.

By adding multiple quantity ranges, you can define different price tiers for the same product.

In OXID eShop, scale prices are displayed on the product detail page (:ref:`oxbafm01`, item 2) when the customer selects the :guilabel:`Block price` button (:ref:`oxbafm01`, item 1).

The price displayed in the shopping cart depends on the quantity specified during purchase.

.. _oxbafm01:

.. figure:: ../../media/screenshots/oxbafm01.png
   :alt: Displaying scale prices
   :width: 650
   :class: with-shadow

   Fig.: Displaying scale prices

|procedure|

Define scale prices in the product management section.

1. Choose :menuselection:`Administer Products --> Products`.
#. Select the desired product from the product list.
#. In the :guilabel:`Stock` tab, under :guilabel:`Scale Prices`, enter a quantity range and the corresponding price (:ref:`oxbafm02`, item 1).

   Example: For quantities between 5 and 10, the price is €33.99 instead of the regular price of €35.99 set in the :guilabel:`Main` tab.

#. Save your changes and add additional scale prices using the same structure.

   Example: For all quantities above 10, the price is €30.

   Make sure the :guilabel:`To` field for the highest scale includes a sufficiently high value, such as `999999`.

   Otherwise, the regular product price will apply if the upper limit is exceeded.

.. _oxbafm02:

.. figure:: ../../media/screenshots/oxbafm02.png
   :alt: Defining scale prices
   :width: 650
   :class: with-shadow

   Fig.: Defining scale prices

Scale Prices Together with Discounts
------------------------------------

Scale prices are similar to discounts. When you configure discounts for products that have scale prices, the discount's :guilabel:`Purchase Price` is compared to the original product price and not to the scale price.

|example|

* You have a product with original price of EUR 10.00.
* The product also has a scale price for 10 to 99 which is EUR 9.00.
* Then you add a discount of 50% for the product with a conditional :guilabel:`Purchase Price` of EUR 100.00.

If you put an amount of ten items into the shopping cart, the original price sum is EUR 100.00. Therefore the discount of 50% is applied. However, since you have ten items in your shopping cart, the scale price of EUR 9.00 will also apply. This means the total order sum results in EUR 45.00 due to the scale price and the 50% discount.

You can also add another item to you shopping cart, resulting in eleven times the same product. With quantity discount you reach EUR 99.00. However, the original price sum - not scale price - is EUR 110.00 and therefore the 50% discount is applied. You pay EUR 49.50.

This behavior applies to product and category specific discounts. General discounts compare the configured :guilabel:`Purchase Price` to the total order sum which is calculated including the quantity discounts.

|example|

Same scenario as before but this time with a general discount. If you now add ten items to the shopping cart, the total order sum is EUR 90.00 due to the quantity discount starting at an amount of ten. The 50% discount is not applied since the total order sum is below EUR 100.00.

Now put any other product to the shopping cart. Let's say a product with a price of EUR 15.00. The total order sum results in EUR 105.00. The :guilabel:`Purchase Price` is reached and the 50% discount is applied.

.. hint:: Discounts coming from :doc:`coupon series <../../operation/coupon-series/coupon-series>` are always calculated using the total order sum since they only have the option :guilabel:`Min. Order Sum` and no :guilabel:`Purchase Price` which may interfere with scale prices.

.. seealso:: :doc:`Products – Stock tab <../products/stock-tab>`

.. Intern: oxbafm, Status:

