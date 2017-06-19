---
# http://learn.getgrav.org/content/headers
title: Zahlungserinnerung Vorkasse
slug: payment_inadvance_dunning
# menu: Zahlungserinnerung Vorkasse
date: 13-05-2011
published: true
publish_date: 13-05-2011
# unpublish_date: 13-05-2011
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
    code: 'payment_inadvance_dunning'
    category: [mailbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/2011/06/payment_inadvance_dunning.png'
    pro: 'pro'
    cert: 'true'
    price: '139 EUR'
    title_en: 'Payment in advance Dunning'
    teaser_en: 'Waiting for Payments? Automatize payment reminders.'
    title_de: 'Zahlungserinnerung Vorkasse'
    teaser_de: 'Automatisierter Ablauf mit Stornierung'
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

Mit diesem MailBeez Module kann der Geschäftsprozess zur Zahlungserinnerung bei Bestellungen per Vorkasse automatisiert werden. Kunden mit Vorkasse-Zahlungen erhalten automatisch in einstellbaren Abständen drei Zahlungsaufforderungen und letztendlich die Information, dass die Bestellung storniert wurde.

Für jeden Schritt kann ein eigene Email Vorlage erstellt werden und die Anzahl Tage nach dem vorhergehenden Schritt eingestellt werden.
 

**Vorbereitung:**

Um Vorkasse-Bestellungen mit offener Zahlung im System erkennen zu können, müssen folgende Bestell-Status informationen vorliegen

- Es muss einen Bestell-Status z.B. “Wartet auf Zahlungseingang” geben
- Alle Zahlarten vom Typ “Vorkasse” müssen diesen Status als Standardstatus erhalten, wenn Bestellungen eingehen oder Bestellung nach Prüfung akzeptiert werden. Dies kann typisch bei der Zahlart eingestellt werden

Für eine automatische Stornierung muss es eine Bestellstatus z.B. “storniert” geben.


[plugin:content-inject](/content_blocks/pro_responsive_template)
