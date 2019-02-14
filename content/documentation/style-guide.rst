Style Guide
===========

This part of the documentation is only for visual style and wording.


Writing Content
---------------

There is an internet slang **TL;DR**, which means *too long, didn't read* (see more information on `Wikipedia <https://en.wikipedia.org/wiki/TL;DR>`__). Many people don't like reading long texts, so please keep the documentation as short as possible. Use step-by-step tutorials instead of writing wall of text.

For example this is a **wrong** example for writing content:

.. code-block:: rst

   The agents are able to change the interface language of OTRS. To change the
   interface language, click on your avatar on the top left corner, then select
   Personal Settings menu item. A new screen will be displayed. On this screen
   click on the User Profile, and then find a widget named Language. Select the
   desired language in the drop-down menu. Please make sure to click on the
   Save button next to the language widget.

The same content in **suggested** *human understandable* format:

.. code-block:: rst

   To change the interface language of OTRS:

   1. Click on your avatar on the top left corner.
   2. Select *Personal Settings*.
   3. Click the *User Profile* in the new screen.
   4. Choose a language from the drop-down menu of the *Language* widget.
   5. Click the *Save* button next to the widget.

The latter is easier to translate, because 6 short sentences will be included in the language file. If a content is changed in one of the sentences, only the changed sentence need to be reviewed and translated again. The first wrong example puts only one huge string to the language file, and if some changes will be made in the source string, the translator needs to review and re-translate the whole string.


Screenshots
-----------

Don't use the native resolution of your machine. Usually it is full HD or bigger, so creating a screenshot with this resolution will became unreadable in some output, because all the images have to be shrink to the width of A4 paper in case of PDF. OTRS uses responsive design, so 1025 pixels is the minimum, that OTRS assumes it is a large display. Please use this as width of your screenshots.

.. seealso::

   The resolution can be set in all web browser with a feature called *mobile mode* or *responsive design*. Check your browser user manual for the usage of the feature and set the width of the screen to 1025 pixels.

This is an example for a **wrong** screenshot, as it has resolution of full HD. Due to the automatic shrinking the texts on the screenshot are hard to read:

.. figure:: images/screenshot-1920.png
   :alt: Agent Dashboard (1920 pixels width)

   Agent Dashboard (1920 pixels width)

The same screenshot with **suggested** resolution. The texts are much easier to read:

.. figure:: images/screenshot-1025.png
   :alt: Agent Dashboard (1025 pixels width)

   Agent Dashboard (1025 pixels width)

It is also wrong, if the screenshot has good resolution in pixels, but with high DPI. For example this screenshot is **wrong**, because the texts on it is much bigger than the other texts in the documentation:

.. figure:: images/AgentVideoInvitationDialog.png
   :alt: Video Invitation Dialog (756 pixels width but with high DPI)

   Video Invitation Dialog (756 pixels width but with high DPI)


Create Screenshots with Firefox
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If only a part of the screenshot is required, the screenshot needs to be cropped. The administrator interface of OTRS consist of a left sidebar and a main content column. To create screenshots with Firefox:

1. Right click on an element in the browser and select *Inspect element*.
2. Select the element in the DOM, if it was not selected.
3. Right click on the node and select *Screenshot Node*.

.. figure:: images/cropping-main.png
   :alt: Example screenshot for the main content

   Example screenshot for the main content

.. figure:: images/cropping-sidebar.png
   :alt: Example screenshot for the left sidebar

   Example screenshot for the left sidebar

.. figure:: images/cropping-content.png
   :alt: Example screenshot for the content column

   Example screenshot for the main content column


Capitalization in Documentation
-------------------------------

For titles always have to use sentence case capitalization, which means, that in titles always capitalize:

- Nouns (man, bus, book).
- Adjectives (angry, lovely, small).
- Verbs (run, eat, sleep).
- Adverbs (slowly, quickly, quietly).
- Pronouns (he, she, it).
- Subordinating conjunctions (as, because, that).

In titles do not capitalize:

- Articles: a, an, the.
- Coordinating conjunctions: and, but, or, for, nor, etc.
- Prepositions (fewer than five letters): on, at, to, from, by, etc.

In normal sentences don't capitalize any words, only names and reference to titles have to be capitalized. This is a **wrong** example:

.. code-block:: rst

   An Agent is a user, who handles Tickets in the Ticket Zoom screen.

The **suggested** sentence with proper capitalization. Besides, *Ticket Zoom* is the name of the screen, so it should be emphasized:

.. code-block:: rst

   An agent is a user, who handles tickets in the *Ticket Zoom* screen.


Buttons and Screen Names
------------------------

In the content sentences all buttons and screens should be emphasized and should be written with capital letters or in sentence case. Don't use apostrophes or quotation marks for emphasizing.

This sentence is **wrong**, because apostrophes are used for emphasizing:

.. code-block:: rst

   If you click the 'Save and Finish' button, you will be redirected to the 'Ticket Zoom' screen.

The **suggested** way is to use asterisks for emphasizing:

.. code-block:: rst

   If you click the *Save and Finish* button, you will be redirected to the *Ticket Zoom* screen.


Wording
-------

Don't use variable names in sentences. This sentence is **wrong**, because a variable name is meaningless for some people:

.. code-block:: rst

   Add a new widget to AgentTicketZoom.

The same sentence without variable name, this is **suggested**:

.. code-block:: rst

   Add a new widget to the *Ticket Zoom* screen of the agent interface.


Variable Names
--------------

Variable names should always marked as ``literal`` content. This is useful for translators, as they can exactly know, that the string mustn't be translated. If a string is not marked as literal content, it usually should be translated. For example:

.. code-block:: rst

   The ``ObjectManager`` object has an ``Init()`` function. Additional configuration can be set in ``Kernel::Config::Config.pm`` file.
