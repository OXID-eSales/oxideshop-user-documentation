Images
======

Each product can have up to twelve product images that are displayed in the product’s detailed view. Products have zoom images that are also available on the product’s details page. Smaller product images show the product in product lists, product boxes and in the shopping cart. All required image types are generated automatically.

Information on image generation and the directory structure of product images starting with OXID eShop 4.5.1 and newer versions can be found in the English-language tutorial `Image handling changes <https://oxidforge.org/en/image-handling-changes-since-version-4-5-1.html>`_ on the OXIDforge page.

Image generation and quality
----------------------------
The settings required for image generation and image sizes for all products can be found in the Admin panel. Go to :menuselection:`Master Settings --> Core Settings`, :guilabel:`Settings` tab and click on :guilabel:`Pictures` to view the settings. The first setting is “Installed GDLib Version”, a server software for the dynamic generation of graphics. Version 2 is the latest version. You can also see that the automatic generation of icons is activated. Leave these settings unchanged.

There is also a small :guilabel:`Pictures` section in the :guilabel:`System` tab. Specifying the image quality is important for image generation. The default setting is 75, which is a good compromise between the image quality and the file size. At a much smaller value, product images will be highly compressed, having a small file size but a poor image quality (blurring and compression artefacts). If the value is greater than 75, the image quality will increase, but the file size will also (longer loading times).

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