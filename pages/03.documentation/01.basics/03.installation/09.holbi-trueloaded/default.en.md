---
# http://learn.getgrav.org/content/headers
title: Holbi Trueloaded
slug: holbi-trueloaded
# menu: Holbi Trueloaded
date: 04-12-2012
published: true
publish_date: 04-12-2012
# unpublish_date: 04-12-2012
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

MailBeez works with Holbi TrueLoaded, running on php 5.3+

The installation is straight forward and can be done in a couple of minutes by following these three steps:

- copy new files
- modify existing files
- add admin access rights

### Requirements

You need to be able to upload new files to your TrueLoaded shopping cart system and modify existing ones.


## Step 1 – copy new files

[plugin:content-inject](/content_blocks/download_installer)


In the mailbeez_installer-v3.xx fileset, navigate to catalog > admin, then copy the following file to your TrueLoaded admin-directory.

```bash
mailbeez.php
```


In the mailbeez_installer-v3.xx fileset, navigate to the catalog folder, then copy the following file and folder to your Trueloaded root directory (where your index.php is located).

```bash
mailhive (folder)
mailhive.php
```


## Step 2 – modify existing files

### Add a menu entry

In your Trueloaded shopping cart system files, locate and open the file:

```bash
admin/includes/boxes/tools.php
```


find

```
tep_admin_files_boxes(FILENAME_WHOS_ONLINE, BOX_TOOLS_WHOS_ONLINE) .
```


add a new line with the following text:

```
 // mailbeez
 tep_admin_files_boxes('mailbeez.php', 'MailBeez') .
 // - mailbeez
```
 

this will add the menu-entry “MailBeez” to your Tools-Box.

## Step 3: add admin access

### Add File Access

Administrator > File Access

1. Click Folder “Tools”
2. Click Button “store files”
3. Select “mailbeez.php” in dropdown list
4. Click Button “save”

### Assign Access Rights

Administrator > Member Groups

1. Click Button “Groups”
2. Select the Group you would like to give access to MailBeez
3. Click Button “new permission”
4. Check mailbeez.php in section “Tools”

repeat for any group you would like to give access to MailBeez

[plugin:content-inject](/content_blocks/run_installer)
