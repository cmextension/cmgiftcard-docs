========
Cron Job
========

To send electric gift card to recipient on the delivery date which sender has chosen, you need to setup for a cron job to run at least once a day to check and send the gift cards of the current date.

Each hosting has its own way to setup cron job. If you are not sure how to setup cron job for your hosting, please contact your hosting provider for more information. 

The general command to run CM Gift Card cron job is:

php5 /path/to/your/joomla/administrator/components/com_cmgiftcard/cron.php

"php5" is the command of PHP CLI. Depending on your server's setup, the command could be different, you need to contact your hosting provider for knowing the correct command.

If the path to Joomla!'s installation folder is

/home/username/public_html/

the path to the cron job file could be

/home/username/public_html/administrator/components/com_cmgiftcard/cron.php

Once the cron job runs, it checks for the gift cards which should be sent on the current date and send them to recipients.

You need to enter your site's URL into "Site URL" option in CM Gift Card's configuration to help cron job script know your site's URL.

.. image:: ../images/configuration_06.jpg