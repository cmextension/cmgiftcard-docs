==========================
Predefined Gift Card Codes
==========================

CM Gift Card allows you to use your own gift card codes, this helps you control what codes are available. For example you can generate your coupon codes from your ecommerce (shopping cart) application and import these codes into CM Gift Card, after gift card code is delivered to customer, he/she can use it to buy for your products in your ecommerce software instantly.

You can access Predefined Gift Card Codes section via Joomla!'s top menu or side menu of CM Gift Card.

.. image:: ../images/predefined_code_01.jpg

To create a new code, you click "New" button on the toolbar.


.. image:: ../images/predefined_code_02.jpg

You enter the code, set "Status" to "Published" if the code is ready to be given to customer, or to "Unpublished" if you don't want it to be used yet.

If you have lots of gift card code, you can use the import tool to create all of them automatically.

First you need to store you codes in a text file with "txt" extension, for example "my_codes.txt". Each code is in a separate line.

Ensure the your codes are in the same length and have the same character types which you set in CM Gift Card's configuration. Example:

* If you set the length of gift card code to 5 in CM Gift Card's configuration and the code in your code file is "4KD01L" (6 characters), then it will be converted to "4KD01" (5 characters).
* If you set the type of gift card code to "Latin alphabetic" in CM Gift Card's configuration and the code in your code file is "03P4FA" (has both alphabetic and numeric characters), it will be converted to "3PFA" (only alphabetic characters, numeric characters are removed). It will not be imported if its length is smaller than gift card code's length.

If there are lower case characters in your code, they will be converted to upper case automatically.

You go to "Tools" section in CM Gift Card, select your code file in "Import Gift Card Code" section and click "Upload & Import" button.

.. image:: ../images/predefined_code_03.jpg

After the file is uploaded, the codes will be imported and you will see the result when the import process is completed. If there are the codes which are not imported, they may be already available on your site as predefined gift card codes or purchased gift card codes.

.. image:: ../images/predefined_code_04.jpg

Go back the predefined gift card code list, you can see your codes imported.

.. image:: ../images/predefined_code_05.jpg
