Images
======

Assign up to twelve product images to products, which are displayed in the detailed view of the product.

Items have zoom images that can also be called up on the detail page. Specify globally or at category level or for individual products which type of zoom you want to use.

Smaller item images show the item in the item lists, in product boxes and in the shopping cart. All required image types are generated automatically. To optimize page load speed and user experience, specify the maximum image size and image quality.

Specify whether order confirmations should be sent with images.

Specifying image generation and quality
---------------------------------------

The required settings for image generation and image sizes are made for all products in the administration area.

Displaying basic settings
^^^^^^^^^^^^^^^^^^^^^^^^^

If required, check the version of the software that is responsible for the dynamic creation of images.

|procedure|

1. Under :menuselection:`Master Settings --> Core Settings`, choose the :guilabel:`Settings` tab.
#. Choose :guilabel:`Pictures`.

   * Check the version of GDLib, the software on the server that generates graphics dynamically.
   * Check whether the automatic generation of icons is activated.

   Leave both settings unchanged.

Specifying the image quality
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If required, increase the speed at which pages are loaded in the browser.

|procedure|

1. Under :menuselection:`Master Settings --> Core Settings`, choose the :guilabel:`System` tab.
#. Choose the :guilabel:`Pictures` section.

   You have the following options:

   * :guilabel:`Picture Quality`: Specify the image quality when generating the images.

     The default setting is 75 and is a good compromise between image quality and file size.

     If the value is significantly lower, the product images are heavily compressed and therefore have a small file size, but poor image quality (blurring and compression artifacts).

     If the value is greater than 75, the image quality increases, but so does the size of the file (longer loading times).

   * :guilabel:`Automatically convert images to WebP format`: Increase the browser speed.

     To do so, automatically convert the images to WebP image format.

Sending order confirmations with pictures
-----------------------------------------

Decide whether order confirmations should include images.

|background|

E-mails with item images can quickly become large, which can lead to problems when sending and receiving the e-mails.

By default, e-mails are sent without item images.

The item images are loaded by the customer's mail program when the e-mail is read.

|procedure|

1. Under :menuselection:`Master Settings --> Core Settings`, choose the :guilabel:`System` tab.
#. Choose the :guilabel:`Pictures` section.
#. To send product images in the order confirmation, activate the :guilabel:`Send e-mails with inline Images` checkbox.


Optimizing image sizes
----------------------

To optimize the speed at which pages are loaded, set the smallest possible image sizes. Your images are then scaled down to this maximum image size before loading by the browser.

The actual :emphasis:` displayed` size of the images for products and categories as well as the manufacturer and brand logos depends on the design of your OXID eShop. You define these values with your CSS.

|example|

In our demo store, the images for displaying subcategories (:ref:`oxbaaz03a`) are downsized to a size of 400x300 pixels (:ref:`oxbaaz04`, item 1). This is the size that the browser would download on the end device.

.. _oxbaaz04:

.. figure:: ../media/screenshots/oxbaaz04.png
   :alt: Example: Set maximum image size to 400x300 pixels
   :width: 650
   :class: with-shadow

   Fig.: Example: Set maximum image size 400x300 pixels

The stylesheet in turn reduces the image to 62x62 pixels. This is the actual displayed (rendered) size compared to the intrinsic size of the image downloaded by the browser (:ref:`oxbaaz05`, item 1).

The displayed intrinsic size of 300 x 300 pixels differs from the maximum size because it is a square image. In this case, the system uses the smallest side length as a basis, i.e. 300 pixels in this example.

.. _oxbaaz05:

.. figure:: ../media/screenshots/oxbaaz05.png
   :alt: Rendered image size 62x62 pixels in the stylesheet
   :width: 650
   :class: with-shadow

   Fig.: Rendered image size 62x62 pixels in the stylesheet

|procedure|

