Defining the Display Order of Products in Categories
====================================================

Define the order in which products are displayed within a category.

You can control the display order of products in categories in three different ways:

* **Automatic sorting** – Let the products be sorted automatically based on a selected field, such as title, price, or creation date, in ascending or descending order.
* **Manual sorting** – Arrange products in a specific order manually using the assignment window.
* **Customer-defined sorting** – Specify which sorting options are available to customers in the frontend, such as by price, rating, or article number.

Automatically sorting products
------------------------------

Select a sorting criterion, such as :guilabel:`Title`, :guilabel:`Price`, or :guilabel:`Date Created`, to automatically sort the products.

Define whether the products should be sorted in ascending or descending order based on that field.

|procedure|

1. Choose :menuselection:`Administer Products --> Categories`.
#. In the category list, select the desired category.
#. In the :guilabel:`Main` tab, open the dropdown list :guilabel:`Fast sorting`.
#. Select a sorting criterion for the quick sorting.
#. Choose :guilabel:`asc` or :guilabel:`desc` for ascending or descending order.
#. Save your settings.

Manually sorting products
-------------------------

Arrange the products of a category manually in a specific order.

|procedure|

1. Choose :menuselection:`Administer Products --> Categories`.
#. Select the desired category from the category list.
#. In the :guilabel:`Main` tab, make sure that the :guilabel:`Fast sorting` option is set to :guilabel:`no sorting`.
#. In the :guilabel:`Sorting` tab, choose the :guilabel:`Sort Categories` button.
#. Move the products into the desired order in the right-hand list of the assignment window.
#. Choose the button :guilabel:`Save new sorting`.

|result|

The left-hand list now shows the current sort order (:ref:`oxbafq01`, item 1). The :guilabel:`Position` column displays the values that determine the order.

.. _oxbafq01:

.. figure:: ../../media/screenshots/oxbafq01.png
   :alt: Manually defining the product order
   :width: 650
   :class: with-shadow

   Fig.: Manually defining the product order

Enabling customer-defined sorting
---------------------------------

Specify whether and how customers can sort the products within categories.

|procedure|

1. Choose :menuselection:`Master Settings --> Core Settings`.
#. In the :guilabel:`Settings` tab, go to the :guilabel:`Products` section.
#. Make sure the :guilabel:`Users can sort product lists` checkbox is selected (:ref:`oxbafq02`, item 1).
#. Define the fields used for sorting (:ref:`oxbafq02`, item 2).

   You can use the following options:

   * ``oxtitle``: Product title
   * ``oxprice``: Product price
   * ``oxvarminprice``: Lowest variant price (if variants with different prices are used)
   * ``oxartnum``: Article number
   * ``oxrating``: Product rating
   * ``oxstock``: Available stock

   Each field must be listed in a separate line.

   The sorting fields correspond to the database fields of the table ``oxarticles``.

   .. _oxbafq02:

   .. figure:: ../../media/screenshots/oxbafq02.png
      :alt: Configuring customer-defined sorting
      :width: 650
      :class: with-shadow

      Fig.: Configuring customer-defined sorting

#. Save your settings.

|result|

In our example, customers can now sort products not only by title and price, but also by article number (:ref:`oxbafq02`, item 3).

To achieve this, we added the field ``oxartnum`` to the default sorting fields ``oxtitle`` and ``oxvarminprice`` in the core settings (:ref:`oxbafq02`, item 2).

.. seealso:: :doc:`Categories - Main tab <../categories/main-tab>` | :doc:`Categories - Sorting tab <../categories/sorting-tab>`

.. Intern: oxbafq, Status:

