Master/Slave
============

Der Shop kann mit mehreren Datenbanken betrieben werden. Dabei ist eine Datenbank die Master-Datenbank, die hauptsächlich Schreibzugriffe verarbeitet. Die Slave-Datenbanken enthalten gespiegelte Daten und bedienen die Lesezugriffe. Ein Load-Balancer verteilt die Datenbankzugriffe nach dieser grundsätzlichen Unterscheidung auf die Master-Datenbank und auf die Slave-Datenbanken.

Konfiguration
-------------
Master/Slave wird über einen Eintrag in der :file:`config.inc.php` aktiviert.

.. code:: php

   $this->aSlaveHosts = null;

In diesem Eintrag werden alle Server-Adressen der Slave-Datenbanken als Array angegeben. Im Beispiel werden zwei Slave-Datenbanken verwendet.

.. code:: php

   $this->SlaveHosts = array('slave1host', '10.2.3.12');

.. Intern: oxbaca, Status: