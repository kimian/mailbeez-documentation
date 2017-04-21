---
# http://learn.getgrav.org/content/headers
title: Zen Cart 1.5.x
slug: basic-installation-zen-cart-1-5-x
# menu: Zen Cart 1.5.x
date: 01-02-2012
published: true
publish_date: 01-02-2012
# unpublish_date: 01-02-2012
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

MailBeez works with **Zen Cart v1.5.x** running on PHP 5.2+


The installation is straight forward and can be done in a couple of minutes by following these steps:

- copy new files
- install MailBeez

MailBeez maintains its own tables – the shopping cart's existing tables remain as they are... unchanged.


## Step 1 – copy new files

[plugin:content-inject](/content_blocks/download_installer)


In the mailbeez_installer-v3.xx fileset, navigate to **catalog > admin**, then copy the following file to your Zen-Cart admin-directory. 

```bash
 mailbeez.php

```


In the mailbeez_installer-v3.xx fileset, navigate to the **catalog** folder, then copy the following file and folder to your root Zen Cart directory (where your index.php is located).

```bash
mailhive (folder)
mailhive.php

```

In the mailbeez_installer-v3.xx fileset, navigate to **extra_files > extra_zencart > zencart_1.5.x > admin**, then copy/merge its contents into your Zen Cart admin-directory.

## Step 2 – install MailBeez

Log in to your zen-cart administration panel. From the navigation bar, select **Tools > MailBeez**. Then, click the “Install” button.


## Adaption of Zen Cart

####changes to your .htaccess rewrite rules

Please add following condition

    # Don't rewrite MailBeez directory
    RewriteCond %{REQUEST_URI} !^/mailhive [NC]
       
as a new line above

    # Handle all other URIs using Zen Cart (its index.php)


####Fix the email function

The Zen Cart email function is peculiar when sending custom emails, and you may experience some minor issues when sending MailBeez generated emails through Zen Cart. See FAQ:

>>>>> Please see [Zen Cart FAQ](/documentation/frequently-asked-questions#zen-cart) for more details

**Quick Solution:** configure a SMTP Email Server in MailBeez > Configuration > Email Engine. This will bypass the Zen Cart email function and give MailBeez full control for sending emails.

If you would like MailBeez to use its own template system to generate MailBeez email (recommended), rather than integrating with and using Zen Cart’s email template system to generate MailBeez email (default), please do the following:

1. Using your FTP program, download includes/functions/functions\_email.php from your server to your local drive (i.e. your computer)
2. Using a text editing program such as Notepad or Notepad++, find this line of code:


`$email_html = zen_build_html_email_from_template($module, $block);`

1. And change it as described on:  
<http://www.zen-cart.com/showthread.php?158085-Mailbeez-After-Sales-Modules&p=1170912#post1170912>

This code change tells Zen Cart to check if the content contains a valid html tag, and if not, applies the Zen Cart template system.

[plugin:content-inject](/content_blocks/run_installer)
