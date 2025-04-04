Defining payment methods for specific users
===========================================

As a shop owner, you make a fundamental decision about which payment methods to offer your customers.

Decide for which customers it is acceptable to ship goods before receiving payment—and for which customers such advance delivery is not appropriate.

Payment by invoice is very popular with customers, as it allows them to inspect or test the goods before paying. However, this creates a risk for shop owners: not every customer pays their invoice on time—or at all.

In OXID eShop, you can restrict payment methods to specific users in two ways:

* Assign a credit rating to the payment method
* Assign the payment method to a user group

Assigning a credit rating to a payment method
---------------------------------------------

One option is to assign a required credit rating to the payment method.

This setting ensures that only customers whose credit rating is greater than or equal to the defined value will see the payment method during checkout.

Keep in mind: this approach can be time-consuming, as each user's credit rating must be individually defined and maintained.

1. Define the required credit rating for the payment method.

   a. Go to :menuselection:`Shop Settings --> Payment Methods`.
   #. Select the desired payment method from the list.
   #. In the :guilabel:`Main` tab, enter a credit rating value.
   #. Save your changes.

2. Assign a credit rating to each individual user.

   a. Go to :menuselection:`Administer Users --> Users`.
   #. Select the desired user from the list.
   #. In the :guilabel:`Extended` tab, enter a value in the :guilabel:`Credit Rating` field.
   #. Save your changes.

Assigning payment methods to user groups
----------------------------------------

The second option is to assign payment methods to specific user groups.

For example, you can allow payment by invoice only for the user group "Retailers".

|procedure|

1. Go to :menuselection:`Shop Settings --> Payment Methods`.
#. Select the desired payment method from the list.
#. In the :guilabel:`Main` tab, click :guilabel:`Assign User Groups`.
#. Drag and drop the user group into the right-hand list of the assignment window.
#. Close the assignment window.

.. seealso:: :doc:`Payment Methods - Main tab <../payment-methods/main-tab>` | :doc:`Users - Extended tab <../../operation/users/extended-tab>`

.. Intern: oxbafu, Status: