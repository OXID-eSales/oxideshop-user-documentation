Main tab
========

Coupon series combine a number of coupons. They can be created and edited in the :guilabel:`Main` tab. You can define the validity of a coupon series which also determines the validity of the coupons belonging to the series. An absolute or relative discount represents the actual value of a coupon, which will be applied in the shopping cart. The coupons of a series can be generated with a fixed or a random coupon code and exported as a file in CSV format. A small overview shows the number of all generated, redeemed and unused coupons.

.. image:: ../../media/screenshots/oxbahs01.png
   :alt: Coupon series - Main tab
   :height: 343
   :width: 650

The assignment of user groups, categories and/or products takes place in the next tab.

:guilabel:`Name` |br|
Name of the coupon series. This is only displayed in the list of coupon series and can be used to search for coupon series.

:guilabel:`Description` |br|
Enter a short description to provide more detailed information about a coupon series.

:guilabel:`Valid from` |br|
You can specify a corresponding time period for the coupon series if the coupons should only be used in a temporary marketing campaign, such as a summer sale, Christmas sale or a late night sale. This time period will also apply to the individual coupons. Enter the start of validity in the YYYY-MM-DD HH:MM:SS format. Without the start date, the coupon series will be valid until a set end time, or it is unlimited.

:guilabel:`Valid until` |br|
The end of validity for the coupon series in the YYYY-MM-DD HH:MM:SS format. Without the end date, the coupon series will be valid from a set start time, or it is unlimited.

:guilabel:`Discount` |br|
Define the coupon value that will be applied when the customer redeems the coupon in the shopping cart. This can be expressed as a percentage or in absolute terms. Select the type of the coupon value in the selection list following the input field. |br|
:guilabel:`abs`: The coupon value is absolute, e.g. €10. |br|
:guilabel:`%`: The coupon value is based on a percent, e.g. 10% of the purchase value.

.. hint:: If multiple coupons are used for an order, the coupon value may be duplicated depending on the other settings.

:guilabel:`Valid with purchase amount` |br|
A coupon in this series will only be accepted by the shop when a defined purchase value has been reached. If you leave this field empty, the purchase value of the products in the shopping cart won’t be taken into account.

:guilabel:`Valid with same Series` |br|
Specify whether your customers may use multiple coupons from the same coupon series when placing an order. If multiple coupons can be used for an order, they will only be accepted if the total order amount is greater than €0.00. If you select :guilabel:`No`, they will only be able to redeem one coupon in this series per order.

:guilabel:`Valid with different Series` |br|
Use this option to specify whether customers may combine coupons of different series within one order. If you select :guilabel:`No`, they won’t be able to combine coupons from this series with coupons from other series. If you select :guilabel:`Yes`, you will also need to select :guilabel:`Yes` for the coupon series to be combined.

:guilabel:`Valid with same Series, different Order` |br|
Select :guilabel:`Yes` to allow your customers to use coupons from this coupon series for several orders. Select :guilabel:`No` to specify that coupons in this series can only be redeemed for one order.

:guilabel:`Calculate only once (valid only for product or category vouchers)` |br|
This setting only affects coupons of a coupon series that have products and/or categories assigned to them. If the box is checked, the coupon will be redeemed for only one of the products assigned to the coupon series even if the shopping cart contains several such products. If the box is not checked, the coupon will be applied to each of these products.

:guilabel:`Coupons - Quantity` |br|
Number of coupons generated for the coupon series.

:guilabel:`Coupons - Available` |br|
Number of coupons in this coupon series that have not yet been used.

:guilabel:`Coupons - Used` |br|
Number of redeemed coupons in this coupon series.

:guilabel:`Create new Coupons (optional)` |br|
You can create as many coupons as you wish for a coupon series. They can be generated once or, if necessary, multiple times. During export, a file containing the generated coupon numbers will be written to a file and stored in the shop's :file:`/export` directory.

:guilabel:`Random Numbers` |br|
If this option is enabled, coupons will be generated with a 32-digit alphanumeric coupon code. Example of a random coupon code: f2119e0585d1c5514f6729c703f14bf0

:guilabel:`Coupon Number` |br|
Enable this option if you want to create coupons with the same coupon code. All generated coupons will receive the coupon code that you have entered here. Example of the same coupon code: SALE2018

:guilabel:`Quantity` |br|
Specify how many coupons in the coupon series should be generated.

:guilabel:`Generate` |br|
Press this button to generate the coupons. If necessary, you can also add new coupons to the coupon series. Coupons with their coupon code will be stored in the oxvoucher table of the database.

:guilabel:`Export` |br|
The button allows you to write the generated coupons with the coupon codes in a file. This is especially necessary if coupons have been generated with random coupon codes as they are not displayed in the Admin panel. The file will list all coupons, including those already redeemed. It will be saved in the shop’s :file:`/export` directory and can be opened with any text editor or spreadsheet program.

.. Intern: oxbahs, Status:, F1: voucherserie_main.html