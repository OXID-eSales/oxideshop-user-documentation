SEO tab
=======

.. todo: SB: still valid for now

Use the :guilabel:`SEO` tab (:ref:`oxbagd01`) to improve the visibility of manufacturer pages in search engines.

* Assign a readable :guilabel:`SEO URL` so users can find the page more easily.
* Define a clear meta title and a meaningful :guilabel:`META Description` to increase click-through rates in search results.
* Add relevant :guilabel:`META Keywords` to help the page appear for relevant search queries.
* Check :guilabel:`Fixed URL` to prevent automatic changes and avoid duplicate content.
* Use the language selector to manage SEO settings individually for each activated language.

.. _oxbagd01:

.. figure:: ../../media/screenshots/oxbagd01.png
   :alt: Manufacturers – SEO tab
   :width: 650
   :class: with-shadow

   Fig.: Manufacturers – SEO tab

Use the language switcher at the bottom of the input area to edit SEO settings for additional active languages.

:guilabel:`Fixed URL`
   By default, the shop automatically updates the SEO URL when the manufacturer’s title changes.

   Check this box to keep the current SEO URL unchanged and avoid unintended changes.

:guilabel:`Show SEO Suffix in Category`
   Enable this option to include the title suffix in the page title.

   When customers open the product overview for a brand, the page title will include the suffix defined under :menuselection:`Master Settings --> Core Settings --> SEO --> Title Suffix`.

   Example from the demo shop: ``online kaufen``
   Title: ``OXID eShop | Imperial | online kaufen`` (:ref:`oxbagd02`, Pos. 1)

.. _oxbagd02:

.. figure:: ../../media/screenshots/oxbagd02.png
   :alt: Displaying title suffix (example: manufacturer)
   :width: 650
   :class: with-shadow

   Fig.: Displaying title suffix (example: manufacturer)

   For more information, see :doc:`SEO settings <../../configuration/seo-settings>`.

:guilabel:`SEO URL`
   Enter a friendly SEO URL or edit the automatically generated one.

   Optionally, check :guilabel:`Fixed URL` to prevent future changes.

:guilabel:`META Keywords`
   Enter relevant keywords that will be included as meta tags in the HTML source code.

   If left empty, the shop generates keywords automatically—for example, based on the manufacturer title, the "By Manufacturer" category, and search terms of assigned products.

:guilabel:`META Description`
   Enter the meta description for search engines. This text often appears in search results.

   If you leave it empty, the shop creates a description automatically—for example, from the manufacturer title, category, and assigned product titles.

:guilabel:`In Language`
   Choose the language in which you want to edit the SEO metadata.

.. Intern: oxbagd, Status:, F1: manufacturer_seo.html
