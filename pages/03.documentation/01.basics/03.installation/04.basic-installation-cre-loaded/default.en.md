---
# http://learn.getgrav.org/content/headers
title: CRE Loaded
slug: basic-installation-cre-loaded
# menu: CRE Loaded
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

MailBeez works with CRE_Loaded_PCI_CE_v6.4.1a, running on PHP 5.2.11

The installation is straight forward and can be done in a couple of minutes by following this single step:

- copy new files

MailBeez is maintaining it’s own tables – the shops existing table stay as they are.

## Step 1 – copy new files

[plugin:content-inject](/content_blocks/download_installer)

The “Quickstart Package” Zip-File contains several folders. The Folder “catalog” contains the files and folders you need to copy into your Shop Root.

Copy following file and folder to your Shop Root (where your index.php is located)

```bash
catalog/admin/mailbeez.php -> admin/mailbeez.php  
catalog/mailhive -> mailhive (folder)  
catalog/mailhive.php -> mailhive.php

```

and the CRE Loaded specific “drop-in installation files” located in

```bash
 (MailBeez package) / extras_creloaded

```

into their locations:

```bash
admin/includes/runtime/applicationtop/MAILBEEZ_applicationtop_bottom.php  
admin/includes/runtime/marketing/MAILBEE_marketing_boxesbottom.php  
includes/runtime/applicationtop/MAILBEEZ_applicationtop_bottom.php

```
 

## Step 2 (CRE Loaded B2B) – add admin rights

the B2B version of CRE Loaded supports admin rights. After copying the files into CRE Loaded you need to grant access to the MailBeez system with following steps:

1. go to “Administrator > Menu File Access”
2. Click on line item “Marketing”
3. Click Button “Insert File”
4. Choose “mailbeez.php” in the drop-down list & save the settings

Now you find the Menu item “MailBeez” under “Marketing” in the admin menu


[plugin:content-inject](/content_blocks/run_installer)
