Payment methods for specific users
====================================

Shop owners have to make a fundamental decision about which payment methods their customers can use. They need to decide for which customers it is acceptable to ship the products before receiving the payment and for which customers such advanced shipping is not efficient. For example, payment against invoice is very popular with customers since it allows them to look at the products or try them out before paying. However, for shop owners, this means an increased risk because not all customers pay their bill on time or at all.

OXID eShop allows you to offer payment methods only for specific users in two different ways. One of these is the credit rating that can be stored for payment methods. This setting ensures that the payment method in the ordering process will only be displayed to customers whose credit rating is greater or equal to the credit rating of the payment method. This option can be very time-consuming because the credit rating will need to be defined and kept up to date for each individual user.

The required credit rating for the payment method is defined.

* Go to :menuselection:`Shop Settings --> Payment Methods`.
* Select the desired payment method from the list.
* Enter the required credit rating in the :guilabel:`Main` tab.
* Save the settings.

The credit rating must be defined for each individual user.

* Go to :menuselection:`Administer Users --> Users`.
* Select the desired user from the user list.
* Enter a value in the :guilabel:`Credit Rating` field in the :guilabel:`Extended` tab.
* Save the settings.

The second option for customer-related payment methods in the ordering process is to assign user groups to payment methods. For example, you can specify that only the “Retailer” user group can use payment against invoice as the payment method.

Assigning user groups to a payment method

* Go to :menuselection:`Shop Settings --> Payment Methods`.
* Select the desired payment method from the list.
* Click on :guilabel:`Assign User Groups` in the :guilabel:`Main` tab.
* Drag and drop the user group into the right-hand list of the assignment window.
* Close the assignment window.

.. seealso:: :doc:`Payment methods - Main tab <../payment-methods/main-tab>` | :doc:`Users - Extended tab <../../operation/users/extended-tab>`

.. Intern: oxbafu, Status: