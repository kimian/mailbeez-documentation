---
# http://learn.getgrav.org/content/headers
title: osCommerce 2.2
slug: basic-installation-oscommerce
# menu: osCommerce 2.2
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

MailBeez arbeitet problemlos mit osCommerce ms2.2 / rca2, auf PHP 5.2+

Die Installation ist in wenigen Schritten erledigt:
- Die neuen Dateien übertragen
- Menü-Eintrag anlegen

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
admin/includes/boxes/tools.php
```


finde

```
BOX_TOOLS_WHOS_ONLINE . '</a>'
```


Danach in einer neuen Zeile folgendes einfügen:


```
. '<br><a href="' . tep_href_link(FILENAME_MAILBEEZ, '', 'NONSSL') . '">MailBeez</a><br>'
```


hierdurch wird der Menü-Eintrag “MailBeez” in die Tools-Box gesetzt.


[plugin:content-inject](/content_blocks/run_installer)