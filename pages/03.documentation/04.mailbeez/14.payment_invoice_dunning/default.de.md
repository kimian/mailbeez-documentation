---
# http://learn.getgrav.org/content/headers
title: Mahnungsablauf Rechnungskauf
slug: payment_invoice_dunning
# menu: Mahnungsablauf Rechnungskauf
date: 28-06-2011
published: true
publish_date: 28-06-2011
# unpublish_date: 28-06-2011
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
    code: 'payment_invoice_dunning'
    category: [mailbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/2011/06/payment_inadvance_dunning.png'
    pro: 'pro'
    cert: 'true'
    price: '139 EUR'
    title_en: 'Payment Invoice Dunning'
    teaser_en: 'Waiting for Invoice Payments? Automatize payment dunning.'
    title_de: 'Mahnwesen Rechnungen'
    teaser_de: 'Mahnablauf für unbezahlte Rechnungen'
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

Mit diesem MailBeez Module kann der Geschäftsprozess des Mahnungsablaufes bei Rechnungskauf automatisiert werden. Kunden mit offenen Rechnung erhalten automatisch in einstellbaren Abständen drei Zahlungsaufforderungen und letztendlich die Information, das rechtliche Schritte eingeleitet werden. Parallel zu diesem letzten Schritt kann eine Email z.B. zum Inkasso-Unternehmen gesendet werden.

Für jeden Schritt kann ein eigene Email Vorlage erstellt werden und die Anzahl Tage nach dem vorhergehenden Schritt definiert werden.

**Vorbereitung:**

Um Rechnungs-Bestellungen mit offener Zahlung im System erkennen zu können, müssen folgende Bestell-Status informationen vorliegen

- Es muss einen Bestell-Status z.B. “offene Rechnung” geben
- Alle Zahlarten vom Typ “Kauf auf Rechnung” müssen diesen Status erhalten, wenn die Bestellung versendet wurde

Für die Identifikation von Bestellungen, die ein Inkasso-Verfahren (manueller Vorgang) erfordern, muss es eine Bestellstatus z.B. “Inkasso” geben.

 
[plugin:content-inject](/content_blocks/pro_responsive_template)
