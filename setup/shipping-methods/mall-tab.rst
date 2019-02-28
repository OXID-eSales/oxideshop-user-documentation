Mall tab
========

The :guilabel:`Mall` tab is only available for shipping methods in OXID eShop Enterprise Edition.

Shipping methods can be inherited when creating shops. If the option :guilabel:`Shop inherits all inheritable items (products, discounts etc) from it's parent shop` is selected, the new shop will also contain all the shipping methods of the parent shop. The inherited shipping methods can’t be changed and retain the original assignments to the payment methods, the user groups or individual users.

The :guilabel:`Mall` tab can be used to manage the assignments of shipping methods to subshops and supershops. Multishops don’t inherit shipping methods from other shops.

.. image:: ../../media/screenshots/oxbadh01.png
   :alt: Shipping methods - Mall tab
   :height: 343
   :width: 650

The inheritance of all shipping methods for a shop can be undone. To do this, uncheck the box :guilabel:`Inherit delivery information from parent shop` in the Mall tab of the subshop or supershop under :menuselection:`Master Settings --> Core Settings`. This will also remove the assignment to the inherited shipping cost rules.

:guilabel:`Assigned to following subshops` |br|
Check or uncheck the appropriate box to assign/unassign the shipping method to/from subshops and supershops. If the box is not checked, the shipping method will be available in the parent shop but not in the respective subshop or supershop.

Use the :guilabel:`Select All` and :guilabel:`Select None` links on the right side of the window to assign/unassign the shipping method to/from all shops. Any changes made must be saved and will immediately be effective for subshops or supershops.

.. Intern: oxbadh, Status:, F1: deliveryset_mall.html