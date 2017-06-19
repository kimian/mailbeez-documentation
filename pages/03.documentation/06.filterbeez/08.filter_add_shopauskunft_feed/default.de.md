---
# http://learn.getgrav.org/content/headers
title: Shopauskunft Bewertungen in Emails einfügen
slug: filter_add_shopauskunft_feed
menu: Shopauskunft Bewertungen einfügen
date: 03-05-2011
published: true
publish_date: 03-05-2011
# unpublish_date: 03-05-2011
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
    code: 'config_shopauskunft_rss_importer'
    category: [filterbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    pro: 'pro'
    cert: 'true'      
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

Fügen Sie Ihre wertvollen Shopauskunft Bewertungen automatisch in Ihre MailBeez Email Kampagnen ein – hervorragend geeignet, um z.B. die Emails zur [Kundenrückgewinnung](/dokumentation/mailbeez/winback_advanced) und [Kunden ohne Kauf](/dokumentation/mailbeez/nopurchase_advanced) aufzuwerten.

Dieses Hilfsmodule ist Teil der [Shopauskunft Integration Suite](/dokumentation/configbeez/config_shopauskunft_rss_importer/ "Shopauskunft Integration Suite").

### Installation

Modul installieren und aktivieren – vorher die [Shopauskunft Integration Suite](/dokumentation/configbeez/config_shopauskunft_rss_importer/ "Shopauskunft Integration Suite") konfigurieren und testen.

Mit folgenden Platzhaltern können Sie die konfigurierte Anzahl an Bewertungen in von MailBeez generierten Emails einfügen. Die Platzhalter können an jeder beliebigen Stellen in den MailBeez Vorlagen eingefügt werden. Sollen die Bewertungen in allen Emails sichtbar sein, am besten die Platzhalter direkt in die Hauptvorlage einfügen

Platzhalter für die HTML-Version der Vorlage:

```
{$content.rss.shopauskunft.html}
```

Platzhalter für die TXT-Version der Vorlage:

```
{$content.rss.shopauskunft.txt}
```

Die Vorlage für die Darstellung der Bewertungen ist folgende Datei

```
rss_email_html.tpl  
rss_email_txt.tpl
```

welche in folgendem Ordner liegt:

`mailhive\configbeez\config_shopauskunft_rss_importer\templates`

Fortgeschrittene Benutzter können auch das Daten-Object mit den Bewertungen direkt im Email Template verwenden:


```
{assign var=feed_feed value=$data.feed.shopauskunft}
{section name=item loop=$feed_feed}
  {$feed_feed[item].rating_stars}
  {$feed_feed[item].text}</br>
  {$feed_feed[item].user_deeplink}</br>
  {$feed_feed[item].date|date_format}
{/section}
```


### Optionen:

**Anzahl Bewertungen**  
 Anzahl Bewertungen in den Emails (Zahl)

**Mindestanzahl Sterne**  
 Nur Bewertungen mit mindestens diese Anzahl Sterne anzeigen (3-5)

**Zufällige Reihenfolge**  
 Zufällige Reihenfolge (True) oder chronologische Reihenfolge (False)

 