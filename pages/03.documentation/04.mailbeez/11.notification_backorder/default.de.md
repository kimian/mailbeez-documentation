---
# http://learn.getgrav.org/content/headers
title: Rückstands-Benachrichtigung 
slug: notification_backorder
date: 17-12-2013
published: true
publish_date: 17-12-2013
# unpublish_date: 17-12-2013
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
    code: 'notification_backorder'
    category: [mailbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2013/03/icon_32.png'
    pro: 'pro'
    cert: 'true'
    price: '139 Eur'
    title_en: 'Notification: Backorder'
    teaser_en: 'notify your customers about products in backorder'
    title_de: 'Benachrichtigung Bestell-Rückstand'
    teaser_de: 'Informieren Sie Ihre Kunden laufend über Produkte im Rückstand'
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

*Der Kunde hat einen Artikel bestellt, der gerade oder noch nicht auf Lager ist. Dieser Artikel ist in Rückstand und der Kunde wartet darauf.*

*Etwa alle 2 Tage fragt der Kunde jetzt nach, wann der Artikel lieferbar ist...*

**Hört sich das bekannt an?**

Dann sollten Sie sich das Modul "Benachrichtigung Bestell-Rückstand" genauer ansehen:

Basierend auf dem "Verfügbar ab" Datum (Datenbank-Feld products_date_available) ermittelt das Modul, ob eine Bestellung ein Produkt enthält, welches gerade oder noch nicht auf Lager ist.

Und weil es das Verfügbarkeits-Datum protokolliert, kann es Änderungen erkennen und dann gleich eine Benachrichtigung senden.

Das Modul versendet folgende 3 Arten von Benachrichtigungs-Emails:

### 1. Email - Vorstellung des Benachrichtigungs-Services

Ein bestelltes Produkt ist in Rückstand? Dann erhält der Kunde sofort eine erste Email gleich nach der Bestellung, in welcher Benachrichtigungs-Service vorgestellt wird:

> Lieber Kunde,   
>   
>  mindestens einer der bestellten Artikel ist in Rückstand.   
>   
>  Wir werden Sie alle 2 Tage oder auch sofort bei Änderung des erwarteten Lieferdatums informieren.   
>   
>  Folgende Artikel sind in Rückstand:   
>   
>  (Liste der Artikel mit Verfügbarkeits-Datum)

### 2. Email - Informieren Sie den Kunden laufend

Diese 2. Email wird periodisch z.B. alle 3 Tage gesendet, um den Kunden laufend über die Artikel in Rückstand zu informieren. Ein toller Service, um die Wartezeit zu verkürzen und auch die Geduld des Kunden zu wertschätzen.

> Lieber Kunde,   
>   
>  mindestens einer der bestellten Artikel ist in Rückstand.   
>   
>  Wir wissen, dass Sie auf diesen Artikel warten und freuen uns über Ihre Geduld. Sobald es Neuigkeiten gibt, werden wir Sie benachrichtigen!   
>   
>  Folgende Artikel sind in Rückstand:   
>   
>  (Liste der Artikel mit Verfügbarkeits-Datum)

### 3. Email - Sofort den Kunden bei Änderung informieren

Diese Email wird sofort versendet, wenn sich das Verfügbarkeits-Datum ändert!

> Lieber Kunde,   
>   
>  Es tut sich was!   
>   
>  Das Verfügbarkeits-Datum der fehlenden Artikel hat sich wie folgt geändert:   
>   
>  (Liste der Artikel mit altem und neuem Verfügbarkeits-Datum)

## Arbeitserleichterung bei voller Kontrolle

Einmal eingerichtet wird dieses Modul auf Autopilot arbeiten (erfordert, dass MailBeez entsprechend automatisiert ist). Basierend auf einem oder mehr Bestellstatus kann konfiguriert werden, welche Bestellungen verarbeitet werden können.

So viel Kontrolle wie nötig und so viel Automatisierung wie möglich!

[plugin:content-inject](/content_blocks/pro_responsive_template)
