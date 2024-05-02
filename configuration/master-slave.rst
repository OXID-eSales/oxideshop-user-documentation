Master/slave
============

The shop can be operated with several databases. One database is the master database that mainly handles write accesses. Slave databases contain mirrored data and handle read accesses. Based on this fundamental distinction, database accesses are distributed to the master database and to the slave databases by a load balancer.

Configuration
-------------
Master/slave is enabled by making an entry in :file:`config.inc.php`.

.. code:: php

   $this->aSlaveHosts = null;

In this entry, all server addresses of the slave databases are specified as an array. The example uses two slave databases.

.. code:: php

   $this->aSlaveHosts = array('slave1host', '10.2.3.12');

.. Intern: oxbaca, Status: