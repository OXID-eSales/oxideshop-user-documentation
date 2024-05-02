Memcached
=========

To use Memcached for caching OXID eShop, you will need to install the system on a separate server. Another requirement is that an additional license key for the high load option has been purchased and activated in the shop.

As soon as Memcached is recognised by OXID eShop, it can be selected in the Admin panel under :menuselection:`Master Settings --> Core Settings --> Cache` as :guilabel:`Cache connector`.

Installation
------------
Install Memcached on a server. The software can be found on the manufacturer's website: `http://memcached.org <http://memcached.org/>`_. Installation instructions and further information about Memcached can be found in the PHP manual: `http://php.net/manual/en/book.memcached.php <http://php.net/manual/en/book.memcached.php>`_ .

Make sure that the PHP library, \"memcached\" is active.


.. Intern: oxbacc, Status: