---
# http://learn.getgrav.org/content/headers
title: Service-Modul: Repariere Bestell-Datenbank
slug: service_db_repair_order
# menu: Service-Modul: Repariere Bestell-Datenbank
date: 07-02-2013
published: true
publish_date: 07-02-2013
# unpublish_date: 07-02-2013
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
    code: 'service_db_repair_order'
    category: [mailbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: ''
    pro: 'pro'
    cert: 'true'
    price: '29 EUR'
    title_en: 'Service-Module: Repair Orders DB '
    teaser_en: 'This module repairs corrupted Order Databases'
    title_de: 'Service-Modul: Repariere Bestell-Datenbank'
    teaser_de: 'Dieses Modul repariert korrupte Bestell-Datenbanken'
    author: 'MailBeez.com'
# added collection selector

author:
    name: admin
metadata:
    author: admin
#      description: Your page description goes here
#      keywords: HTML, CSS, XML, JavaScript
#      robots: noindex, nofollow
#      og:
#          title: The Rock
#          type: video.movie
#          url: http://www.imdb.com/title/tt0117500/
#          image: http://ia.media-imdb.com/images/rock.jpg
#  cache_enable: false
#  last_modified: true
---

## Problem:

Externe Bestell-Verwaltungssysteme oder andere Addons können die Integrität der Bestell-Datenbank-Tabellen beschädigen.

## Symptome:

Der Bestell-Status in der Auflistungen der Bestellungen stimmt nicht mit dem Status in der Bestell-Bearbeitungs-Ansicht überein.

MailBeez kann keine oder nicht alle Bestellungen / zu kontaktierende Kunden finden.

## Lösung:

Dieses Modul repariert die beschädigte Bestell-Datenbank automatisch.

Funktionen:

- Im Simulationsmodus werden die beschädigten Bestellungen aufgelistet, aber nicht repariert
- Sehr effizientes Modul, welches vor allen weiteren Modulen ausgeführt wird
- Zwei Betriebsarten: Bestell-Status beibehalten oder den reparierten Bestellungen einen neuen Status zuweisen
