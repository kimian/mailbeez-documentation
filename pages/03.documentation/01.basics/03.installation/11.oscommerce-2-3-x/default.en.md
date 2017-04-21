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

MailBeez works with osCommerce 2.3.1, running on PHP 5.2+

The installation is straight forward and can be done in a couple of minutes by following these two steps:

- copy new files
- add menu entry



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


## Step 2 – add menu entry

depending on your version you can either use the admin plugin or manually add the menu entry:

### A. Admin Plugin

since oscommerce 2.3.3 a plugin system for adding admin entries is available. For this version please copy

```bash
extra_files/extras_osc_233x/admin/includes/boxes/customers/mailbeez.php
```

into your oscommerce system:

```bash
admin/includes/boxes/customers_mailbeez.php
```


### B. Add a menu entry

located and open the file

```bash
admin/includes/boxes/tools.php
```

find

```
    array(
        'code' => FILENAME_WHOS_ONLINE,
        'title' => BOX_TOOLS_WHOS_ONLINE,
        'link' => tep_href_link(FILENAME_WHOS_ONLINE)
    )
```

add

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


this will add the menu-entry “MailBeez” to your Tools-Box.

Feel free to place this link whereever you want.

Open the MailBeez System and start exploring!

[plugin:content-inject](/content_blocks/run_installer)