---
# http://learn.getgrav.org/content/headers
title: '[Zen Cart] Check Customer Authorization'
slug: filter_add_invoicenumber_xtcm
date: 19-06-2017
published: true
publish_date: 19-06-2017
template: docs
# theme: false
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration_status: done
    category: [docs]
    tag: [pro]
module:
    code: 'filter_add_invoicenumber_xtcm'
    category: [filterbeez]
    compatiblity: [comp_xtcm2]
    pro: 'pro'
    cert: 'true'      


---

Do you have installed the module "Invoice Number"? This filterbeez-module will provide placeholders allowing you to insert the custom invoice number in any MailBeez email template.

The placeholders will be filled by any MailBeez module providing the "order_id" - typically any module, which is related to orders.



    [[$data.order.ibn_billnr]] 
    [[$data.order.invoice_number]] // Alias for ibn_billnr
    [[$data.order.ibn_billdate]]
    [[$data.order.invoice_date]] // Alias for ibn_billdate