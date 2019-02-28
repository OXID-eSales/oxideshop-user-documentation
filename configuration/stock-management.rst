Stock management
================

The management of product stocks is integrated in OXID eShop. This way, the customer can be informed about a product’s availability. There are three different statuses to indicate a product’s availability: many, few, or out of stock. The status is indicated by a coloured symbol and a note text in the product details.

Products with sufficiently large quantities
-------------------------------------------
A green symbol and the :guilabel:`Ready for shipping` default text below the price indicate sufficient stock.

Low volume products
-------------------
The symbol below the price turns orange. The default text :guilabel:`Only some items on stock - order quickly!` will be displayed.

Out of stock products
---------------------
A red symbol and the notice text :guilabel:`This item is not on stock and has to be re-ordered` indicate that the product is sold out.

Before you can use the stock management feature, you will need to activate it. To do this, go to :menuselection:`Master Settings --> Core Settings`,:guilabel:` Settings` tab and click on :guilabel:`Stock` to view the settings.

The :guilabel:`Activate Stock Management` box is checked by default. With each order, the quantity of a product will be reduced and the stock status updated. If stock management is deactivated, a green symbol will always be displayed in the product details.

Additional settings are available for active stock management.

:guilabel:`Allow negative Stock Values` |br|
This setting is only relevant if you are sourcing the products from an external stock. If this setting is selected, negative stock levels will be calculated when additional items are ordered. If this setting is not selected, a product’s stock level will never fall below 0. This is also true if the product is sold out and further items have been ordered.

:guilabel:`Stock Level at which Users are informed that only a few products remain in Stock` |br|
Enter a quantity at which a low stock level should be displayed.

:guilabel:`Use default \"in-stock\" Message` |br|
If this setting is selected, :guilabel:`Ready for shipping` will be displayed as the default message. This message is always displayed if no specific message for a product’s stock status has been entered. You can define a message different from the default message for every product.

:guilabel:`Use default \"out-of-stock\" Message` |br|
Here, too, the default message is used if no other message has been defined for a product. If this box checked, :guilabel:`This item is not on stock and has to be re-ordered` will be displayed as the default message.

Save your settings.

.. Intern: oxbaaw, Status: