---
title: 'Payment: In advance Dunning'
slug: payment_inadvance_dunning
date: 13-05-2011
published: true
publish_date: 13-05-2011
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
    code: payment_inadvance_dunning
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
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/2011/06/payment_inadvance_dunning.png'
    pro: pro
    cert: 'true'
    price: '139 EUR'
    title_en: 'Payment in advance Dunning'
    teaser_en: 'Waiting for Payments? Automatize payment reminders.'
    title_de: 'Zahlungserinnerung Vorkasse'
    teaser_de: 'Automatisierter Ablauf mit Stornierung'
    author: MailBeez.com
author:
    name: admin
metadata:
    author: admin
---

**Awaiting payment from a customer? Take a chunk out of your admin time and automate staggered email reminders and see who has yet to pay with the Payment Dunning module from Mailbeez.**

This advanced MailBeez multistep module automates the process of Dunning for orders that require payment in advance of despatch. In effect an intelligent and fully automated payment reminder system, the Payment in Advance Dunning module can be configured to send emails to all open, non despatched orders that are awaiting payment, with emails developing from friendly reminders, all the way through to debt collection.

**Easy configuration**

For each step you can easily configure the email template, (these are called .tpl files and will hopefully familiar to you from using other Mailbeez modules) and the delay between steps. Plus, for each step you can configure the Email template (.tpl file as you know them from other MailBeez modules) and the delay *after* the step before.

 

**Preparation**

To identify which orders require a payment in advance before processing you just need to configure your order status / payment modules as following:

- You need to have an order status which identifies orders with a pending payment, e.g. “waiting for payment”
- All “in advance” payment types need to have this order status as default when the order is created or approved. You can choose the default order status in the payment module setting

For automatic cancellation of orders you need to have an order status in your system like “canceled” for example.

[plugin:content-inject](/content_blocks/pro_responsive_template)

