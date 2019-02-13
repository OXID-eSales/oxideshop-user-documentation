Rights and roles
=================

One of the features of Enterprise Edition is rights and roles management. Rights and roles allow you to control access to the elements to be displayed and available functions of OXID eShop for individual users and user groups.

There is a distinction between the rights and the roles for the actual shop, here also referred to as front end, and the Admin panel, the so-called back end. In this document, front and back end are used as terms to clarify the various aspects of rights and roles management.

Rights regulate access to certain functions, such as access to products and categories or the display of certain areas of the product’s details page. Multiple rights can be grouped together in roles and assigned to users and user groups.

Rights and roles for the shop (front end)
-----------------------------------------
Different permissions can be granted for the shop. This can be defined in the products’ and categories’ management section in the Admin panel as well as under :menuselection:`Administer Users --> Shop Roles`.

Displaying products and categories
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
You can choose to allow only certain user groups to see selected products and categories. This can be defined in the :guilabel:`Rights` tab of products and categories by assigning one or more user groups. This is an exclusive right. This means that only users who belong to the assigned user groups will be able to see the respective products and categories after logging into the shop. All other users and user groups will never be able to see these parts of the product catalogue.

Buying products and categories
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
You can also define specific user groups that will be able to buy certain products and categories. This can also be done by assigning the respective user groups in the :guilabel:`Rights` tab of products or categories. The screenshot shows that unauthorised users don’t have the option of adding, for example, kites to the shopping cart in the product overview. By clicking on :guilabel:`More information`, they can only open the product’s details page.

.. image:: ../media/screenshots/oxbaev01.png
   :alt: Product overview (rights and roles)
   :class: with-shadow
   :height: 360
   :width: 650

The :guilabel:`To cart` button also doesn’t display in the detailed view, as long as the customer is not logged in to the shop and belongs to the authorised user group.

.. image:: ../media/screenshots/oxbaev02.png
   :alt: Product detailed view (rights and roles)
   :class: with-shadow
   :height: 307
   :width: 609

Access to functions and areas of the details page
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Rights and roles can also be assigned for the entire product catalogue. The shop comes with the following rights that can be combined into roles and assigned to the desired user groups:

* Add product to shopping cart (TOBASKET)
* Show product price (SHOWARTICLEPRICE)
* Show product’s short description (SHOWSHORTDESCRIPTION)
* Show product’s long description (SHOWLONGDESCRIPTION)

These rights and roles can be defined under :menuselection:`Administer Users --> Shop Roles`. You can combine different rights combinations in roles and assign them to user groups. Once a right has been granted for one user group, this right will no longer apply to all other user groups. You can also define your own rights based on view classes and their methods. Rights-based display can be implemented in templates using an assigned ident.

.. image:: ../media/screenshots/oxbaev03.png
   :alt: Rights for detailed view (rights and roles)
   :class: with-shadow
   :height: 158
   :width: 319

As you can see in the screenshot, prices are not displayed for unauthorised users on the details page and in the product overview.

.. image:: ../media/screenshots/oxbaev04.png
   :alt: Product detailed view (rights and roles)
   :class: with-shadow
   :height: 310
   :width: 612

Rights and roles for the Admin panel (back end)
----------------------------------------------------------
Roles can also be defined for the Admin panel to represent the various responsibilities in the administration of OXID eShop.

Access to menus, submenus and tabs
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The roles allow you to define access to menus and submenus of the navigation panel as well as to individual tabs of the input area. This will give each editor his/her own custom Admin panel. These rights and roles can be defined and assigned to the respective users under :menuselection:`Administer Users --> Admin Roles`.

.. image:: ../media/screenshots/oxbaev05.png
   :alt: Access in the Admin panel
   :class: with-shadow
   :height: 335
   :width: 650

Access to products and categories
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The rights can be defined very differently for the editing of products and categories. For example, they regulate the creation, modification and deletion of products and categories as a whole and, if necessary, access to each control element (field, check box, or option) of the respective input area.

.. image:: ../media/screenshots/oxbaev06.png
   :alt: Access in the Admin panel
   :class: with-shadow
   :height: 335
   :width: 650

.. Intern: oxbaev, Status: