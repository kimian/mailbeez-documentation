---
title: 'Shopper Approved Advanced'
slug: shopperapproved_advanced
date: 08-05-2015
published: true
publish_date: 08-05-2015
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
    code: shopperapproved_advanced
    category:
        - mailbeez
    compatiblity:
        - comp_osc
        - comp_cre
        - comp_digi
        - comp_zencart
        - comp_xtc
        - comp_xtcm2        
        - comp_gambio
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2013/06/top_64.png'
    pro: pro
    cert: 'true'
    price: '99 EUR'
    title_en: 'Shopper Approved Advanced'
    teaser_en: 'Advanced Features: Delay for international orders, multiple Order status, recognition of regular customers'
    title_de: 'Idealo Profi'
    teaser_de: 'Profi-Features: Verzögerung für internationale Bestellungen, Stammkunden-Erkennung und mehr'
    author: MailBeez.com
author:
    name: admin
metadata:
    author: admin
---

**Get the most out of your Shopper Approved plan**

This module allows you to invite your customers to review your Store on Shoppperapproved.com. You can even go back in time to kickstart your reviews!

## Advanced Features

This advanced module gives you a couple of settings to streamline and improve the process of inviting customers to give a review on Shopper Approved.

## Multiple order status

Do you use different order status? No problem, you decide which order status you want the module to react on.

## Delay times for international orders

Shipping to international customers typically takes a couple days longer. To avoid sending a review invite before delivery, you can define an additional delay for orders shipping to other countries than your own!

The module automatically applies this delay to all orders which are shipped to a country, which is different from the home country you configured in your shopping-cart system.

## Recognition of regular customers

Don't want to bother your regular customers with an invite to review on Shopper Approved? Simply define a delay (e.g. 120 days) between two invites and you're done. The module will check when the last invite was sent and decide whether to wait or to send a new invite.

## Segmentation by number of orders

Select how many orders a customer must haved placed before the module invites them to give a review!

### Want to integrate your valuable Shopper Approved ratings with your marketing efforts?

Using the [Shopper Approved Integration Suite](/documentation/configbeez/config_shopperapproved_integration/) you can easily integrate your Shopper Approved reviews with your online shopping-cart - in a way that makes this unique and "fresh" content visible to search engines - and your MailBeez generated marketing emails!

### Different ways to invite 

Choose different ways to invite your customers to give reviews - all customizable to your needs! You can also create the initial invite with pre-populated customer data!

## Default review page

The default review page is template based and you can easily set up your own, customized template!

### Make any page a review page

Insert the following code on the page (e.g. `my-custom-page.php`) where you want to direct the customers to place a review:

```
if (isset($_GET['SA'])) {
    require_once(DIR_FS_CATALOG . 'mailhive/mailbeez/shopperapproved_advanced.php');
    $sa = new shopperapproved_advanced();
    $code = $sa->generate_page($_GET['SA'], 'core.tpl.html');
    echo $code;
}
```


...then adjust the invite link in your MailBeez email template to e.g.:

`http://mydomain.com/my-custom-page.php?SA={$sa_invite_parameter_value}`

## Invite to full Survey with pre-populated order-id

Do you want to skip the initial survey? No Problem!

Copy the link to the full survey from your Shopper Approved account into your MailBeez email template. Replace `<order-id>` with `{$order_id}`

Now customers are directed to the full survey with pre-filled order id!
