---
# http://learn.getgrav.org/content/headers
title: Gutschein-Ablauf Erinnerung
slug: coupon_expire
routes:
    aliases:
        - /dokumentation/mailbeez/gutschein-ablauf-erinnerung
# menu: Gutschein: Ablauf Erinnerung
date: 03-09-2010
published: true
publish_date: 03-09-2010
# unpublish_date: 03-09-2010
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
    tag: [pro,coupon]
module:
    code: 'coupon_expire'
    category: [mailbeez]
    compatiblity: [comp_cre,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2011/10/coupon_32.png'
    pro: 'pro'
    cert: 'true'
    price: '79 EUR'
    title_en: 'Coupon Expiry Reminder'
    teaser_en: ''
    title_de: 'Gutschein-Ablauf Erinnerung'
    teaser_de: ''
    author: 'MailBeez.com'
author:
    name: admin
metadata:
    author: admin

---

**Gutscheine drohen, ungenutzt zu verfallen? Abhilfe kann hier die automatische Erinnerungsmail bringen.**

Wie Sie sicher wissen, haben personalisierte Ecommerce Email Kamapagnen die höchsten Rendite aller Werbeformen – und deshalb ist die Mailbox des Kunden ein heiss umworbener Platz. Wenn Sie sicherstellen wollen, dass Gutschein Kampagnen optimale Resultate erzielen, ist eine Erinnerung vor Ablauf des datierten Gutscheines ein wertvolles Hilfsmittel.

**Eine automatisierte und intelligente Lösung**

Wie alle MailBeez Kampagnen Module, so ist auch die Gutschein Ablauf Erinnerung – einmal installiert, angepasst und konfiguert – ein voll-automatisches Module welches prüft, welche Gutschein noch ungenutzt sind und im konfigurierten Zeitraum verfallen. Die entsprechenden Kunden werden dann per Email erinnert.

Natürlich ist das Modul so intelligent aufgebaut, dass nicht mehr gültige Gutschein ausgeschlossen werden – es werden nur Kunden kontaktiert, die ihren personalisierten Gutschein noch nicht genutzt haben.

[plugin:content-inject](/content_blocks/pro_responsive_template)
 

**Einstellungen**

Dieses Module hat neben den üblichen Konfigurationsparametern zwei Einstellungen, um den Zeitrahmen vor Ablauf des Gutscheines zu bestimmen:

- **Mindest Anzahl Tage vor Ablauf (A) ** Der Gutschein ist mindestens noch diese Anzahl Tage gütig
- **Maxium Anzahl Tage vor Ablauf (B) **Der Gutschein ist höchstens noch diese Anzahl Tage gütig (“in weniger als X Tagen verliert der Gutschein seine Gültigkeit)

**Beispiel:**

A auf 5, B ist auf 7 gesetzt:

Mit diesen Einstellungen wird das Module alle Kunden kontaktieren, welche einen von MailBeez generierte Gutschein erhalten aber nicht genutzt haben, dessen Gültigkeit in weniger als 7 aber mehr als 5 Tage abläuft.