1. Under :menuselection:`Extensions --> Themes`, choose the theme.
#. Choose the :guilabel:`Settings` tab and choose :guilabel:`Images`.

   You have the following options for adjusting the image sizes:

   * :guilabel:`Product picture size (width*height)`

     Product image that is displayed on the detail page.

     Define the maximum size of up to 12 product images.

     This allows product images of different sizes.

     For each product image there is a line at the beginning of which is ``oxpic`` and a number. ``oxpic1`` stands for the first product picture, ``oxpic2`` for the second product picture and so on.

     .. hint:: Use different image sizes with caution.

        Product images of different sizes could possibly lead to a rather unprofessional-looking presentation of the products.

   * :guilabel:`Size of a subcategory's picture (width*height)`.

     Image for displaying subcategories in the category overview.

     Name of the function: ``category.getIconUrl``
     |br|
     Name of the parameter: ``CatIconsize``
     |br|
     Default size: 400 pixels wide and 300 pixels high.

     .. _oxbaaz03a:

     .. figure:: ../media/screenshots/oxbaaz03a.png
        :alt: Category image of a subcategory
        :width: 650
        :class: with-shadow

        Fig.: Category image of a subcategory

   * :guilabel:`Category picture size for promotion on startpage (width*height)`

     Image for displaying the category overview. This image type is currently not used, but is retained to ensure downward compatibility, to enable future use and to allow you to integrate it into your own templates if required.

     Name of the function: ``category.getPromotionIconUrl``
     |br|
     Name of the parameter: ``CatPromotionsize``
     |br|
     Default size: 370 pixels wide and 107 pixels high.

   * :guilabel:`Category picture size (width*height)`

     Image of the category that is advertised on the start page.

     This image type is not used in the current demo data. However, it is part of the APEX theme and can be used at any time (example: :ref:`oxbaaz03c`).

     Name of the function: ``category.getThumbUrl``
     |br|
     Name of the parameter: ``sCatThumbnailsize``
     |br|
     Default size: 1600 pixels wide and 500 pixels high.

     .. _oxbaaz03c:

     .. figure:: ../media/screenshots/oxbaaz03c.png
        :alt: Category image
        :width: 650
        :class: with-shadow

        Fig: Category picture

   * :guilabel:`Icon size (width*height)`

     Icons are the smallest product images. They are used

     * in the shopping cart preview (minibasket) (:ref:`oxbaaz03d`, item 1)
     * in the shopping cart (:ref:`oxbaaz03d`, item 2)
     * as an image switcher (:ref:`oxbaaz03d`, item 3)
     * as image switcher for the modal zoom (see :ref:`configuration/images:Choosing a zoom type`)
     * for the size of the gift box

     Name of the function: ``article.getIconUrl``
     |br|
     Name of the parameter: ``sIconsize``
     |br|
     Default size: 100 pixels wide and 100 pixels high.

     .. _oxbaaz03d:

     .. figure:: ../media/screenshots/oxbaaz03d.png
        :alt: Icon in various functions
        :width: 650
        :class: with-shadow

        Fig.: Icon in various functions

   * :guilabel:`Manufacturer's/brand logo size`

     Logo that is displayed

     * in the brand overview on the start page (:ref:`oxbaaz03e`, item 1)
     * in the product overview per manufacturer (:ref:`oxbaaz03e`, item 1)
     * on the product detail page (:ref:`oxbaaz03e`, item 1)

     Name of the function: ``vendor.getIconUrl``
     |br|
     Name of the parameter: ``ManufacturerIconsize``
     |br|
     Default size: 100 pixels wide and 100 pixels high.

     .. _oxbaaz03e:

     .. figure:: ../media/screenshots/oxbaaz03e.png
        :alt: Manufacturer/brand logo in various functions
        :width: 650
        :class: with-shadow

        Fig.: Manufacturer/brand logo in various functions

   * :guilabel:`Manufacturer's/brand picture size`

     This image type is currently not used, but is retained to ensure downward compatibility, to enable future use and to allow you to integrate it into your own templates if required.

     Name of the function: ``manufacturer.getPictureUrl``
     |br|
     Name of the parameter: ``ManufacturerPicturesize``
     |br|
     Default size: 1140 pixels wide and 1140 pixels high.

   * :guilabel:`Manufacturer promotion Icon picture size (width*height)`

     This image type is currently not used, but is retained to ensure downward compatibility, to enable future use and to allow you to integrate it into your own templates if required.

     Name of the function: ``manufacturer.getPromotionIconUrl``
     |br|
     Name of the parameter: ``ManufacturerPromotionsize``
     |br|
     Default size: 370 pixels wide and 107 pixels high

   * :guilabel:`Manufacturer's/brand thumbnail size`

     This image type is currently not used, but is retained to ensure backward compatibility, to enable future use and to allow you to integrate it into your own templates if required.

     Name of the function: ``manufacturer.getPromotionIconUrl``
     |br|
     Name of the parameter: ``ManufacturerThumbnailsize``
     |br|
     Default size: 370 pixels wide and 370 pixels high


   * :guilabel:`Thumbnail size (width*height)`

     Thumbnails are preview images and are displayed wherever products are listed, for example in

     * Product comparison pages
     * Item lists, such as category overviews and search results
     * Promotions (example: Just arrived!)

     They can appear in grid view (:ref:`oxbaaz03i`, item 1) or list view (:ref:`oxbaaz03i`, item 2).

     Name of the function: ``article.getThumbnailUrl``
     |br|
     Name of the parameter: ``Thumbnailsize``
     |br|
     Default size: 500 pixels wide and 500 pixels high.

     .. _oxbaaz03i:

     .. figure:: ../media/screenshots/oxbaaz03i.png
        :alt: Thumbnails in grid and list view
        :width: 650
        :class: with-shadow

        Fig.: Thumbnails in grid and list view

   * :guilabel:`Zoom picture size (width*height)`

     Enlarged display of modal product images that can be called up on the detail page.

     For more information, :ref:`configuration/images:Choosing a zoom type`.

     Name of the function: ``article.getZoomPictureUrl``
     |br|
     Name of the parameter: ``ZoomImageSize``
     |br|
     Default size: 1200 pixels wide and 1200 pixels high.

Choosing a zoom type
--------------------

Depending on the application and product, positively influence the willingness to buy by addressing different psychological needs of customers with one of three ways of enlarging images in the APEX theme.

* Hover zoom: This function offers an interactive way of viewing product images in detail.

  When the mouse pointer hovers over the image, it is enlarged and the magnification follows the mouse movement.

  Hover zoom is ideal for stores with a wide range of products where customers frequently switch between different products. The interactive nature of the hover zoom can improve the user experience and increase dwell time.

  Hover zoom encourages curiosity and engagement, which can lead to faster, emotionally driven purchase decisions.

* Modal zoom: Clicking on the product image opens it in a larger modal window, in which further details become visible.

  In addition, the user can zoom into the image again within the modal to see particularly fine details.

  This offers a comprehensive opportunity to take a close look at products.

  The modal zoom conveys trust and security, supports rational decisions and strengthens confidence in product quality.

* Magnifying glass zoom: A magnifying glass function is activated when the mouse pointer is moved over the image (:ref:`oxbaaz01`).

  A separate area shows a greatly enlarged view of the image section directly under the mouse pointer.

  This enables precise viewing of specific product details without having to enlarge the entire image.

  The magnifying zoom emphasizes precision and quality, which is particularly well received by customers who pay attention to details and specifications, and can thus strengthen confidence in specific product features.

  .. _oxbaaz01:

  .. figure:: ../media/screenshots/oxbaaz01.png
     :alt: Example: Magnifying glass zoom
     :width: 650
     :class: with-shadow

     Fig.: Example: Magnifying glass zoom

You can define the desired type of zoom globally for your eShop. In addition to this standard zoom, you can also set the three zoom options individually for each product.

Setting the zoom globally
^^^^^^^^^^^^^^^^^^^^^^^^^

Choose the type of zoom globally for your eShop.

|procedure|

1. Under :menuselection:`Extensions --> Themes`, choose the APEX theme.
#. On the :guilabel:`Settings` tab, expand the :guilabel:`Product detail page` area.
#. Under :guilabel:`Zoom type for product detail page` choose the desired zoom type.
#. Save your settings.

Specifying the zoom for individual products
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If required, assign an individual zoom option to individual products.

In addition to setting a standard image zoom option in the theme settings, you can use the three zoom options individually for each product.

This gives you greater flexibility for different products.

|procedure|

1. Under :menuselection:`Administer Products --> Products`, choose the product and choose the :guilabel:`Settings` tab.
#. Set the desired zoom by entering the path of the corresponding template in the :guilabel:`Alternative Template` input field (in our example, defining the magnifyer zoom type, :ref:`oxbaaz02`, Pos. 1).

   * Hover zoom: ``custom/hover_zoom.html.twig``
   * Modal zoom: ``custom/modal_zoom.html.twig``
   * Magnifier zoom: ``custom/magnifier_lens.html.twig``

   .. _oxbaaz02:

   .. figure:: ../media/screenshots/oxbaaz02.png
      :alt: Defining an alternative template for a product
      :width: 650
      :class: with-shadow

      Fig.: Defining an alternative template for a product

