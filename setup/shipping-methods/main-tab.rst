Main tab
========

On the :guilabel:`Main` tab, configure the shipping method.

Assign, for example, shipping rules and countries to the shipping method. Set a tracking URL so that the system can send a tracking link to your customer.

.. image:: ../../media/screenshots/oxbade01.png
   :alt: Shipping methods - Main tab
   :height: 339
   :width: 650

:guilabel:`Name`
   Enter the name of the shipping method. It will be displayed to the customer in ordering step 3. If multiple shipping methods are valid, one of them must be selected from a drop-down list.

:guilabel:`Active`
   For the shipping method to be active and usable, activate the checkbox.

:guilabel:`Active for a period`
   Specify a time period when the shipping method should be active. The input format should be YYY-MM-DD HH:MM:SS. To have the time period applied, don’t check the :guilabel:`Active` box.

:guilabel:`Sorting`
   Set the order of shipping types in the drop-down list. The shipping method with the smallest number will be listed first and preselected.

:guilabel:`Tracking URL`
   A separate tracking URL can be defined for each shipping method. ##ID## serves as a placeholder, which is replaced by the respective package ID of the order (depending on the shipping service provider tracking code, parcel label number, package reference, shipment number, etc).

   If a shipping method does not have its own tracking URL, the one entered in the administration panel under :menuselection:`Master data --> Basic settings --> Settings. --> Other settings` will be used.

   Tracking URL and specific package ID of the order are combined to the tracking link. It will be sent to the customer as a tracking link in the e-mail informing him/her of the shipment. The tracking link is also displayed in the customer's order history in the frontend.

:guilabel:`In Language`
   The shipping method can be edited in other active languages of the shop. To do this, select the desired language from the drop-down list.

:guilabel:`Copy to`
   You will need to copy a shipping method before it can be edited in another active language. To do this, select the language from the drop-down list and click on :guilabel:`Copy to`. This button won’t be displayed if there are no other active languages in the shop.

:guilabel:`Assign Shipping Cost Rules`
   You will need to assign at least one shipping cost rule to the shipping method. Clicking on :guilabel:`Assign Shipping Cost Rules` opens a new window. All available shipping cost rules will be displayed in the left-hand list. Shipping cost rules can be filtered by title, cost and/or type (absolute or percentage price) and sorted in the ascending or descending order. Drag and drop the shipping cost rules into the right-hand list to complete the assignment.

:guilabel:`Assign Countries`
   Assigning countries to the shipping method ensures clear payment and shipping conditions. If countries have been assigned and a customer places an order from a country to which no shipping method has been assigned, he/she will receive the following notification: \"No shipping method has been defined for this country. We will try to find delivery options and inform you about shipping costs.\". The payment methods won’t be displayed to the customer.

   If no country has been assigned, the shipping method will apply to all countries.

   Clicking on :guilabel:`Assign Countries` opens a new window with all active countries displayed in the left-hand list. Countries can be sorted and filtered by title and/or country abbreviation (ISO Alpha 2). Drag the desired countries into the right-hand list using the mouse. Hold down the Ctrl key to select multiple countries. The assignment to the shipping method is now completed.


.. Intern: oxbade, Status:, F1: deliveryset_main.html, transL