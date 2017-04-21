---
# http://learn.getgrav.org/content/headers
title: modified-shop 1.0x
slug: basic-installation-modified-shop
# menu: modified-shop 1.0x
date: 12-09-2010
published: true
publish_date: 12-09-2010
# unpublish_date: 12-09-2010
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

MailBeez arbeitet problemlos mit **xtc-modified / modified-shop 1.05** auf PHP 5.2+.

Die Installation ist in wenigen Schritten erledigt und sollte nicht mehr als ein paar Minuten dauern (es sei denn, der FTP Transfer ist sehr langsam…)

- Neue Dateien kopieren
- Eine Datei anpassen
- Admin Rechte setzen (halb automatisch)
- MailBeez installieren

MailBeez verwaltet eigene Datenbank-Tabellen – die Tabellen des Shop-Systemes werden nicht berührt.

## Schritt 1 – Neue Dateien kopieren

[plugin:content-inject](/content_blocks/download_installer)


Aus dem Ordner “catalog” folgende Dateien in das Root-Verzeichnis des Shops  (dort, wo sich die index.php befindet) kopieren

```bash

 /admin/mailbeez.php

 /mailhive (folder)
 /mailhive.php

```

## Schritt 2 – Datei anpassen

### 1. Menü-Eintrag hinzufügen

**Modified Shop bis V1.05**  
 folgende Datei finden und öffnen:

 
```bash

 /admin/includes/column_left.php


```

dort

```bash


 ' . BOX_IMPORT . '</a><br>';


```

finden und folgendes danach einfügen:

```bash


if (($_SESSION['customers_status']['customers_status_id'] == '0') && ($admin_access['module_newsletter'] == '1')) echo '<li><a href="' . xtc_href_link('mailbeez.php') . '" class="menuBoxContentLink" > -MailBeez</a></li>';


```

**Modified Shop ab V1.06**  
 folgende Datei finden und öffnen:

```bash


 /admin/includes/column_left.php
 

```


dort

```


 //----HILFSPROGRAMME


```

finden und folgendes vor der Zeile


```
 
 
echo ('</ul>');


```


einfügen:


```

if (($_SESSION['customers_status']['customers_status_id'] == '0') && ($admin_access['module_newsletter'] == '1')) echo '<li><a href="' . xtc_href_link('mailbeez.php') . '" class="menuBoxContentLink" > -MailBeez</a></li>';


```

## Schritt 3 - Zugriffsrechte vergeben

einmalig im Browser

```bash

 (shop-url)/mailhive.php
 

```

aufrufen.

Hierdurch werden die erforderlichen Admin-Rechten für den HAUPT-Admin vergeben.
Falls erforderlich dann Zugriffs-Rechte im Admin System für weitere Admin-user vergeben.

[plugin:content-inject](/content_blocks/run_installer)
