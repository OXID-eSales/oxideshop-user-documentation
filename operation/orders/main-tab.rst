Main tab
========

The :guilabel:`Main` tab allows you to add or change the order information. This applies to order and invoice numbers as well as payment and shipping information. If the ordered products are downloadable, an e-mail with the download links can be sent to the customer.

.. image:: ../../media/screenshots/oxbaed01.png
   :alt: Orders - Main tab
   :height: 354
   :width: 650

:guilabel:`IP Address`
   Displays the IP address that the customer has used to complete the order. This setting has to be activated globally. Go to the :guilabel:`System` tab under :menuselection:`Master Settings --> Core Settings` and click on :guilabel:`Orders` to find the setting :guilabel:`Store User IP Addresses` :guilabel:`(check your local laws if legal)`.

   The name of the setting already draws attention to the fact that the storage of IP addresses can be questionable under data protection law. In Germany, the law clearly states that it is a violation of data protection regulations if shop owners store the customer’s IP addresses together with his/her order data. However, in other countries, such as in the United States, IP addresses can be collected without any issues.

:guilabel:`Order No.`
   Orders get assigned consecutive order numbers in the shop. The order number can be changed here if you want the shop to continue counting starting with the next order by using the subsequent order number.

:guilabel:`Invoice No.`
   Enter your custom invoice number. If you leave this field empty, the order number will also be the invoice number.

:guilabel:`Discount` ... :guilabel:`(EUR)`
   Displays a discount applied to the ordered product, if any. Discounts can also be changed or granted at a later point. Enter the value in the input field and save the changes. The total price of the order will be recalculated.

:guilabel:`Payment Information`
   Allows the shop owner to document the receipt of payment for the order. To do this, set the payment date in the YYYY-MM-DD HH:MM:SS format in the :guilabel:`Paid on` field. After saving, you will see a new line with the note :guilabel:`Order was paid` along with the date and time. If you want to use the current date for the orders, just click on the Current Date link and it will be entered in the input field.

:guilabel:`Payment with`
   Use the drop-down list to select the payment method that the customer used to complete the order. If necessary, you can assign a different active payment method to the order. To do this, select the desired payment method from the drop-down list and save the changes.

:guilabel:`Shipping Information`
   When placing an order, the customer had to select a shipping method that will be displayed together with the shipping costs. The shop owner can change this information if needed.

:guilabel:`Shipping Information - Tracking Code`
   Enter here the package ID of the order (depending on the shipping service provider tracking code, parcel label number, package reference, shipment number, etc.). The tracking link, consisting of the tracking URL and the package ID of the order, is sent to the customer for tracking purposes with the e-mail notifying him/her of the shipment. The tracking link is also displayed in the customer's order history in the frontend.

   The tracking URL can be defined for each individual shipping method. If there is no special tracking URL for a shipping method, the one entered in the Admin panel under :menuselection:`Master Settings --> Core Settings --> Settings --> Other settings` will be used.

   You can enter the tracking URL of the shipping service provider under :menuselection:`Master Settings --> Core Settings --> Settings --> Other settings` in the Admin panel to allow customers to track their orders. The tracking URL and the order's package ID (tracking code, parcel label number, package reference, etc., depending on the shipping service provider) will be sent to the customer as a tracking link in the e-mail informing him/her of the shipment. By default, shipment tracking is configured for the DPD (Dynamic Parcel Distribution) shipping service provider.

   The :guilabel:`Ship Now`, :guilabel:`Reset Shipping Date` and :guilabel:`Send e-mail?` buttons perform the same function as in the :guilabel:`Overview` tab. You can set the shipping date and inform the customer about the shipment of the products by e-mail. The :guilabel:`Shipped on` line will be filled with the date and time.

:guilabel:`Ordered download links`
   With OXID eShop 4.6.0, we have introduced a new product type: downloadable products. These could be software, photos, music files or document templates. When the customer adds a downloadable product to the shopping cart, he/she will receive all the associated files and will be able to download them in the shop. Click on :guilabel:`Send` to send an e-mail with the download links to the customer.

.. seealso:: `Data protection: Are online retailers allowed to store IP addresses of their customers? <http://shop.trustedshops.com/de/rechtstipps/datenschutz-duerfen-online-haendler-ip-adressen-ihrer-kunden-speichern>`_ (Trusted Shops, in German) | `Features/oxCounter implementation <http://oxidforge.org/en/oxcounter-implementation.html>`_ (OXIDforge)


.. Intern: oxbaed, Status:, F1: order_main.html, transL