#. Save your settings.
#. Optional: To ensure the uniformity of the display, repeat the steps for all products in a category.

   Background: It is not possible to apply the zoom templates at category level.






.. todo: tbd: folgendes löschen:
    Each product can have up to twelve product images that are displayed in the product’s detailed view. Products have zoom images that are also available on the product’s details page. Smaller product images show the product in product lists, product boxes and in the shopping
    .. todo: #cart. All required image types are generated automatically.
    Information on image generation and the directory structure of product images starting with OXID eShop 4.5.1 and newer versions can be found in the English-language tutorial `Image handling changes <https://oxidforge.org/en/image-handling-changes-since-version-4-5-1.html>`_ on the OXIDforge page.
    Image generation and quality
    ----------------------------
    The settings required for image generation and image sizes for all products can be found in the Admin panel. Go to :menuselection:`Master Settings --> Core Settings`, :guilabel:`Settings` tab and click on :guilabel:`Pictures` to view the settings. The first setting is "Installed GDLib Version", a server software for the dynamic generation of graphics. Version 2 is the latest version. You can also see that the automatic generation of icons is activated. Leave these settings unchanged.
    On the :guilabel:`System` tab there is also a :guilabel:`Images` section. You have the following options there:
    |br|
    * :guilabel:`Image quality`: Specifying the image quality is important for the image generation.
      The default setting is 75 and represents a good compromise between image quality and file size.
      If the value is much smaller, the article images are heavily compressed and therefore have a small file size, but poor image quality (blurring and compression artifacts).
      If the value is greater than 75, the image quality increases, but so does the file size (longer loading times).
    * :guilabel:`Convert images automatically to WebP format`: Increase the browser speed.
      To do this, you can automatically convert the images to the WebP image format
    The option :guilabel:`Send e-mails with inline Images` has nothing to do with image generation. With this setting selected, product images will be sent in e-mails, which means that the e-mail that will be sent as order confirmation will contain product images. This will lead to larger e-mail sizes which may cause problems when sending and receiving e-mails. By default, e-mails are sent without product images. Product images will be downloaded by the customer's mail program upon reading the e-mail.
    Image sizes
    -----------
    The size of product and category images as well as manufacturer and brand logos depends on the design of the shop. For this reason, the settings are stored in the active theme under :menuselection:`Extensions --> Themes`. Go to the :guilabel:`Settings` tab of the \"Azure\" theme and click on :guilabel:`Images`.
    :guilabel:`Icon size (width*height)` |br|
    Icons are the smallest product images that are used in the shopping cart and product boxes (for example: Top of the Shop). Default size: 87 pixels wide and 87 pixels high.
    :guilabel:`Thumbnail size (width*height)` |br|
    Thumbnails are preview images that are displayed in product lists such as category overviews and search results as well as in special promotions (for example: Just arrived!). Default size: 185 pixels wide and 150 pixels high.
    :guilabel:`Category picture size (width*height)` |br|
    Image displayed in the category overview. Default size: 784 pixels wide and 150 pixels high.
    :guilabel:`Zoom picture size (zoom 1-4) in pixels (width*height)` |br|
    Enlarged view of a product image available on the product’s details page. Default size: 665 pixels wide and 665 pixels high.
    :guilabel:`Product picture size (picture 1-12) in pixels (width*height)` |br|
    Product image shown on the product’s details page. You can define the size of up to 12 product images, which means that you can have product images with different sizes. There is a line for each product image beginning with oxpic and a number. oxpic1 stands for the first product image, oxpic2 for the second product image, and so on. Default size: 380 pixels wide and 340 pixels high.
    .. hint::The option to specify different image sizes should be used with caution as different-sized product images may contribute to a rather unprofessional presentation of the products.
    :guilabel:`Manufacturer’s/brand logo size` |br|
    Logo displayed in the brand overview on the start page. Default size: 100 pixels wide and 100 pixels high.
    :guilabel:`Size of a subcategory’s picture (width*height)` |br|
    Images of the subcategories displayed in the category overview. Default size: 168 pixels wide and 100 pixels high.
    :guilabel:`Category picture size for promotion on start page (width*height)` |br|
    Image of the category promoted on the start page. Default size: 370 pixels wide and 107 pixels high.

.. Intern: oxbaaz, Status: