Emails
=======

OXID eShop sends different types of emails. After placing an order, customers will receive an email with the order summary. They will also receive an email when they register in your OXID eShop. As the shop owner, you can send out newsletters to tell your customers about the latest news.

To ensure the proper sending of emails, you will need to enter the correct SMTP data and set up the email addresses. The required settings can be found in the :guilabel:`Main` tab under :menuselection:`Master Settings --> Core Settings`.

Emails are usually sent via a separate mail server. If you have an in-house server that is used for sending emails through the shop, you will need the server login data. Enter the login data in the :guilabel:`SMTP Server`, :guilabel:`SMTP User` and :guilabel:`SMTP Password` fields. Your hosting package contains the SMTP data from your OXID Hosting Partner or Internet Service Provider (ISP). Emails are often sent directly via the server where your shop is installed with PHP. In this case, use the \"localhost\" entry for the SMTP server.

Now, you will need to define the email addresses to which the emails from the shop should be sent. These email addresses must be set up on your mail server or in the email configuration of your hosting package.

:guilabel:`Info e-mail Address` |br|
Whenever customers send a message via the contact form, an email is sent to the email address entered here. Good email addresses would be, for example, info@yourshopurl.com or contact@yourshopurl.com.

:guilabel:`Order e-mail reply` |br|
After placing an order through your shop, the customer receives an email with the order summary. The customer might reply to this email if, for example, he/she has a question or comment about the order. The customer’s reply will be sent to the email address entered here.

:guilabel:`Order e-mails to` |br|
Whenever a customer places an order through your shop, an email is also sent to the shop owner. The shop owner will receive a message about the order to the email address entered here.

The shop sends a number of emails to customers. Apart from the order confirmation, these are emails to confirm registration, change the password and inform that the order has been shipped. You can specify a separate subject line for these emails. The subject briefly summarises the content of the email. If your products are shipped to different countries, the subject line can also be written in several languages. You can switch between the available languages by using the selection list.

:guilabel:`Order e-mail Subject` |br|
Subject line of the email that customers receive when they place an order through your shop.

:guilabel:`Registration e-mail Subject` |br|
Subject line of the email that customers receive when they register in your shop.

:guilabel:`Forgot Password? e-mail Subject` |br|
If a customer has forgotten their password, they can use the \"Forgot your password?\" function to have an email sent to them so they can change the password. The subject of this email can be specified here.

:guilabel:`Shipped now e-mail Subject` |br|
Once the products have been sent to the customer, the order can be marked as sent in the Admin panel. As an option, the customer can be informed via email. The subject line for this email can be defined here.

Click on :guilabel:`Save`. The emails will now be sent with an individual subject line, but they will still contain the default text. Go to Section \"CMS\" to learn how to customise the default text for these emails.

.. Intern: oxbaav, Status: