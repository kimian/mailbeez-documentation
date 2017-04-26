---
# http://learn.getgrav.org/content/headers
title: Digistore 4.1
slug: digistore-2
# menu: Digistore 4.1
date: 22-09-2011
published: true
publish_date: 22-09-2011
# unpublish_date: 22-09-2011
template: docs
# theme: false
visible: false
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

MailBeez workswith *DigiStore 4.1*, running on php 5.3+

If MailBeez is not included in your DigiStore 4.1+ release please follow these instructions

The installation is straight forward and can be done in a couple of minutes by following these two steps:

- copy new files
- modify existing files

## Step 1 – copy new files

[plugin:content-inject](/content_blocks/download_installer)


The “Quickstart Package” Zip-File contains several folders. The Folder “catalog” contains the files and folders you need to copy into your Shop Root.

Copy following file and folder to your Shop Root (where your index.php is located)

```bash

catalog/admin/mailbeez.php -> admin/mailbeez.php  
catalog/mailhive -> mailhive (folder)  
catalog/mailhive.php -> mailhive.php

```

## Step 2 – modify existing files

### 1. Add a menu entry

located and open the file

```bash

admin/includes/boxes/email.php

```

find

```bash


'<a href="' . tep_href_link(FILENAME_CONFIGURATION, 'gID=12', 'NONSSL') . '" class="menuBoxContentLink">' . BOX_CONFIGURATION_EMAIL_OPTIONS . '</a>');


```

replace with


```bash


 '<a href="' . tep_href_link(FILENAME_CONFIGURATION, 'gID=12', 'NONSSL') . '" class="menuBoxContentLink">' . BOX_CONFIGURATION_EMAIL_OPTIONS . '</a>'.
 '<a href="' . tep_href_link('mailbeez.php', '', 'NONSSL') . '" class="menuBoxContentLink">Mail Beez</a>');

```

this will add the menu-entry “MailBeez” to your Email-Menu item.

Feel free to place this link whereever you want.


[plugin:content-inject](/content_blocks/run_installer)