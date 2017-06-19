---
# http://learn.getgrav.org/content/headers
title: Status-Änderungs-Benachrichtigung
slug: notification_order_status
date: 01-03-2013
published: true
publish_date: 01-03-2013
# unpublish_date: 01-03-2013
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
    code: 'notification_order_status'
    category: [mailbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2013/03/icon_32.png'
    pro: 'pro'
    cert: 'true'
    price: '49 EUR'
    title_en: 'Notification: Order Status Update'
    teaser_en: 'Notify your customers about an specific order status update, e.g. to send a delivery tracking link'
    title_de: 'Benachrichtigung: Bestell-Status Änderung'
    teaser_de: 'Benachrichtigen Sie Ihre Kunden bei speziellen Bestell-Status Änderungen, z.B. um einen Link zur Paket-Verfolgung zu schicken'
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

Dieses praktische Module sendet bei Änderung des Bestell-Status auf einen oder mehrere konfigurierbare Status eine Benachrichtigung an den Kunden.

Optional kann das Modul nach Versand den Bestell-Status auf einen neuen, wählbaren Status setzen. Ein eventuell vorliegender Kommentar zur Bestellung kann in die Email eingefügt werden.

Die Benachrichtigungs-Emails wird beim nächsten Durchlauf von MailBeez versendet. Um den Zeitversatz zwischen Setzen des Bestell-Status und Versand der Email gering zu halten, empfehlen wir mit Hilfe eines Cronjobs MailBeez z.B. minütlich auszuführen. Der MailBeez Support hilft bei Fragen hierzu.

Anwendungsbeispiele:

- Eine externe Software zur Bestellbearbeitung setzt den Bestellstatus, jedoch ohne eine Benachrichtung zu versenden
- Sie möchten die Standard Bestelltstatus-Email mit einer eigenen Version ersetzen
- Sie möchten Abläufe in Abhängigkeit vom Bestell-Status automatisieren

**Vorlagen Variablen**


| Vorlage-Variable   | Ausgabe                                 |
|--------------------|-----------------------------------------|
| {$status_date}     | formatiertes Datum des Bestell-Status   |
| {$status_date_raw} | unformatiertes Datum des Bestell-Status |
| {$status_id}       | Bestell-Status-ID                       |
| {$status_name}     | Bestell-Status-Name                     |
| {$comments}        | Kommentar                               |

**Beispiel für status-abhängigen Email-Text**

Sie können mit etwas [Smarty.net Code](http://www.smarty.net/docs/en/language.function.if.tpl) beliebige Ausgaben z.B. in Abhängigkeit vom Bestell-Status generieren:

    {if $status_id == 3}
       Ihre Bestellung wurde versendet.
    {/if}



[plugin:content-inject](/content_blocks/pro_responsive_template)
