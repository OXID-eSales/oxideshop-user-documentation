SEO settings
============

Customers often start searching for products by entering queries in search engines and portals. To make sure that they find your shop, products and special offers, you will need to optimise and index the relevant information. Search Engine Optimisation (SEO) is supported in OXID eShop starting with version 4. SEO implementation automatically generates “speaking URLs” for categories and products, taking into consideration reserved words and special characters as well as different shop’s languages.

Shop owners only need to change a few settings to specify content for SEO. These are the page title, the structure of the URLs and the so-called metadata. The content can be defined in any shop’s language.

Page title
----------
The page title is displayed in the title bar of some browsers and is used as a bookmark or favourite when saving a page. Although the page title in the shop is almost invisible, it plays an important role in search engines. Search engines extract information from the page title indicating which content can be found on a website. Except for the shop's start page, page titles are automatically generated from the title of a product or category and are extended with a prefix and a suffix.

Example of a page title structure: OXID Surf and Kite Shop | Transportcontainer THE BARREL | purchase online

The settings for the page title can be found under :menuselection:`Master Settings --> Core Settings --> SEO`. Make sure to select the desired language.

:guilabel:`Title Prefix` |br|
Text placed before the generated part of the page title. It is best to enter your shop’s name here. Demoshop example: OXID Surf and Kite Shop

:guilabel:`Title Suffix` |br|
Text attached to the generated part of the page title. Here, you can add the characteristics for all the shop pages. Demoshop example: purchase online

:guilabel:`Front Page Title` |br|
You can specify the title text for the start page. It should precisely describe your online shop offer. Unlike other pages, the start page title consists of a prefix and a defined text, without using the suffix. Demoshop example: OXID Surf and Kite Shop | Online Shop for water sports and summertime

URL structure
-------------
The so-called “speaking URLs” are also an important part of SEO. Instead of displaying URLs with parameters and cryptic values, the URL is rewritten to show the name of the category and the product instead. This is good for search engines and visitors of your online shop.

Example of internally used URL: ``www.yourshopurl.com/index.php?`` |br|
``cl=details\&anid=f4f73033cf5045525644042325355732\&cnid=fadcb6dd70b9f6248efa425bd159684e``

Example of rewritten speaking URL: ``www.yourshopurl.com/offers/transport-container-THE-BARREL.html``

Just like the specifications for the page title, those for the URLs are language-dependent. Make sure to select the desired language.

:guilabel:`Default language for SEO URLs` |br|
Language codes (de, en, etc.) are not used in the URLs for the default language set here. The corresponding language codes will be added to the URLs of the other languages.

:guilabel:`SEO IDs Separator (e.g.\"+\",\"-\")` |br|
The separator is used when category or product titles consist of several words. It is inserted in the URL instead of a space. The hyphen is used as the default separator.

Example: ``www.yourshopurl.com/multiple-word-category/multiple-word-product.html``.

:guilabel:`SEO Suffix for differing Similar SEO URLs` |br|
If several products have the same title and belong to the same category, they would be assigned the same URL. The SEO suffix is attached to prevent this from happening and to avoid using the same URLs. If you don’t specify a SEO suffix, ``-oxid`` will be used by default.

:guilabel:`Characters that will be replaced in SEO URLs` |br|
Certain special characters such as umlauts (Ä, Ö, Ü) should not be used in URLs as they can cause problems. Enter the characters replacing the special characters in the input field. The syntax is as follows: special character =\> replacement character, for example Ü =\> Ue. Replacement characters are already set for the German language. If you want to enter or add special characters and replacement characters, for example, for a new language, you will need to use a separate line for each.

.. hint:: Starting with shop version 4.7.0/5.0.0, the list of characters to be replaced in the URL by other characters (transliteration) is defined in the :file:`/application/translation/{local}/translit_lang.php` file. The input area in the :guilabel:`SEO` tab has been removed.

:guilabel:`Reserved Words (are automatically suffixed)` |br|
Certain URLs are specified in eShop, for example ``www.yourshopurl.com/admin``, for opening the Admin panel. A category named \"admin\" would also have the URL ``www.yourshopurl.com/admin``, and you wouldn’t be able to open it. That's why the SEO suffix is automatically appended to such URLs. By default, OXID eShop treats all shop’s directories – even the added ones – as reserved words. You can enter additional reserved words in the input field.

:guilabel:`Words which are ignored in automatic Creation of Meta-tags` |br|
If products or categories don’t have their own meta tags, this information will be generated from the description. Words without any information value should be omitted. All words listed in the input field are ignored during automatic generation.

:guilabel:`Static URLs` |br|
Static URLs are defined for specific pages, such as Contacts and Newsletters. These replace the internal URLs with different parameters. You can create new static URLs or change the existing ones, even in different languages.

Metadata
--------
Although metadata is no longer critical for search engines, there is a way to change its content. There is metadata for the start page and metadata for products and categories. These are phrases and terms that are provided as a description or keywords with the respective page.

Demoshop example:

.. code:: html

   <meta name="description "content=\"All about water sports, sportswear and fashion. Comprehensive product range with the latest trending products. Fast shipping.">
   <meta name="keywords "content="kite, kites, kiteboarding, kiteboards, wakeboarding, wakeboards, boards, beach, summer, water sports, fashion, style, shirts, jeans, accessories, offers">

Start page
^^^^^^^^^^
The metadata for the shop’s start page can be entered under :menuselection:`Customer Info --> CMS Pages`. The CMS page “META description start page” (ID: oxstartmetakeywords) includes the shop description and the CMS page “META keywords start page” (oxstartmetadescription) includes the keywords.

Categories and products
^^^^^^^^^^^^^^^^^^^^^^^
Metadata for categories and products is automatically generated from their description. It can be overwritten by self-penned descriptions and keywords for each category or product. Metadata is entered in the :guilabel:`SEO` tab of the Categories or Products sections.

.. Intern: oxbabi, Status: