---
title: 'Advanced Opt-Out with Admin'
slug: config_block_admin
date: 18-10-2011
published: true
publish_date: 18-10-2011
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
        - pro
module:
    code: config_block_admin
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
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2011/10/icon_325.png'
    pro: pro
    cert: 'true'
    price: '99 EUR'
    title_en: 'Advanced Opt-Out with Admin'
    teaser_en: 'Block all modules and administer customers opt-out settings'
    title_de: 'Erweitertes Opt-out mit Admin'
    teaser_de: 'Alle Module blockieren und Opt-Out der Kunden administrieren'
    author: MailBeez.com
author:
    name: admin
metadata:
    author: admin
---

 

## About This Module

This module enhances the default Opt-Out handling which is already built into MailBeez by allowing you to adjust customer Opt-Out settings by manually editing which of your customers will receive Mailbeez generated emails. And it can all be done from within your store’s admin! With this module, you can:

- Insert “block all” links into your email templates, allowing customers to choose between blocking specific emails and blocking all MailBeez generated emails
- Manually unblock customers who opt-out via accidental click
- Disable opt-out for selected modules – for example, payment reminder emails
- Manually block and unblock a customer on a per module basis
- Manually block and unblock a customer on a global basis


##Features

The Advanced Opt-Out with admin covers following featres
>>>>>>the following code is already integrated in the latest responsive main templates


**Opt-Out all MailBeez Emails**

Introducing the template var `{$block_all_url}` allows you to add a new link to your email footer:

```html
<a href="{$block_url}">no more emails like this</a> | 
<a href="{$block_all_url}">no ore emails at all</a>
```

**Disable opt-out for selected modules**

for some modules, e.g. payment reminders you don't want to allow customers to block these emails. Using the following code these emails will not provide the opt-out links:
```
{if $noblock}
   You can not block this notification
{else}
   <a href="{$block_url}">no more emails like this</a> | 
   <a href="{$block_all_url}">no ore emails at all</a>
{/if}
```

## Opt-Out Administration

In some cases you might want to manually block - or unblock - a customer. The MailBeez Opt-Out Admin panel allows you to quickly find the customer and perform the necessary action: 

[plugin:youtube](https://www.youtube.com/watch?v=3yYfw8--94s)



## Import of blacklist

Are you having email-addresses to block from external systems? This new feature allows you to easily block the matching customers.

- Pasted Email-Addresses you want to block into the input field – one address per line
- Select the modules to block
- the Email-Addresses are processed against your customer-table and the matching customers are blocked

Installation and configuration are fast and easy! Installation instructions are included in the download package.
