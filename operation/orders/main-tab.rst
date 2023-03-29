Main tab
========

The :guilabel:`Main` tab allows you to add or change the order information. This applies to order and invoice numbers as well as payment and shipping information. If the ordered products are downloadable, an e-mail with the download links can be sent to the customer.

.. image:: ../../media/screenshots/oxbaed01.png
   :alt: Orders - Main tab
   :height: 354
   :width: 650

:guilabel:`IP Address`
   Display the IP address from which the customer completed the order.

   .. attention::

      **Privacy**

      Displaying the IP address may be illegal.

      In Germany, you violate privacy laws if you store a customer's IP address along with their order information.

      In other countries, however, such as the United States, you are allowed to collect IP addresses.

      Enable the feature only if you are sure you are not violating any laws.

      You do this under :menuselection:`Master Settings --> Core Settings` on the :guilabel:`System` tab. Under :guilabel:`Order`, choose :guilabel:`Store User IP Addresses (check your local laws if legal)`.

      See also: `Data protection: Are online retailers allowed to store IP addresses of their customers? <http://shop.trustedshops.com/de/rechtstipps/datenschutz-duerfen-online-haendler-ip-adressen-ihrer-kunden-speichern>`_ (Trusted Shops, in German)

:guilabel:`Order No.`
   The store assigns a consecutive order number for each order. Change it if you want the store to continue counting from the next order with the following order number.

:guilabel:`Invoice No.`
   Enter your custom invoice number.

   If you leave this field empty, the order number will also be the invoice number.

:guilabel:`Discount` ... :guilabel:`(EUR)`
   If a discount was effective for the ordered items, it will be displayed here.

   You can change or grant a discount afterwards. Enter the value in the input field and save the changes. The total price of the order will be recalculated.


:guilabel:`Payment Information`
   Document the receipt of payment for the order.

   To do this, in the :guilabel:`Paid on` field, set the payment date in the :code:`YYYY-MM-DD HH:MM:SS` format.

   After saving, a new line will appear with the :guilabel:`Order was paid` note and the date and time information.

   If you want to use the current date for the orders, just click on the link with the same name and it will be entered into the input field.

:guilabel:`Payment with`
   Use the drop-down list to select the payment method that the customer used to complete the order.

   If necessary, you can assign a different active payment method to the order. To do this, choose the desired payment method from the drop-down list and save the changes.

:guilabel:`Shipping Information`
   When placing an order, the customer has chosen a shipping method, which is displayed together with the shipping costs.

   Change this information if necessary.

   The :guilabel:`Ship Now`, :guilabel:`Reset Shipping Date` and :guilabel:`Send e-mail?` buttons perform the same function as in the :guilabel:`Overview` tab. You can set the shipping date and inform the customer about the shipment of the products by e-mail.

   The :guilabel:`Shipped on` line will be filled with the date and time.

.. _tracking-url-orders:

:guilabel:`Shipping Information - Tracking Code`
   Enter the package ID of the order (epending on the shipping service provider tracking code, parcel label number, package reference, shipment number, etc.).

   For tracking purposes, the tracking link, consisting of the tracking URL and the package ID of the order, is generated and sent to your customer with the email notifying him/her of the shipment of the goods.

   The tracking link is also displayed in the customer's order history in the frontend.

   You can define the tracking URL separately for each shipping method.
   |br|
   To find out how to do this, see :ref:`Tracking-URL <tracking-url-shipping-method>`.

   If you have not defined a special tracking URL for a shipping method, the system uses the tracking URL you have defined in the administration area under :menuselection:`Master Settings --> Core Settings --> Settings --> Other settings`.

   By default, shipment tracking is configured for the DPD (Dynamic Parcel Distribution) shipping service provider.



:guilabel:`Ordered download links`
   With downloadable products, offer software, photos, music files or document templates, for example.

   If the customer puts a download item in the shopping basket, he or she acquires all the associated files that can be downloaded from the shop.

   To send an e-mail with the download links to the customer, choose the :guilabel:`Send` button.



.. Intern: oxbaed, Status:, F1: order_main.html, transL