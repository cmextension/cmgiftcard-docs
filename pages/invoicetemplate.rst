.. _ref-invoice-template:

================
Invoice Template
================

CM Gift Card gives you ability to attach a PDF invoice of customer order into the email sent to customer after payment is completed. To use this feature you need to enable it in CM Gift Card's configuration and install mPDF library.

You can design your invoice template in CM Gift Card's configuration by using HTML and CSS. After invoice is generated, it is converted to PDF by mPDF library and is attached to order confirmation email.

.. image:: ../images/configuration_08.jpg

Here are the available tags for invoice. They will be converted to actual info of customer and order before being sent to customer.

* {customer_name}: Customer's name
* {customer_email}: Customer's email address
* {customer_address_1}: Customer's address line 1
* {customer_address_2}: Customer's address line 2
* {customer_address_3}: Customer's address line 3
* {customer_postal_box}: Customer's postal box
* {customer_city}: Customer's city
* {customer_state}: Customer's state
* {customer_postal_code}: Customer's postal code
* {customer_country}: Customer's country
* {order_number}: Order's number
* {order_date}: Order's completed date or created date
* {payment_method}: Payment method's name
* {transaction_id}: Transaction ID
* {order_items}: List of order items (gift cards)

There is a special tag, "{order_items}", which shows the list of gift cards in order. By default, the result of "{order_items}" is a table HTML element (<table>), the code which generates this table is in

administrator/components/com_cmgiftcard/layouts/invoice_items.php.

To customize this output of order items, you create a new file 

administrator/components/com_cmgiftcard/layouts/invoice_items_custom.php

Copy the content of invoice_items.php and paste into invoice_items_custom.php and start customize invoice_items_custom.php. Your own customizations will not be lost when you upgrade CM Gift Card because the file invoice_items_custom.php doesn't exist in CM Gift Card.

Here is a sample invoice template. Copy the HTML code below, switch the editor of invoice template file to HTML mode (if you use TinyMCE editor, click "Toggle editor" button), paste the code into the editor, switch back to What-You-See-Is-What-You-Get (WYSIWYG) mode to see the result (click "Toggle editor" button again for TinyMCE)::

	<table style="width: 100%;" border="0" cellspacing="0" cellpadding="2">
	<tbody>
	<tr>
	<td style="width: 70%;">
	<p style="font-size: 30px; font-weight: bold;">YOUR COMPANY NAME</p>
	<p>123 Street,<br />ABC City,<br />DEF Country</p>
	<p>Tel: 012 345 6789</p>
	</td>
	<td style="width: 30%;">Your company logo</td>
	</tr>
	</tbody>
	</table>
	<table style="margin: 20px 0; width: 100%;" border="0" cellspacing="0" cellpadding="2">
	<tbody>
	<tr>
	<td style="width: 50%; vertical-align: top;">
	<table style="width: 100%;" border="0" cellspacing="0" cellpadding="2">
	<tbody>
	<tr>
	<td style="background-color: #d6d6d6;" colspan="2" align="left"><strong>Customer Information</strong></td>
	</tr>
	<tr>
	<td width="50%"><strong>Name</strong></td>
	<td width="50%">{customer_name}</td>
	</tr>
	<tr>
	<td width="50%"><strong>Email</strong></td>
	<td width="50%">{customer_email}</td>
	</tr>
	<tr>
	<td width="50%"><strong>Address</strong></td>
	<td width="50%">{customer_address_1}</td>
	</tr>
	<tr>
	<td width="50%"><strong>Address Line 2</strong></td>
	<td width="50%">{customer_address_2}</td>
	</tr>
	<tr>
	<td width="50%"><strong>Address Line 3</strong></td>
	<td width="50%">{customer_address_3}</td>
	</tr>
	<tr>
	<td width="50%"><strong>Postal Box</strong></td>
	<td width="50%">{customer_postal_box}</td>
	</tr>
	<tr>
	<td width="50%"><strong>City</strong></td>
	<td width="50%">{customer_city}</td>
	</tr>
	<tr>
	<td width="50%"><strong>State</strong></td>
	<td width="50%">{customer_state}</td>
	</tr>
	<tr>
	<td width="50%"><strong>Postal Code</strong></td>
	<td width="50%">{customer_postal_code}</td>
	</tr>
	<tr>
	<td width="50%"><strong>Country</strong></td>
	<td width="50%">{customer_country}</td>
	</tr>
	</tbody>
	</table>
	</td>
	<td style="width: 50%; vertical-align: top;">
	<table style="width: 100%;" border="0" cellspacing="0" cellpadding="2">
	<tbody>
	<tr>
	<td style="background-color: #d6d6d6;" colspan="2" align="left"><strong>Order Information</strong></td>
	</tr>
	<tr>
	<td width="50%"><strong>Order Number</strong></td>
	<td width="50%">{order_number}</td>
	</tr>
	<tr>
	<td width="50%"><strong>Date</strong></td>
	<td width="50%">{order_date}</td>
	</tr>
	<tr>
	<td width="50%"><strong>Payment method</strong></td>
	<td width="50%">{payment_method}</td>
	</tr>
	<tr>
	<td width="50%"><strong>Payment ID</strong></td>
	<td width="50%">{transaction_id}</td>
	</tr>
	<tr>
	<td width="50%"><strong>Payment Status</strong></td>
	<td width="50%">Paid</td>
	</tr>
	</tbody>
	</table>
	</td>
	</tr>
	</tbody>
	</table>
	<table style="width: 100%;" border="0" cellspacing="0" cellpadding="2">
	<tbody>
	<tr>
	<td style="background-color: #d6d6d6;" colspan="2" align="left"><strong>Gift Cards</strong></td>
	</tr>
	<tr>
	<td colspan="2">{order_items}</td>
	</tr>
	</tbody>
	</table>

Please don't hesitate to contact us if you need help in customize invoice template and gift card list in invoice.