---
# http://learn.getgrav.org/content/headers
title: Gambio GX 1.x
slug: basic-installation-gambio
# menu: Gambio GX 1.x
date: 08-09-2010
published: true
publish_date: 08-09-2010
# unpublish_date: 08-09-2010
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
    tag: [ftp]
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


MailBeez arbeitet problemlos mit *Gambio GX 1.x*.

Die Installation ist in wenigen Schritten erledigt:
- Die neuen Dateien übertragen
- Menü-Eintrag anlegen (frühe Gambio 2 Versionen)
- Zugriffs-Rechte für den Admin vergeben (halb automatisch)
- MailBeez per Button-Klick installieren

MailBeez verwaltet eigene Tabellen - die vorhandenen Shop-Tabellen werden nicht verändert.



## Schritt 1: Neue Dateien

[plugin:content-inject](/content_blocks/download_installer)


folgende Dateien und Ordner aus dem entpackten Zip-Archiv auf den Shop-Server übertragen:


```bash
admin/mailbeez.php
mailhive/
mailhive.php


```




## Schritt 2 - Menü-Eintrag anlegen


folgende Datei öffnen:

```bash 
admin/includes/column_left.php  


```


finde

``` 
' . BOX_IMPORT . '</a><br>';


```


Danach in einer neuen Zeile folgendes einfügen:



``` 
if (($_SESSION['customers_status']['customers_status_id'] == '0') && ($admin_access['mailbeez'] == '1')) 
    echo '<li class="leftmenu_body_item"><a class="fav_drag_item" href="' . xtc_href_link('mailbeez.php') . '"> MailBeez</a></li>';

```



## Schritt 3 - Zugriffsrechte vergeben

einmalig


```
http://(shop)/mailhive.php


```


im Browser aufrufen.

Hierdurch werden die erforderlichen Admin-Rechten für den HAUPT-Admin vergeben.
Nach einem erneuten Login und leeren des Seiten-Caches wird MailBeez im Admin Menü erscheinen.
Falls erforderlich dann Zugriffs-Rechte im Gambio-Admin System für weitere Admin-user vergeben



[plugin:content-inject](/content_blocks/run_installer)



