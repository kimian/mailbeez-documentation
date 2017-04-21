---
# http://learn.getgrav.org/content/headers
title: Digistore up to 4.0
slug: digistore
# menu: Digistore up to 4.0
date: 24-08-2010
published: true
publish_date: 24-08-2010
# unpublish_date: 24-08-2010
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

MailBeez works with *DigiStore 4.0*, running on PHP 5.2+

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

admin/advanced_menu.php


```

find

```bash

 stm_aix("p7i3","p0i0",[0,"    <?php echo   BOX_CONFIGURATION_EMAIL_OPTIONS?>  ","","",-1,-1,0,"configuration.php?gID=12"]);


```

add in a new line

```bash

 stm_aix("p7i3","p0i0",[0,"    MailBeez   ","","",-1,-1,0,"mailbeez.php"]);
 

```

this will add the menu-entry “MailBeez” to your Email-Menu item.

Feel free to place this link whereever you want.


[plugin:content-inject](/content_blocks/run_installer)