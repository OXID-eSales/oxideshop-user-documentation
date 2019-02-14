Alternative prices for user groups
======================================
OXID eShop allows you to set alternative product prices for three user groups. These user groups are \"Price A\", \"Price B\" and \"Price C\". When a customer who has been assigned to such a user group logs on to the shop, he/she will see the alternative price for the corresponding products.

Defining alternative prices in the product management section

* Go to :menuselection:`Administer Products --> Products`.  
* Select the desired product from the product list.  
* Input fields :guilabel:`A`, :guilabel:`B` and :guilabel:`C` can be found under :guilabel:`Alt. Prices (€)` in the :guilabel:`Main` tab.  
* Specify alternative prices for the three user groups.  
* Save the changes.  

Users can be assigned to the user groups \"Price A\", \"Price B\"and \"Price C\"in two ways.

Assigning the user group to a single user

* Go to :menuselection:`Administer Users --> Users`.  
* Select the desired user from the user list.  
* Click on :guilabel:`Assign User Groups` in the :guilabel:`Main` tab.  
* Drag and drop the user group into the right-hand list of the assignment window.  
* Close the assignment window.  

Assigning multiple users to a user group

* Go to :menuselection:`Administer Users --> User Groups`.
* Select the desired user group from the user group list.
* Click on :guilabel:`Assign Users` in the :guilabel:`Main` tab.
* Drag and drop the user into the right-hand list of the assignment window.
  Hold down the Ctrl key to select multiple users.
* Close the assignment window.

If users belong to the user groups \"Price A\", \"Price B\" or \"Price C\", you will also need to enter alternative prices for all products. If this is not the case, €0.00 will be displayed instead. A global setting ensures that the regular price will be displayed if alternative prices for a product are not available. Go to :menuselection:`Master Settings --> Core Settings --> Settings` and open the :guilabel:`Products` section. Check the box :guilabel:`Use standard Product Price if no A/B/C Price is set` and click on :guilabel:`Save`.

.. seealso:: :doc:`Products - Main tab <../products/main-tab>` | :doc:`Users - Main tab <../../operation/users/main-tab>` | :doc:`User groups - Main tab <../../operation/user-groups/main-tab>`

.. Intern: oxbafk, Status: