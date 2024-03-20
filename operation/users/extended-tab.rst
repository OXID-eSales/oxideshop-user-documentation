Extended tab
============

The :guilabel:`Extended` tab allows you to store additional information about the user. In addition, the user’s billing address is displayed. The billing address can only be changed in the Main tab.

.. image:: ../../media/screenshots/oxbads01.png
   :alt: Users - Extended tab
   :height: 343
   :width: 650

:guilabel:`Evening Phone`
   Phone number to reach the customer privately.

:guilabel:`Cellular Phone`
   Customer’s cell phone number.

:guilabel:`Newsletter`
   If customers want to receive newsletters from the shop, they can choose this option when buying a product or registering in the shop.

   This box will be checked after the customer clicks on a confirmation link received by e-mail and activates the newsletter via the so-called double opt-in.

   The email address stored in the :guilabel:`Main` tab is used for the newsletter.

   Shop owners can use this checkbox to change newsletter subscription settings if needed.

   This function will also be disabled if the customer cancels the subscription.

:guilabel:`Email adr. is invalid`
   If the customer has entered his e-mail address incorrectly when buying a product or registering in the shop, the shop owner can deactivate the sending of the newsletter here.

   This means that the customer data is no longer included in the .csv file, which can be exported for a newsletter mailing.

   The indicated e-mail address will still be used for other e-mails, such as shipping confirmation.

:guilabel:`Credit Rating`
   This value represents the customer’s creditworthiness and determines what payment methods he/she can use in the shop.

   This allows the shop owner to specify that only certain customers can use payment methods, such as invoice or direct debit.

   By default, users are created with a credit rating of 1000.

:guilabel:`URL`
   This field can be used to store a web address, such as a business customer's web page, a private web page or a blog.

.. todo: Zu klären ob obsolet: OXDEV-7965, evtl. reaktivieren
    :guilabel:`Credit points`
       Users can earn bonus points for bringing customers to the shop.
       Newly recruited customers can also receive bonus points when they register in the shop.
       You will need to first activate this function in :menuselection:`Master Settings --> Core Settings`, the :guilabel:`Settings` tab, under :guilabel:`Invitations`.
       This is where you can also specify the number of bonus points for inviting new customers and for registering in the shop.
       The shop owner determines how to use the users’ bonus points in the context of his/her business model.


.. Intern: oxbads, Status: transL, F1: user_extend.html