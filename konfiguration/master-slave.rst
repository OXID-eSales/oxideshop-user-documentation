Master/Slave
============
Mit der Version 5.0 wurde die Skalierbarkeit des OXID eShop Enterprise Edition vergrößert. Der Shop kann nun mit mehreren Datenbanken betrieben werden. Dabei ist eine Datenbank die Master-Datenbank, die hauptsächlich Schreibzugriffe verarbeitet. Die Slave-Datenbanken enthalten gespiegelte Daten und bedienen die Lesezugriffe. Ein Load-Balancer verteilt die Datenbankzugriffe nach dieser grundsätzlichen Unterscheidung auf die Master-Datenbank und auf die Slave-Datenbanken.

Konfiguration
-------------
Master/Slave wird über zwei Einträge in der :file:`config.inc.php` aktiviert und konfiguriert.

.. code:: php

   $this->aSlaveHosts = null;
   $this->iMasterSlaveBalance = 0;

Im ersten Eintrag werden alle Server-Adressen der Slave-Datenbanken als Array angegeben. Soll die Balance zwischen Master und Slave genutzt werden, muss auch der Hostname oder die IP des Servers mit der Master-Datenbank im Array stehen.

Der zweite Eintrag definiert die Balance zwischen Master/Slave mit einem Wert zwischen 0 und 100. Der Wert 0 bedeutet, dass die Slave-Datenbanken alle SELECT-Abfragen bearbeiten. Wird der Wert auf 100 gesetzt, übernimmt die Master-Datenbank komplett alle SELECT-Abfragen. Im Beispiel werden zwei Slave-Datenbanken verwendet. Die Datenbankanfragen werden zu 50% auf die Master-Datenbank und zu 50% auf die Slave-Datenbanken verteilt.

.. code:: php

   $this->aSlaveHosts = array('slave1host', '10.2.3.12', 'masterhost');
   $this->iMasterSlaveBalance = 50;

Master/Slave im Quellcode
-------------------------
Die nachfolgend genannten Methoden aus der Klasse oxLegacyDb, welche Daten selektieren, haben einen zusätzlichen Parameter $blType. Mit diesem kann angegeben werden, ob die Daten aus der Master- oder der Slave-Datenbank gelesen werden sollen. Der Standardwert ist\"true\"und bewirkt, dass alle Daten aus der Slave-Datenbank kommen. Methoden: getOne(), getArray(), getRow(), getAll(), select(), getAssoc(), getCol() und selectLimit().

Das Beispiel zeigt, wie Daten aus der Slave-Datenbank und aus der Master-Datenbank gelesen werden. Wenn Master/Slave nicht eingerichtet ist, werden die Daten in beiden Fällen aus der Master-Datenbank gelesen.

.. code:: php

   $oDb = oxDb::getDb();

   // from slave
   $oDb--> getOne(\"select oxid from oxcountry\");

   // from master
   $oDb--> getOne(\"select oxid from oxcountry\", false, false );

.. Intern: oxaaca, Status: