Caching
=======

Database table structures, contents of the language files used and templates compiled by the Smarty template engine are saved in all shop editions by default. Queries to the OXSEO database table are also written to files, if enabled in the performance settings, to avoid repeated database access. Files are saved in the shop’s :file:`/tmp` directory and its subdirectories, e.g. :file:`/tmp/smarty`. Caching allows the system to use the contents from the cache and send them to the inquiring web clients, whenever possible. This reduces database access and significantly reduces OXID eShop response times.

OXID eShop Enterprise Edition offers far more capabilities for caching.

Dynamic Content Cache has been an integral part of Enterprise Edition from the very beginning. It's a caching solution that caches the generated HTML pages, including their dynamic content. For this, the technical capabilities of the Zend Server or simply the file system of the server where the shop is running can be used. If a page is requested by the browser, the system will first check whether this page is still in the cache and still valid. The validity is determined by the set lifetime (TTL, Time To Live). If the page is in the cache and contains dynamic content, it will be reloaded and then the complete page will be sent to the browser. If the requested page is not in the cache, it will be created, displayed and cached.

Caching has been enhanced with Enterprise Edition version 5.0.0.

The new and enhanced caching is implemented using three main components: the Cache Manager integrated into OXID eShop, supported by the Varnish reverse proxy and/or Memcached.

The *Cache Manager*, which is a direct component of OXID eShop, processes all caching requirements and ensures that the data in the various caches used is always up-to-date.

The *Varnish reverse proxy* is a web accelerator. The system processes incoming enquiries from web clients before the web server and compiles the web pages to be delivered predominantly from the cached content. Contents are queried by the web server and read from the database as soon as the cache lifetime has expired.

*Memcached* is a cache server. It allows you to store the cache in the memory instead of in the file system. Access to data in the memory is much faster than access to the hard drive.

-----------------------------------------------------------------------------------------

Varnish reverse proxy
---------------------
**Contents**: Varnish, functionality, installation instructions, configuration, default.vcl, servers_conf.vcl, HTTP, HTTPS, SSL |br|
:doc:`Read article <varnish-reverse-proxy>` |link|

Memcached
---------
**Contents**: Memcached, installation instructions, configuration |br|
:doc:`Read article <memcached>` |link|

Caching settings
---------------------
**Contents**: default cache back end, cache lifetime (TTL), cache connector, file system, cache directory, Memcached, Memcached server, reverse proxy, cachable pages, dynamic content caching, cacheable classes |br|
:doc:`Read article <caching-settings>` |link|

.. note:: Additional links: Smarty Template Engine: `http://www.smarty.net <http://www.smarty.net/>`_ | Zend Server: `http://www.zend.com/en/products/zend_server <http://www.zend.com/en/products/zend_server>`_ | Varnish: `http://www.varnish-cache.org <http://www.varnish-cache.org/>`_ | Memcached: `http://memcached.org <http://memcached.org/>`_

.. Intern: oxbabz, Status: