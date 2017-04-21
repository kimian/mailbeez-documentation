---
# http://learn.getgrav.org/content/headers
title: osCommerce 2.3.x
slug: oscommerce-2-3-x
# menu: osCommerce 2.3.x
date: 26-01-2011
published: true
publish_date: 26-01-2011
# unpublish_date: 26-01-2011
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

MailBeez arbeitet problemlos mit *osCommerce 2.3.x*.


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

Je nach osCommerce Version können Sie entweder das Admin Plugin nutzen oder den Menü-Eintrag in den Code einfügen:

### A. Admin Plugin

Seit osCommerce 2.3.3 gibt es ein Plugin-System zum Hinzufügen von Admin Menü-Einträgen. Kopieren Sie hierzu

```bash
extra_files/extras_osc_233x/admin/includes/boxes/customers/mailbeez.php
```

in das osCommerce System:

```bash
admin/includes/boxes/customers_mailbeez.php
```


### B. Code Änderung

Diese Datei zum Bearbeiten öffnen:

```bash
admin/includes/boxes/tools.php
```

Die Zeile

```
    array(
        'code' => FILENAME_WHOS_ONLINE,
        'title' => BOX_TOOLS_WHOS_ONLINE,
        'link' => tep_href_link(FILENAME_WHOS_ONLINE)
    )
```

finden und folgenden Code hinzufügen:

```
// mailbeez
     ,
     array(
         'code' => 'mailbeez.php',
         'title' => 'MailBeez',
         'link' => tep_href_link('mailbeez.php')
     )
     // - mailbeez
```


Hiermit wird der Admin-Menü Eintrag angelegt.


[plugin:content-inject](/content_blocks/run_installer)

