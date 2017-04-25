Reverse Proxy Varnish
*********************
Funktionsweise
--------------
Varnish ist ein Reverse Proxy, der vor dem eigentlichen Webserver eingehende Anfragen von Web-Clients verarbeitet. Die Webseiten, welche an die Web-Clients ausgeliefert werden, werden zum größten Teil aus zwischengespeicherten Inhalten zusammengestellt. Erst wenn die Lebensdauer des Caches abgelaufen ist, fragt Varnish Inhalte vom Webserver ab. Der OXID eShop muss dann die angeforderten Daten aus der Datenbank lesen und bereitstellen.\

Die Verarbeitung durch Varnish basiert auf der Aufteilung der einzelnen Seiten des OXID eShop in kleine Teilbereiche, so genannte Widgets. Für Varnish werden diese Widgets als ESI-Tags gekennzeichnet. Dadurch kann Varnish dynamische Seitenbereiche, wie beispielsweise Warenkorb oder Login, separat abfragen und aktualisieren. Darüber hinaus werden Grafiken, Artikel- und Kategoriebilder, Stylesheet- und JavaScript-Dateien immer zwischengespeichert.

.. image:: ../../media/screenshots-de/oxbacb01.png
   :alt: Web-Clients, Varnish und Server mit OXID eShop
   :height: 204
   :width: 650

Um den Reverse Proxy Varnish für das Caching des OXID eShop nutzen zu können, muss Varnish auf einem separaten Server installiert und konfiguriert werden.

Installation
------------
Installieren Sie Varnish auf einem Server. Die Software und die Anleitung zur Installation erhalten Sie auf der Website des Herstellers: `http://www.varnish-cache.org <http://www.varnish-cache.org/>`_ .

Konfiguration
-------------
Varnish verfügt über eine eigene Sprache, mit welcher dessen Verhalten konfiguriert werden kann. Mit VCL (Varnish Configuration Language) definiert, wird die Konfiguration in Binärcode übersetzt und bei Anfragen aus dem Web ausgeführt. Die Standard-Konfigurationsdatei ist :file:`default.vcl` und befindet sich im Verzeichnis :file:`/etc/varnish`.

Wir haben die Konfigurationsdatei :file:`default.vcl` für das Caching des OXID eShop angepasst. Die Definitionen entsprechen einem Standard-Shop. Sie sollten nur bei einem stark angepassten Shop verändert werden. Das betrifft ausschließlich Veränderungen im Standardverhalten des Shops durch modulare Erweiterungen, beispielsweise komplett geänderter Umgang mit Artikeln oder Einsatz eigener Cookies. Die notwendigen Änderungen in der Konfigurationsdatei setzen profunde Kenntnisse der VCL voraus. Fehlerhafte Anweisungen können die Performance beeinträchtigen und den Shop Daten bereitstellen lassen, die nicht aktuell sind. Wird die Konfigurationsdatei unverändert in einem stark angepassten Shop verwendet, kann das zu Datenverlust und unerwartetem Verhalten führen.

Die Konfigurationsdatei :file:`servers_conf.vcl` enthält Hostnamen und IPs der beteiligten Server und muss an die reale Systemumgebung angepasst werden.

Varnish ab Version 4.0.3
++++++++++++++++++++++++
Varnish Version 3.0 wird nicht mehr länger unterstützt, da die Software bereits seit April 2015 den Status End Of Life (EOL) erreicht hat. Die jetzt ausgelieferte Datei :file:`default.vcl` enthält die Konfiguration für Varnish ab Version 4.0.3. Bitte setzen Sie nicht die Versionen 4.0.0, 4.0.1 und 4.0.2 ein, da diese Probleme in der Behandlung von Cookies hatten, die dazu führten, dass Artikel nicht in den Warenkorb gelegt und Kunden sich nicht an den Shop anmelden konnten.

Wenn dieses Verhalten in Ihrem Shop auftritt und Sie nicht auf die neueste Version von Varnish aktualisieren können, versuchen Sie den folgenden Workaround. Dieser wurde nicht explizit getestet, deshalb prüfen Sie das Verhalten des Shops gründlich, bevor die Änderung in die Produktivumgebung übernommen wird.

Ersetzen Sie in der Konfigurationsdatei :file:`default.vcl` die Zeile 463

``set beresp.http.Set-Cookie = regsuball(beresp.http.Set-Cookie,\"(, |^)[^@][^,|$]+\",\"\");``

durch diese Zeile

``set beresp.http.Set-Cookie = regsuball(beresp.http.Set-Cookie,\"(, |^)[^@]\",\"\");``

Download der Konfigurationsdateien
++++++++++++++++++++++++++++++++++
Die beiden Konfigurationsdateien :file:`default.vcl` und :file:`servers_conf.vcl` für die Konfiguration des Reverse Proxys können hier heruntergeladen werden. Markieren Sie dafür den Link mit der rechten Maustaste und speichern Sie die Datei lokal. Ein Klick mit der linken Maustaste öffnet die Konfigurationsdatei im Browser.

*  `default.vcl <https://support.oxid-esales.com/downloads/varnish/5.2.5/default.vcl>`_ 
* für Enterprise Edition ab 5.2.5 und Varnish ab 4.0.3
  Die Datei wurde am 26.01.2016 aktualisiert. Grund: kleine Korrekturen im Cookie-Handling.
*  `default.vcl <http://support.oxid-esales.com/downloads/varnish/5.2.0/default.vcl>`_ 
* für Enterprise Edition ab 5.2.0
*  `default.vcl <http://support.oxid-esales.com/downloads/varnish/5.1.0/default.vcl>`_ 
* für Enterprise Edition ab 5.1.0
*  `default.vcl <http://support.oxid-esales.com/downloads/varnish/5.0.9/default.vcl>`_ 
* für Enterprise Edition ab 5.0.9
*  `default.vcl <http://support.oxid-esales.com/downloads/varnish/5.0.2/default.vcl>`_ 
* für Enterprise Edition 5.0.2 - 5.0.8
* .. note:: Bitte beachten Sie die Release-Informationen zu
*  `OXID eShop 4.7.2/5.0.2 <de/support-services/dokumentation-und-hilfe/oxid-eshop/releases/releases-2012/oxid-eshop-472502.html>`_ 
*  `default.vcl <http://support.oxid-esales.com/downloads/varnish/5.0.0/default.vcl>`_ 
* für Enterprise Edition 5.0.0 - 5.0.1
*  `servers_conf.vcl <http://support.oxid-esales.com/downloads/varnish/5.2.5/servers_conf.vcl>`_ 
* für Enterprise Edition ab 5.2.5 und Varnish ab 4.0.3
*  `servers_conf.vcl <http://support.oxid-esales.com/downloads/varnish/5.0.0/servers_conf.vcl>`_ 
* für Enterprise Edition ab 5.0.0

Kopieren Sie die Dateien in das Verzeichnis :file:`/etc/varnish`. Wurden diese Dateien in Ihrem System bereits angepasst, müssen Sie die Inhalte der Dateien manuell zusammenführen. Starten Sie danach Apache und Varnish neu.

``/etc/init.d/apache2 stop
| /etc/init.d/varnish restart
| /etc/init.d/apache2 start``

Anpassung der Konfiguration für OXID eShop Mobile Theme
+++++++++++++++++++++++++++++++++++++++++++++++++++++++
Wenn Sie OXID eShop Mobile Theme einsetzen, müssen Sie die Konfigurationsdatei :file:`default.vcl` des Reverse Proxy anpassen. Alle dafür notwendigen Einträge finden Sie in der Datei :file:`device.vcl`, welche dem Installationspaket beiliegt. Sie können diese Datei auch durch einen Klick mit der linken Maustaste öffnen: `device.vcl <http://support.oxid-esales.com/downloads/varnish/5.0.0/device.vcl>`_ für Enterprise Edition 5.0.0 und höher.

* Kopieren Sie den Inhalt der Datei :file:`device.vcl`.
* Öffnen Sie Varnish's Konfigurationsdatei :file:`default.vcl`, die standardmäßig im Verzeichnis :file:`/etc/varnish` gespeichert ist.
* Suchen Sie nach der Funktion ``oxDefineDeviceTypeRecv`` und ersetzen Sie den Inhalt durch den kopierten Code-Schnipsel.
* Ist die Funktion nicht vorhanden, fügen Sie diese hinzu.
* Suchen Sie nun nach der Funktion ``vcl_recv``.
* Prüfen Sie, ob folgende Zeile enthalten ist: ``call oxDefineDeviceTypeRecv;``
* Fehlt diese Zeile, fügen Sie diese hinzu.
* Starten Sie Varnish neu.

SSL-Verschlüsselung
+++++++++++++++++++
Varnish verarbeitet Anfragen aus dem Web, die das HTTP-Protokoll verwenden. Verschlüsselte Anfragen mit HTTPS-Protokoll können durch den Reverse Proxy nicht umgesetzt werden. Da der OXID eShop auf SSL-Verschlüsselung umschalten kann, sobald Benutzerdaten übertragen werden, beispielsweise bei Registrierung, Anmeldung oder im Warenkorb, muss dafür eine separate Lösung geschaffen werden. Es gibt dafür aktuell zwei Möglichkeiten. Zum einen können Anfragen mit HTTPS-Protokoll direkt an den Server mit dem OXID eShop gesendet werden. Das muss mit Server-Tools umgesetzt werden. Zum anderen kann ein Load Balancer eingesetzt werden, welcher Anfragen über HTTP, Port 80 an Varnish und über HTTPS, Port 443 direkt zum OXID eShop leitet.