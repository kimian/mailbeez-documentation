---
title: 'Run MailBeez automatically'
slug: config_cron_simple
date: 05-07-2011
published: true
publish_date: 05-07-2011
template: docs
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration_status: done
    category:
        - docs
    tag: [pro]
module:
    code: config_cron_simple
    category:
        - configbeez
    compatiblity:
        - comp_osc
        - comp_cre
        - comp_digi
        - comp_zencart
        - comp_xtc
        - comp_xtcm2        
        - comp_gambio
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2011/08/icon_cron_32.png'
    pro: pro
    cert: 'true'
    price: '19 EUR'
    title_en: 'Run MailBeez Automatically'
    teaser_en: 'do some magic'
    title_de: 'MailBeez automatisch ausf&uuml;hren'
    teaser_de: 'Die einfache L&ouml;sung, um MailBeez zu automatisieren'
    author: MailBeez.com
author:
    name: admin
metadata:
    author: admin
---

>>>>>A "real" Cronjob is the most reliable way to automize MailBeez. This module is a simple alternative solution.

 

## About This Module

With this simple Mailbeez add-on, you can do away with the need to configure a cronjob to activate your Mailbeez installed modules. Instead, the plugin cleverly utilizes your store’s traffic to trigger Mailbeez as often as you have configured it to run. For site owners looking to get up and running quickly, or who do not wish to enter the server environment to setup a Cronjob, this is a very handy feature.

## Lightweight and fast

Thanks to time stamp based caching technology, the additional load added to your store’s pages by the add-on is extremely small. In fact, with the aid of modern AJAX technology, visitors to your store will not feel or notice any difference, as the add-on only triggers MailBeez after a page has loaded completely.


## Installation

>>>>>[plugin:content-inject](/content_blocks/hint_preintegration)


####osCommerce
Edit `<store-root>/includes/footer.php` as follows: At the end of the file, but before the closing `?>` tag, insert the following code:

```PHP
// MailBeez
if (defined('MAILBEEZ_CRON_SIMPLE_STATUS') && MAILBEEZ_CRON_SIMPLE_STATUS == 'True') {
    require_once(DIR_FS_CATALOG . 'mailhive/configbeez/config_cron_simple/includes/cron_simple_inc.php');
}
// - MailBeez

```
To avoid "/mailhive.php?cron_simple=1" page calls in the 'who is online' table, edit `<store-root>/includes/functions/whos_online.php` as follows:


find
```php
$wo_last_page_url = getenv('REQUEST_URI');
```

after the above code is located, insert this after it:

```php
// MailBeez
// avoid /mailhive.php?cron_simple=1 in who is online table
if (preg_match("/mailhive.php/", $wo_last_page_url)) {
   return false;
}
// - MailBeez
``` 


####Zencart
Edit `<store-root>/includes/modules/footer.php` as follows: At the end of the file, but before the closing `?>` tag, insert the following code:

```PHP
// MailBeez
if (defined('MAILBEEZ_CRON_SIMPLE_STATUS') && MAILBEEZ_CRON_SIMPLE_STATUS == 'True') {
    require_once(DIR_FS_CATALOG . 'mailhive/configbeez/config_cron_simple/includes/cron_simple_inc.php');
}
// - MailBeez

```

To avoid "/mailhive.php?cron_simple=1" page calls in the 'who is online' table, edit `<store-root>/includes/functions/whos_online.php` as follows:


Find the line containing
```php
$wo_last_page_url = (...)');
```

after the above code is located, insert this after it:

```php
// MailBeez
// avoid /mailhive.php?cron_simple=1 in who is online table
if (preg_match("/mailhive.php/", $wo_last_page_url)) {
   return false;
}
// - MailBeez
``` 




####Gambio 2.x, Modified-Shop 1.x

Edit `includes/application_bottom.php` as follows: Find the line contain

`echo '</body></html>';`

and above this line insert following code:
```php
// MailBeez
if (defined('MAILBEEZ_CRON_SIMPLE_STATUS') && MAILBEEZ_CRON_SIMPLE_STATUS == 'True') {
    require_once(DIR_FS_CATALOG . 'mailhive/configbeez/config_cron_simple/includes/cron_simple_inc.php');
}
// - MailBeez
```

To avoid "/mailhive.php?cron_simple=1" page calls in the 'who is online' table, edit `inc/xtc_update_whos_online.inc.php` as follows:

Find

```php
$wo_last_page_url = addslashes(getenv('REQUEST_URI'));
```

and insert after this line:

```php
// MailBeez
// avoid /mailhive.php?cron_simple=1 in who is online table
if (preg_match("/mailhive.php/", $wo_last_page_url)) {
   return false;
}
// - MailBeez
```

