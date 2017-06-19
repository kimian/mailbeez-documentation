---
title: 'Payment: Invoice Dunning'
slug: payment_invoice_dunning
date: 28-06-2011
published: true
publish_date: 28-06-2011
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
    code: payment_invoice_dunning
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
    title_en: 'Payment Invoice Dunning'
    teaser_en: 'Waiting for Invoice Payments? Automatize payment dunning.'
    title_de: 'Mahnwesen Rechnungen'
    teaser_de: 'Mahnablauf für unbezahlte Rechnungen'
    author: MailBeez.com
author:
    name: admin
metadata:
    author: admin
---

**The Mailbeez Invoice Dunning module is an incredibly powerful solution for stores that send out orders for clients on invoice terms, and one that drastically reduces store administration; allowing the business owner to focus on sales rather than admin.**

As an intelligent and fully automated payment reminder system, the Invoice Dunning module can be configured to send emails to all open account orders that are awaiting payment. Emails develop, naturally, from friendly reminders, all the way through to debt collection.
 

**Easy configuration**

For each step, you can easily configure the email template, and the delay between steps, providing total control over the eco-system of emails.

**Preparation:**

To identify which orders are waiting for payment, you simply need to configure your order status / payment modules as following:

- You need to have an order status which identifies orders with open payment, e.g. “open payment of invoice”
- All “invoice” payment orders need to be set to this status until you received the payment. You can choose the default order status in the payment module setting

For automatic identification of orders with long overdue payments, the module can assign an order status of “debt collection”


[plugin:content-inject](/content_blocks/pro_responsive_template)
