---
# http://learn.getgrav.org/content/headers
title: Share Review on Facebook
slug: review_facebook
routes:
    default: /dokumentation/mailbeez/review_facebook
# menu: Share Review on Facebook
date: 04-06-2010
published: true
publish_date: 04-06-2010
# unpublish_date: 04-06-2010
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
    tag: [ce]
module:
    code: 'review_facebook'
    category: [mailbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2010/06/facebook_112.png'
    pro: ''
    cert: ''
    price: ''
    title_en: 'Share Review on Facebook'
    teaser_en: ''
    title_de: 'Bewertung auf Facebook teilen'
    teaser_de: 'Bitte Kunden, ihre Produktbewertung auf Facebook zu teilen'
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

Dieses Modul kontaktiert Kunden nach der Abgabe einer Produkt-Bewertung mit der Möglichkeit, die Bewertung mit einem Klick auf Facebook zu teilen.


Die Email beinhaltet eine Liste der Produkte mit
- Bild
- Link zur Facebook Teilen Seite

Wie bei alle MailBeez Modulen wird der Inhalt der Email basierend auf vorlagen generiert und die Produkt-Liste ist in einer Unter-Vorlage definiert.

Der Facebook Teilen Link zeigt auf die review_info Seite, auf der Anhand der products_id und review_id die Bewertung des Kunden gezeigt wird.

Facebook muss in der Lage sein, den Bewertungs-Text von dieser Seite zu lesen - ggf. die Shopseite anpassen.