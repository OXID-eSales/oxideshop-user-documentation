Inline Markup und Formatvorlagen
********************************

Inline Markup für Menünavigation (menuselection) :menuselection:`Artikel verwalten -->  Artikel`

Inline Markup für Dateinamen (file) :file:`/usr/lib/python2.{x}/site-packages`

Inline Markup für (guilabel) :guilabel:`Cancel` 

Inline Markup für Code (code) ``exclude_patterns = ['_build', 'Thumbs.db', '.DS_Store']``

Inline Markup für Kommando (command) :command:`cd ..\\GitHub\\Dokumentation-und-Hilfe`

.. warning:: Das ist ein "warning/Warnung".

.. attention:: Das ist ein "attention/Achtung".

.. caution:: Das ist ein "caution/Vorsicht".

.. danger:: Das ist ein "danger/Gefahr".

.. error:: Das ist ein "error/Fehler".

.. hint:: Das ist ein "hint/Hinweis".

.. important:: Das ist ein "important/Wichtig".

.. note:: Das ist ein "note/Bemerkung".

.. tip:: Das ist ein "tip/Tipp".

.. seealso:: Das ist ein "Siehe auch".

Konvertierung
-------------

:menuselection: <span class="tech-control"> für Menünavigation

:guilabel: <span class="tech-control"> für Label, Buttons, Kontrollkästchen, Registerkarten etc.


**Probleme**

Links werden ja automatisch umgesetzt. Was, wenn sie als Quellcode <span class="tech-code"> formatiert sind?

<h4> bei der Übersicht der Registerkarten durch <b> ersetzen. So tauchen die Registerkarten nicht im Menü auf. Eventuell eigenes Inline Markup :guitabs: ?