==========
Menu Items
==========

.. image:: ../images/menu_item_types.jpg

There are 7 menu item types available for CM Gift Card:

* Default
* Shopping Cart
* Checkout
* Orders
* Order
* Check Gift Cards
* Check Gift Card Detail

You need to create at least "Default" menu item to let your customers select the gift card types they want to buy.

CM Gift Card can work without "Shopping" and "Checkout" menu items, however the URLs of these pages don't look good. So it is recommended that you create menu items for these pages to have ability to control the URLs.

"Orders" is required if you allow your customers to check their order history. "Order"

"Check Gift Cards" is used if you allow your staff to check gift card info in front-end.

"Order", "Check Gift Card Detail" are not required. You may want to create these menu item as hidden menu items if you want to control the URL of these pages and the Joomla! modules which are shown on these pages.

Hidden menu items are the menu items which are not shown in your site's front-end. To create hidden menu item:

* You create a new menu, give this menu a title (whatever you like, for example "Hidden menu")
* Create new menu items in this new menu.

As long as you don't assign this new menu to a menu module and show the module in your front-end, the menu items in this menu are also not shown in your front-end, they are considered "hidden".

The purposes of hidden menu item are giving us ability to control the URL of the page (via menu item's alias) and control what modules are shown on the page.