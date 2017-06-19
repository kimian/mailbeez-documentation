---
# http://learn.getgrav.org/content/headers
title: '[Modified] Neue Rechnungsnummer'
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

Wenn Sie das Modul "Neue Rechnungsnummer" installiert haben, dann stellt dieses Filterbeez-Modul die passenden Platzhalter für den Einsatz in alle MailBeez Email Vorlagen zur Verfügung.

Die Platzhalter werden nur befüllt, wenn das jeweilige MailBeez-Modul die "order_id" zur Verfügung stellt. Dies ist typisch bei allen Modulen der Fall, welche in Bezug auf Bestellungen arbeiten.



    [[$data.order.ibn_billnr]] 
    [[$data.order.invoice_number]] // Alias für ibn_billnr
    [[$data.order.ibn_billdate]]
    [[$data.order.invoice_date]] // Alias für ibn_billdate