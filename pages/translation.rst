===========
Translation
===========

CM Gift Card uses English by default however you can always translate CM Gift Card to other languages just like Joomla! or other Joomla! extensions.

Installation
^^^^^^^^^^^^

Before translating CM Gift Card to another language, you need to know install that new language.

In your Joomla! back-end, you go to Extensions -> Language(s). You can see the list of installed languages on your site. Click "Install Languages" button on the toolbar to install a new language.

.. image:: ../images/translation_01.jpg

The next page is the list all of available languages.

.. image:: ../images/translation_02.jpg

You can use the search field to search for the language you want to install, select it in the list and click "Install" button.

.. image:: ../images/translation_03.jpg

If the language is installed successfully, you can see the successful message from Joomla!.

.. image:: ../images/translation_04.jpg

After installing new language, go back to the installed language list, you can see your new language in the list.

.. image:: ../images/translation_05.jpg

You need to remember the language tag of your new language. The language tag is shown next to the language name in "Language" column. In the above screenshot, French language package is installed, and "fr-FR" is the language tag of French.

Preparation
^^^^^^^^^^^

You can use your favorite FTP client software or file managers available in your hosting control panel to navigate to <Joomla! root folder>/components/com_cmgiftcard/language/ folder. In this folder you can see the folder "en-GB", this is where the language files of English are stored.

In this "language" folder, you create a new folder for your new language, the name of the folder is the language tag. Follow the above example, you create a new folder "fr-FR".

Go to "en-GB" folder, copy "en-GB.com_cmgiftcard.ini" file in this folder to the new language folder that you just create ("fr-FR" as in the example).

In the new language folder folder, rename "en-GB.com_cmgiftcard.ini" to "xx-YY.com_cmgiftcard.ini", "xx-YY" is the language tag of your new language, eg "fr-FR".

Translate
^^^^^^^^^

Open "xx-YY.com_cmgiftcard.ini" with a text editor and translate the English strings in this file to your new language.

*Important note*: Joomla! language INI files must be saved as UTF-8 without the Byte Order Mark (BOM). For more information on Byte Order Mark see `http://unicode.org/faq/utf_bom.html#BOM <http://unicode.org/faq/utf_bom.html#BOM>`_

The above instruction is for translating the front-end of CM Gift Card component. To translate the back-end and other extensions, you need to repeat the above steps for the following folders:

* **CM Gift Card component's back-end**: <Joomla! root folder>/administrator/components/com_cmgiftcard/language/
* **PayPal payment method plugin**: <Joomla! root folder>/plugins/cmgiftcard/paypal/language/
