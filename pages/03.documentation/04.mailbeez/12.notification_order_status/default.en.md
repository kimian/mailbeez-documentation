---
title: 'Order Status Update Notification'
slug: notification_order_status
date: 01-03-2013
published: true
publish_date: 01-03-2013
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
    code: notification_order_status
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
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2013/03/icon_32.png'
    pro: pro
    cert: 'true'
    price: '49 EUR'
    title_en: 'Notification: Order Status Update'
    teaser_en: 'Notify your customers about an specific order status update, e.g. to send a delivery tracking link'
    title_de: 'Benachrichtigung: Bestell-Status Änderung'
    teaser_de: 'Benachrichtigen Sie Ihre Kunden bei speziellen Bestell-Status Änderungen, z.B. um einen Link zur Paket-Verfolgung zu schicken'
    author: MailBeez.com
author:
    name: admin
metadata:
    author: admin
---

This handy module sends a custom email notification to a customer once an order is set to one or more configured order status.

Optionally, you can configure the module to change the order status to a new status. The order comment, order status name, and order status date can be inserted into the email using a template variable.

The notification email is sent out at the next batch MailBeez email send - it is recommended to set up a cronjob running every minute to reduce the time delay between setting the order status and sending out the notification email. The MailBeez Support is happy to help you in case you have some questions.

Scenarios where this module can be applied:

- an external order management solution updates the order status, but does not sent any notification email
- you would like to replace the default order status update email with a custom designed email
- you would like to automatise processes depending on the order status

**Template Variables**


| Template Variable  | Output                                  |
|--------------------|-----------------------------------------|
| {$status_date}     | formated order status date              |
| {$status_date_raw} | raw order status date                   |
| {$status_id}       | status id                               |
| {$status_name}     | order status name                       |
| {$comments}        | comments                                |


**Custom Email Message**

You can build your custom messages depending on the order status using some [smarty.net code](http://www.smarty.net/docs/en/language.function.if.tpl)

    {if $status_id == 3}
       Your order is shipped
    {/if}



[plugin:content-inject](/content_blocks/pro_responsive_template)
