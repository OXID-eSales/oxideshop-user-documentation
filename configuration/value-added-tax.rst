Value Added Tax
===============

Set the basic global settings for calculating and displaying VAT in your store.

If needed, you can set special VAT rates for categories or individual items and variants in the next step.


Making global VAT settings
--------------------------

Make basic settings for VAT.

The default settings after installation are suitable for most stores, so usually no changes are needed here.

All listed options are not active by default, and 19 percent is the default for VAT.


|procedure|

In the administration area under :menuselection:`Master Settings --> Core Settings --> Settings --> VAT`, check which of the following options is suitable for you:

:guilabel:`Default VAT rate for all items`.
   The number 19 in the input field means that a VAT rate of 19 percent applies by default to all items in your store.
   |br|
   Optional: If required, define a VAT rate for individual items that differs from the standard VAT rate, for example, 7 percent for food.

:guilabel:`Enter Product Prices as Net Prices (plus VAT)` |br|
   Optional: Enter the item price as net price for all items.
   |br|
   VAT must then be calculated for each item in the store before the item can be displayed with its gross price.
   |br|
   There is an option that ensures that the VAT is only displayed in the shopping cart and ordering process.
   |br|
   So, the store would display items with net prices and only when an item is added to the shopping cart, the VAT would be calculated and displayed.
   |br|
   Find the :guilabel:`Calculate specific VAT only in Shopping Cart and Checkout` option under :menuselection:`Master Settings --> Core Settings --> Perform.`

:guilabel:`Show net prices in frontend (B2B)`
   Optional: Operate your store as a store for business customers.

:guilabel:`VAT calculation of additional services`
   Optional: Specify how you want to calculate VAT for shipping costs, fees or packaging.

**Optional**: Specify if the ancillary services (shipping, payment fees or packaging) are to be entered as net prices.

**Optional**: Specify how amounts for ancillary services are to be displayed in the shopping cart and on the invoice.

By default, the gross amount is displayed. However, you can also display the net amount plus VAT in each case.

:guilabel:`Use shipping country for VAT calculation instead of billing country`.
   The default setting after installation is to calculate VAT based on the billing address.
   |br|
   The address of the invoice recipient determines whether VAT is calculated or not.
   |br|
   Optional: Set the shipping address as the basis for calculating VAT.


Making special VAT settings
---------------------------

Specify the VAT rates that should apply to specific categories or individual items, in deviation from the global VAT rates.


|prerequisites|

* Under :menuselection:`Master Settings --> Core Settings --> Settings --> VAT --> Default VAT for all Products`, you have set the global default VAT rate (see :ref:`configuration/value-added-tax:Making global VAT settings`).

|procedure|

Set special VAT rates as follows:

* For a category: Choose :menuselection:`Administer Products --> Categories --> [desired category] --> Main --> Spec. VAT`.
* For an item: Choose :menuselection:`Administer Products --> Products --> [desired product] --> Main --> Spec. VAT`.
* Variant of an item: Choose :menuselection:`Administer Products --> Products --> [desired product] --> Variants --> Edit Variant --> Spec VAT.`

.. hint::

   **Categories with different VAT rates**

   It may happen that the same item is assigned to categories with different VAT rates.

   In this case, OXID eShop calculates VAT according to the VAT rate of the parent category or according to the category to which you assigned the item first.


.. Intern: oxbaay, Status: