---
title: 'BeezDesk Customer Insight'
slug: config_customer_insight
date: 22-03-2013
published: true
publish_date: 22-03-2013
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
    tag:
        - core
author:
    name: admin
metadata:
    author: admin
---

The extensible BeezDesk CRM Customer Insight add-on helps you to **improve both your understanding about your customers and your customer service** by giving you a customer centric view about the customer related data in your MailBeez compatible store.


The modular Customer Insight view can be opened from any page with customer information (customer, order), while the CRM Pad is available on any store admin page.

Developers can easily enhance the Customer Insight view e.g. with modules to pull-in customer related information from 3rd party systems and reduce development efforts to a minimum. There is no need to modify the core files to keep everything to update.

The Customer Insight view gives you an immediate overview of all orders, products purchased, etc and can be upgraded towards a fully featured professional multichannel ticket system supporting email, live chat, Facebook, twitter, phone calls including web forms, knowledge base, forums and suggestion boards for a real multichannel customer support solution. This allows store owners to consolidate their communication channels and streamline their customer support.

[read more about BeezDesk CRM](https://www.beezdesk.com)

>>>>>[plugin:content-inject](/content_blocks/hint_preintegration)

### Installation




To add the BeezDesk CRM Pad and BeezDesk Customer Insight button to the store-admin pages, see following instructions:

**All Systems**

open

 
`(shop)/<admin-dir>/includes/footer.php`


before the closing PHP Tag  `?>`  insert following code

``` 
// BOF: Mailbeez Customer Insight
define('MH_DIR_FS_CATALOG', (substr(DIR_FS_CATALOG, -1) != '/') ? DIR_FS_CATALOG . '/' : DIR_FS_CATALOG);
@include(MH_DIR_FS_CATALOG . '/mailhive/configbeez/config_customer_insight/includes/admin_footer_include.php');
// EOF: Mailbeez Customer Insight
```


Additional installation-instructions:

**Zencart**

open

 
`(shop)/<admin-dir>/index.php`


insert above the closing HTML Tag `</body>` following code:

```
<?php
// BOF: Mailbeez Customer Insight
define('MH_DIR_FS_CATALOG', (substr(DIR_FS_CATALOG, -1) != '/') ? DIR_FS_CATALOG . '/' : DIR_FS_CATALOG);
@include(MH_DIR_FS_CATALOG . '/mailhive/configbeez/config_customer_insight/includes/admin_footer_include.php');
// EOF: Mailbeez Customer Insight
?>
```

**Modified-Shop**

open

 
`(shop)/<admin-dir>/start.php`


insert above the closing HTML Tag `</body>` following code:

```
<?php
// BOF: Mailbeez Customer Insight
define('MH_DIR_FS_CATALOG', (substr(DIR_FS_CATALOG, -1) != '/') ? DIR_FS_CATALOG . '/' : DIR_FS_CATALOG);
@include(MH_DIR_FS_CATALOG . '/mailhive/configbeez/config_customer_insight/includes/admin_footer_include.php');
// EOF: Mailbeez Customer Insight
?>
```