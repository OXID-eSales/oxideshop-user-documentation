Registerkarte HTML
==================

OXID eShop verschickt Newsletter immer in zwei Formaten: als HTML-Mail und als Nur-Text-Mail. Dadurch wird sichergestellt, dass der Newsletter von allen Mail-Programmen und Webmailern korrekt dargestellt wird. Auf der Registerkarte :guilabel:`HTML` wird der Newsletter im HTML-Format erstellt. Im Gegensatz zum Nur-Text-Format können hier Inhalte durch Überschriftenhierarchien, unterschiedliche Schriftfarben und -größen und andere Formatierungen hervorgehoben werden. Es lassen sich Firmenlogo, Grafiken, Links und Artikelfotos einbinden.

.. image:: ../../media/screenshots/oxbaif01.png
   :alt: Newsletter - Registerkarte HTML
   :height: 346
   :width: 650

:guilabel:`Titel` |br|
Der Newsletter wird mit diesem Titel im Administrationsbereich des Shops angezeigt und kann darüber mit der Suche gefunden werden. Der Titel wird im versendeten Newsletter nicht verwendet.

:guilabel:`Betreff` |br|
Im Betreff wird der Inhalt des Newsletters zusammengefasst. Da der Betreff das Erste ist, was der Empfänger des Newsletters in seinem Posteingang sieht, sollte der Betreff eine kurze und prägnante Information zum Newsletter sein. Das entscheidet darüber, ob der Empfänger den Newsletter öffnet oder direkt in den Papierkorb verschiebt. Der Betreff gilt für beide Newsletter-Formate.

:guilabel:`Vorlage` |br|
Der Inhalt des Newsletters kann komfortabel in einen Editor eingegeben werden. Dieser arbeitet nach dem Prinzip WYSIWYG (What You See Is What You Get), er zeigt also den Text so an, wie er später im Newsletter zu sehen sein wird. Der Editor bietet die Möglichkeit der Textformatierung, des Einfügens von Bildern und von Links.

Für das Erstellen eines Newsletters im HTML-Format ist es wichtig zu wissen, dass die meisten Mail-Programme und Webmailer HTML darstellen können, es aber keine verlässlichen Standards gibt. Um sicher zu gehen, muss auf veraltete Techniken zurückgegriffen werden. Arbeiten Sie mit Tabellen, Font-Tags und Inline-CSS. CSS-Positionierung über floats, Videos, Audios, Formulare und Scripts sollten in Ihrem Newsletter hingegen nicht verwendet werden. Im Internet findet sich eine Vielzahl von Seiten, die Tipps zum Erstellen und Testen von HTML-Newslettern geben.

Eine Besonderheit beim Erstellen des Newsletters ist, dass er Platzhalter für dynamische Inhalte enthalten kann. An dafür vorgesehenen Textstellen können Inhalte aus dem Onlineshop, wie beispielsweise die Anrede, der Vor- und Zuname eines Benutzers, die Adresse des Shops oder Informationen zu bestimmten Artikeln, ausgegeben werden.

Die dynamischen Inhalte werden mit *Smarty*, einer Template-Engine für PHP, umgesetzt. Der bereitgestellte Standard wurde mit speziellen, für den Onlineshop benötigten Funktionen erweitert. Die dazugehörigen Dateien befinden sich im Ordner
:file:`/core/smarty/plugins`.

Die Funktionsweise der Smarty-Anweisungen wird an einem Beispiel aus dem Beispiel-Newsletter deutlich. Beim Versenden des Newsletters werden die Smarty-Anweisungen, die wie Platzhalter fungieren, durch reale Daten aus dem Shop ersetzt.

.. code:: html

   <p style="font-family: Arial, Helvetica, sans-serif; font-size: 12px;"
      Hallo [{ $myuser->oxuser__oxsal->value|oxmultilangsal }] [{ $myuser->oxuser__oxfname->value }] [{ $myuser->oxuser__oxlname->value }],
   </p>

Der Empfänger des Newsletters wird persönlich angesprochen, indem  Anrede, Vorname und Nachname aus der Datenbank gelesen und ausgegeben werden. Das Ergebnis kann auf der Registerkarte :guilabel:`Vorschau` eingesehen werden.

.. seealso:: `E-Mail Standards Project <http://www.email-standards.org>`_ | `Smarty Template Engine <https://www.smarty.net>`_ | :doc:`Registerkarte Vorschau <registerkarte-vorschau>`

.. Intern: oxbaif, Status:, F1: newsletter_main