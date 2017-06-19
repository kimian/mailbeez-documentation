---
# http://learn.getgrav.org/content/headers
title: Trustpilot
slug: trustpilot
routes:
    default: /dokumentation/mailbeez/trustpilot
# menu: Trustpilot
date: 22-05-2010
published: true
publish_date: 22-05-2010
# unpublish_date: 22-05-2010
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
    code: 'trustpilot'
    category: [mailbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2011/03/top_64.png'
    pro: ''
    cert: ''
    price: ''
    title_en: 'Trustpilot'
    teaser_en: ''
    title_de: 'Trustpilot'
    teaser_de: 'Trustpilot macht mehr Besucher zu Kunden. Bis zu 100x mehr Bewertungen auf Trustpilot - arbeitet mit dem Trustpilot Feedback service, welcher eine Email mit Autologin-Link an die Kunden verschickt.'
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


Dieses kostenfreie Modul bitte Kunden automatisch nach der Bestellung um Bewertung auf Trustpilot. Für den professionellen Einsatz empfehlen wir das [Trustpilot Profi](/dokumentation/mailbeez/trustpilot_advanced) Modul als Bestandteil der Profi-Tarife!

**Haben Sie viele zufriedene Kunden, aber wenig positive Bewertungen? Trustpilot’s automatischer Feedback Service sammelt automatisch Bewertungen von Ihren Kunden.**

In enger Zusammenarbeit mit Trustpilot entwickelt und offiziell als Partner-Lösung empfohlen, erweitert das MailBeez Trustpilot Modul den Trustpilot “Automatic Feedback Service”. Das Modul sammelt automatisch die erforderlichen Daten und übermittelt diese kontrolliert an Trustpilot. Trustpilot generiert daraufhin eine “1-Klick”-Email, welche dem Kunden das sofortige Schreiben einer Bewertung erlaubt – dies ergibt bis zu 10x mehr Bewertungen!

**So funktioniert das System:**

- Trustpilot stellt die persönliche Automatic Feedback Service Email Adresse bereit
- Nach dem Kauf sendet das MailBeez Trustpilot Modul nach einem definierten Zeitraum und abhängig vom Bestellstatu eine Email an diese persönliche Email-Adresse.
- Das Trustpilot System extrahiert die erforderlichen Kundeninformationen
- Das System schickt dem Kunden daraufhin eine “1-Klick” Email mit Bitte um Bewertung – der Kunde kann sofort mit dem Schreiben loslegen.
 

Hinweis:

wenn Sie mehrere Sprachen nutzen, bitte in der Email Vorlage die Zeile

```
‘language’ => MAILBEEZ_TRUSTPILOT_LANGUAGE
```

anpassen, so dass die richtige Information zur Kundensprache übermittelt wird.
