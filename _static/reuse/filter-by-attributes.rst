To enable the filtering of products, display a drop-down list of all values of the attribute in the category overview of the store (:ref:`oxbaff02`, item 1).

|procedure|

1. If you use multiple filters, consider the order of the filters to be applied.

   The correct order of the filters is crucial, as it narrows down the product selection step by step and thus optimizes the selection process.

   Let's assume your target group consists of benefit-oriented buyers.

   For motor vehicles, a sensible order of filters from the most important to the less important criteria could be as follows: Vehicle type (e.g. commercial vehicle or passenger car), body type, fuel type and finally color. This allows the customer to find a suitable vehicle.

#. Under :menuselection:`Administer Products --> Attributes`, choose the first attribute that you want to display as a filter.
#. On the :guilabel:`Category` tab, choose the :guilabel:`Assign Categories` button and assign the product category.
#. Under :menuselection:`Administer Products --> Products`, do the following for each article in the category:

   a. On the :guilabel:`Selection` tab, choose the :guilabel:`Assign Attributes` button.
   #. Choose the attribute.

      An input field for the value appears (:ref:`oxbaff04`, item 3).

   #. Enter the value and save your entry.

#. Repeat steps 2 to 4 for all other attributes that you want to use for filtering.

   Would you like to change the order of the filters?

   a. Remove the filter by unassigning the category:

      i. Under :menuselection:`Administer Products --> Attributes`, Choose the attribute.
      ii. On the :guilabel:`Category` tab, choose the :guilabel:`Assign Categories` button and remove the assignment.

   b. Add the assignment to the category again.

      The filter is added again at the end of the sequence.

#. If you operate your OXID eShop in multiple languages, make sure that the filters are available in all languages.

   a. Choose :menuselection:`Administer Products --> Products`.
   #. Choose the language.
   #. Choose the article.
   #. On the :guilabel:`Selection` tab, choose the :guilabel:`Assign Attributes` button.
   #. Assign each attribute a value in the corresponding language (for example \“Size = large\”).

|result|

In the category overview, your customers will find the corresponding filter(s) (:ref:`oxbaff02`, item 1).

.. _oxbaff02:

.. figure:: ../../media/screenshots/oxbaff02.png
   :alt: Displaying filters with attribute values
   :width: 650
   :class: with-shadow

   Fig.: Displaying filters with attribute values