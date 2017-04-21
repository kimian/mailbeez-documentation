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

MailBeez works with osCommerce ms2.2 / rca2, running on PHP 5.2+

The installation is straight forward and can be done in a couple of minutes by following these two steps:

- copy new files
- modify existing files

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


located and open the file

```bash
admin/includes/boxes/tools.php
```


find

```
BOX_TOOLS_WHOS_ONLINE . '</a>'
```


add

```
. '<br><a href="' . tep_href_link(FILENAME_MAILBEEZ, '', 'NONSSL') . '">MailBeez</a><br>'
```


this will add the menu-entry “MailBeez” to your Tools-Box.

Feel free to place this link whereever you want.

[plugin:content-inject](/content_blocks/run_installer)