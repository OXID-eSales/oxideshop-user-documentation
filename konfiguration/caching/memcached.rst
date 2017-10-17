Memcached
=========
Damit Memcached für das Caching des OXID eShop eingesetzt werden kann, muss das System auf einem separaten Server installiert werden. Sobald Memcached vom OXID eShop erkannt wird, kann es im Administrationsbereich unter :menuselection:`Stammdaten --> Grundeinstellungen --> Cache` als :guilabel:`Cache Connector` ausgewählt werden.

Installation
------------
Installieren Sie Memcached auf einem Server. Die Software erhalten Sie auf der Website des Herstellers: `http://memcached.org <http://memcached.org/>`_ . Eine Anleitung zur Installation finden Sie hier: `http://code.google.com/p/memcached/wiki/NewStart <http://code.google.com/p/memcached/wiki/NewStart>`_ . Weiterführende Hinweise zu Memcached erhalten Sie auch im PHP Manual: `http://php.net/manual/en/book.memcached.php <http://php.net/manual/en/book.memcached.php>`_ .

Stellen Sie sicher, dass die PHP-Bibliothek \"php5-memcached\" aktiv ist.

.. Intern: oxbacc, Status: