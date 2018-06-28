Registerkarte Vorschau
======================

Auf der Registerkarte :guilabel:`Vorschau` wird der Newsletter in den beiden Formaten Text und HTML angezeigt.

.. image:: ../../media/screenshots-de/oxbanu01.png
   :alt: Newsletter - Registerkarte Vorschau
   :class: with-shadow
   :height: 346
   :width: 650

Im Beispiel-Newsletter wird am Ende der HTML-Mail ein Hinweis auf vollständige Anbieterkennzeichnung ausgegeben. Der Grund ist eine Smarty-Anweisung, welche die CMS-Seite mit dem Ident "oxemailfooter" aufruft.

.. code:: html

   Bitte fügen Sie hier Ihre vollständige Anbieterkennzeichnung ein.
   <p style="font-family: Arial, Helvetica, sans-serif; font-size: 12px; margin: 0; padding: 0;">
      [{ oxcontent ident="oxemailfooter" }]
   </p>

Auch für die Nur-Text-Mail gibt es eine solche CMS-Seite. Sie hat den Ident "oxemailfooterplain". In beiden CMS-Seiten sollte das Impressum hinterlegt werden, so dass mit den Newslettern, aber auch anderen E-Mails, korrekte Informationen über den Onlineshop verschickt werden.

.. Intern: oxbanu, Status:, F1: newsletter_preview
