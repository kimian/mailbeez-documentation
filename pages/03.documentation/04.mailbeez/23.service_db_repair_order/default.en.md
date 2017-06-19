---
title: 'Service-Module: Repair Orders DB'
slug: service_db_repair_order
date: 07-02-2013
published: true
publish_date: 07-02-2013
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
    code: service_db_repair_order
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
    thumbnail: ''
    pro: pro
    cert: 'true'
    price: '29 EUR'
    title_en: 'Service-Module: Repair Orders DB '
    teaser_en: 'This module repairs corrupted Order Databases'
    title_de: 'Service-Modul: Repariere Bestell-Datenbank'
    teaser_de: 'Dieses Modul repariert korrupte Bestell-Datenbanken'
    author: MailBeez.com
author:
    name: admin
metadata:
    author: admin
---

## Problem:

External order management solutions or custom addons can cause corrupted Order Database Tables.

## Symptom:

The Order status in the order overview does not match with the Order Status in the Order-Edit View.  
 MailBeez modules can’t find any or not all orders / customers.

## Solution:

This module automatically repairs the corrupted Order Database Tables

Features:

- In Simulation mode only the corrupted Orders are listed, but not repaired
- runs very efficiently before all other modules
- You can choose, if you want to keep the Order Status or assign a new order status to repaired orders
