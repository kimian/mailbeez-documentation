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



The Installation of MailBeez is successfully tested with *xt:Commerce Version* 3.04, running on PHP 5.2.11

The installation is straight forward and can be done in a couple of minutes by following these steps:

- copy new files
- add permission (half automatic)
- Install MailBeez

MailBeez is maintaining it’s own tables – the shops existing table stay as they are.

## Step 1 – copy new files

[plugin:content-inject](/content_blocks/download_installer)


copy following file to your admin-directory

```bash

 mailbeez.php

```

copy following file and folder to your catalog-directory (where your index.php is located)

```bash


mailhive (folder)
mailhive.php


```


## Step 2 – modify existing files

### 1. Add a menu entry

located and open the file

```bash


admin/includes/column\_left.php

```

find

```bash


' . BOX_IMPORT . '</a><br>';


```


add

```bash


 if (($_SESSION['customers_status']['customers_status_id'] == '0') && ($admin_access['module_newsletter'] == '1')) echo '<li><a href="' . xtc_href_link('mailbeez.php') . '"> -MailBeez</a></li>';

```
this will add the menu-entry “MailBeez” to your Tools-Box. Feel free to place this link whereever you want.

## Step 3 – add permission

run

```bash

 (shop)/mailhive.php

```

this will add the required permission for MailBeez for the primary admin account.

If necessary add admin permission for MailBeez for secondary admin accounts as well.

[plugin:content-inject](/content_blocks/run_installer)
