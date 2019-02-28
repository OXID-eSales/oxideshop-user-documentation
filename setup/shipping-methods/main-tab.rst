Main tab
========

The :guilabel:`Main` tab contains several settings for the shipping method. Shipping cost rules and countries can be assigned here.

.. image:: ../../media/screenshots/oxbade01.png
   :alt: Shipping methods - Main tab
   :height: 343
   :width: 650

:guilabel:`Name` |br|
Enter the name of the shipping method. It will be displayed to the customer in ordering step 3. If multiple shipping methods are valid, one of them must be selected from a drop-down list.

:guilabel:`Active` |br|
Check this box to make the shipping method active and useable.

:guilabel:`Active for a period` |br|
Specify a time period when the shipping method should be active. The input format should be YYY-MM-DD HH:MM:SS. To have the time period applied, don’t check the :guilabel:`Active` box.

:guilabel:`Sorting` |br|
Sorting determines the order in which shipping methods appear in the drop-down list. The shipping method with the smallest number will be listed first and preselected.

:guilabel:`In Language` |br|
The shipping method can be edited in other active languages of the shop. To do this, select the desired language from the drop-down list.

:guilabel:`Copy to` |br|
You will need to copy a shipping method before it can be edited in another active language. To do this, select the language from the drop-down list and click on :guilabel:`Copy to`. This button won’t be displayed if there are no other active languages in the shop.

:guilabel:`Assign Shipping Cost Rules` |br|
You will need to assign at least one shipping cost rule to the shipping method. Clicking on :guilabel:`Assign Shipping Cost Rules` opens a new window. All available shipping cost rules will be displayed in the left-hand list. Shipping cost rules can be filtered by title, cost and/or type (absolute or percentage price) and sorted in the ascending or descending order. Drag and drop the shipping cost rules into the right-hand list to complete the assignment.

:guilabel:`Assign Countries` |br|
Assigning countries to the shipping method ensures clear payment and shipping conditions. If countries have been assigned and a customer places an order from a country to which no shipping method has been assigned, he/she will receive the following notification: \"No shipping method has been defined for this country. We will try to find delivery options and inform you about shipping costs.\". The payment methods won’t be displayed to the customer.

If no country has been assigned, the shipping method will apply to all countries.

Clicking on :guilabel:`Assign Countries` opens a new window with all active countries displayed in the left-hand list. Countries can be sorted and filtered by title and/or country abbreviation (ISO Alpha 2). Drag the desired countries into the right-hand list using the mouse. Hold down the Ctrl key to select multiple countries. The assignment to the shipping method is now completed.

.. Intern: oxbade, Status:, F1: deliveryset_main.html