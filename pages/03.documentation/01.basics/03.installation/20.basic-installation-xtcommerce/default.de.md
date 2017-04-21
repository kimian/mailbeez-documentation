---
# http://learn.getgrav.org/content/headers
title: xtCommerce 3.04
slug: basic-installation-xtcommerce
# menu: xtCommerce 3.04
date: 21-05-2010
published: true
publish_date: 21-05-2010
# unpublish_date: 21-05-2010
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

MailBeez arbeitet problemlos auf **xt:Commerce Version 3.04**.

Die Installation ist in wenigen Schritten erledigt:

- Die neuen Dateien übertragen
- Menü-Eintrag anlegen
- Zugriffs-Rechte für den Admin vergeben (halb automatisch)
- MailBeez per Button-Klick installieren

MailBeez verwaltet eigene Tabellen - die vorhandenen Shop-Tabellen werden nicht verändert.


## Schritt 1 - Die neuen Dateien übertragen

[plugin:content-inject](/content_blocks/download_installer)


folgende Datei in das admin-Verzeichnis kopieren

```
catalog/admin/mailbeez.php

```

folgende Dateien und Ordner in den Shop-Root kopieren

```
catalog/mailhive (Ordner)  
catalog/mailhive.php

```

## Schritt 2 - Menü-Eintrag anlegen

### 1. Add a menu entry

folgende Datei öffnen:

```bash
admin/includes/column_top.php

```
danach folgendes einfügen


```
 if (($_SESSION['customers_status']['customers_status_id'] == '0') && ($admin_access['module_newsletter'] == '1')) echo '<li><a href="' . xtc_href_link('mailbeez.php') . '"> -MailBeez</a></li>';
 
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