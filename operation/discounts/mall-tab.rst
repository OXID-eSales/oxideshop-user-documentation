Using Individual Discounts in Subshops
======================================

Manage discounts centrally in the parent shop and define which discounts apply in which subshops.

This feature is available only in the Enterprise Edition with the :guilabel:`Mall` tab.

It is only available for subshops. Multishops automatically use discounts from :emphasis:`all` shops.

Inheriting Discounts to Subshops
--------------------------------

|procedure|

1. Create a subshop.

   Under :menuselection:`Master Settings --> Core Settings --> Create New Shop`, you have the following options:

   .. _manage-discounts-step1:

   * Inherit all items and discounts by default to your subshops.

     Later, you can manually exclude specific discounts that should not apply in the subshop.
     (Alternatively, you can disable all inherited discounts: see :ref:`operation/discounts/mall-tab:Removing Inherited Discounts in Subshops`.)

     To do this, check the :guilabel:`Shop inherits all inheritable items (products, discounts etc.) from its parent shop` checkbox (:ref:`oxbahl02`, Pos. 1).

   * Do not inherit items and discounts, and manually assign the discounts you want to apply in your subshop.

   .. _oxbahl02:

   .. figure:: ../../media/screenshots/oxbahl02.png
      :alt: Example: Creating a subshop with inherited settings
      :width: 650
      :class: with-shadow

      Fig.: Example: Creating a subshop with inherited settings

#. Configure discounts in the parent shop that should be available for all subshops.
#. Choose a discount.
#. Go to the :guilabel:`Mall` tab.

   A list will display which subshops apply the discount (:ref:`oxbahl01`).

   .. _oxbahl01:

   .. figure:: ../../media/screenshots/oxbahl01.png
      :alt: Mall Tab: Managing Links to Subshops and Supershops
      :width: 650
      :class: with-shadow

      Fig.: Mall Tab: Managing Links to Subshops and Supershops

#. Depending on how you set up your subshop in :ref:`Step 1 <manage-discounts-step1>`, activate or deactivate the discount for specific subshops.
#. Save your settings.
#. Optional: To create additional discounts that apply only to a specific subshop, choose :menuselection:`Shop Settings --> Discounts` .

Removing Inherited Discounts in Subshops
----------------------------------------

Disable inherited discounts if needed.

|procedure|

#. Switch to the desired subshop.
#. Choose :menuselection:`Master Settings --> Core Settings` and go to the :guilabel:`Mall` tab.
#. Uncheck :guilabel:`Inherit all discounts from parent shop` (:ref:`oxbahl03`, item 1).

  .. _oxbahl03:

  .. figure:: ../../media/screenshots/oxbahl03.png
     :alt: Disabling inherited discounts
     :width: 650
     :class: with-shadow

     Fig.: Disabling inherited discounts

|result|

The discount remains available in the parent shop but is no longer applied in the respective subshop or supershop.

.. Intern: oxbahl, Status:, F1: discount_mall.html