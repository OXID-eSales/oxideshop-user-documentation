Main tab
========

On the :guilabel:`Main` tab, configure the shipping method.

Assign, for example, shipping rules and countries to the shipping method. Set a tracking URL so that the system can send a tracking link to your customer.

.. image:: ../../media/screenshots/oxbade01.png
   :alt: Shipping methods - Main tab
   :height: 339
   :width: 650

:guilabel:`Name`
   Enter the name of the shipping method.

   It will be displayed to the customer in ordering step 3.

   If multiple shipping methods are valid, one of them must be selected from a drop-down list.

:guilabel:`Active`
   For the shipping method to be active and usable, activate the checkbox.

:guilabel:`Active for a period`
   Specify a time period when the shipping method should be active.

   The input format is :code:`YYY-MM-DD HH:MM:SS`.

   For the period to be taken into account, make sure that :guilabel:`Always active` is unchecked.

:guilabel:`Sorting`
   Set the order of shipping types in the drop-down list.

   The shipping method with the smallest number will be listed first and preselected.


.. _tracking-url-shipping-method:

:guilabel:`Tracking-URL`.
   Specify a tracking URL.

   Example (:ref:`oxbade02`, item 1): :code:`https://www.dhl.com/de-de/home/tracking/tracking-express.html?tracking-id=##ID##`

   The system replaces the placeholder :code:`##ID##` with the respective package ID of the order (depending on the shipping service provider tracking code, package slip number, package reference, shipment number, etc.).

   You enter the package ID when you process the respective order.
   |br|
   For more information, see :ref:`Shipping Information - Tracking Code <tracking-url-orders>`.

   .. _oxbade02:

   .. figure:: ../../media/screenshots/oxbade02.png
      :alt: Setting the tracking URL for a shipping method
      :width: 650
      :class: with-shadow

      Figure: Setting the tracking URL for a shipping method

   Result: The tracking URL and the specific package ID of an order are merged into a tracking link. For tracking purposes, the tracking link is sent to the customer with the email informing them that the goods have been shipped.

   The customer can also display the tracking link in the customer order history in the frontend under :menuselection:`My Account --> Order History`.

   If you do not set a custom tracking URL for a shipping method, the system uses the tracking URL you set in :menuselection:`Master Data --> Basic Settings --> Settings. --> Other settings`.

:guilabel:`In Language`
   If you want to edit the shipping method in another active language of the store, select the desired language from the drop-down list.

:guilabel:`Copy to`
   To be able to edit a shipping method in another active language, copy the shipping method.

   Choose the language from the drop-down list and press the :guilabel:`Copy` button. If there is no other active language in the store, this button is not displayed.

:guilabel:`Assign Shipping Cost Rules`
   Assign at least one shipping cost rule to the shipping type.

   Use the :guilabel:`Assign Shipping Cost Rules` button to open a new window. In this assignment window, all shipping cost rules are displayed in the left list.

   Filter and sort the shipping cost rules by title, cost and/or type (absolute or percentage price).

   Drag & drop the shipping rules to the right list. The assignment is complete.

:guilabel:`Assign Countries`
   To ensure clear payment and shipping terms, assign countries to the shipping method.

   If the countries are assigned and a customer orders from a country that does not have a shipping method assigned, the customer receives the following message: \"No shipping method has been defined for this country. We will try to find delivery options and inform you about shipping costs.\". The payment methods are not displayed to him.

   Without country assignment, the shipping method applies to all countries.

   With the :guilabel:`Assign Countries` button, open a new window: In the left list all active countries are displayed.

   Sort and filter the countries by title and/or country abbreviation (ISO Alpha 2).

   Drag the desired countries with the mouse into the list on the right side. Multiple selection is possible by holding down the Ctrl key. This completes the assignment to the shipping type.



.. Intern: oxbade, Status:, F1: deliveryset_main.html, transL