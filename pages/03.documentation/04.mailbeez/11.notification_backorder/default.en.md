---
title: 'Backorder Notification'
slug: notification_backorder
date: 17-12-2013
published: true
publish_date: 17-12-2013
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
    code: notification_backorder
    category:
        - mailbeez
    compatiblity:
        - comp_osc
        - comp_cre
        - comp_digi
        - comp_zencart
        - comp_xtc
        - comp_gambio
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2013/03/icon_32.png'
    pro: pro
    cert: 'true'
    price: '139 Eur'
    title_en: 'Notification: Backorder'
    teaser_en: 'notify your customers about products in backorder'
    title_de: 'Benachrichtigung Bestell-Rückstand'
    teaser_de: 'Informieren Sie Ihre Kunden laufend über Produkte im Rückstand'
    author: MailBeez.com
author:
    name: admin
metadata:
    author: admin
---

*The customer has ordered an item, which was not in stock or was not yet released. The item now is in backorder and the customer is waiting for it.*

*Every 2 days the customer asks when the item will be available...*

## Sounds familiar?

Then you should have a closer look at this automatic Backorder Notification Module.

Based on the Information "Date available" (field products_date_available) the module finds out if an order contains a product which is not or not yet in stock. And as it keeps track with the availability date it can detect changes and fire a notification right away.

The module sends out following 3 types of notification emails:

### 1. Email - tell the customer about the notification service

A product is in backorder? In this case the customer will receive an initial email right after the order telling about the backorder notification service:

> Dear customer,   
>   
>  at least one of your ordered products is in backorder.   
>   
>  We will notify you every 2 days or right a way in case we have a new arrival date.   
>   
>  the following products are in backorder:   
>   
>  (list of products with availability date)

### 2. Email - keep the customer up to date

This second type of email will be sent to the customer periodically e.g. every 3 days keeping him up-to-date with the products in back-order. A great service to make the timing waiting less painful and to appreciate the customers patience.

> Dear customer,   
>   
>  still at least one of your ordered products is in backorder.   
>   
>  We appreciate your patience and know you are waiting for the arrival. As soon as there are news we will inform you!   
>   
>  the following products are in backorder:   
>   
>  (list of products with availability date)

### 3. Email - notify the customer right away

This Email is sent as soon as there is a change in the availability date!

> Dear customer,   
>   
>  there are news regarding the items you are waiting for!   
>   
>  The availability date of the missing items has changed as following:   
>   
>  (list of products with previous and new availability date)

## Reduce workload while having full control

Once set up the module will work on autopilot (requires you have configured MailBeez to run automatically). Based on one or more order status to configure you decide which orders should processed by this module.

So as much control as necessary and as much automation as possible!


[plugin:content-inject](/content_blocks/pro_responsive_template)
