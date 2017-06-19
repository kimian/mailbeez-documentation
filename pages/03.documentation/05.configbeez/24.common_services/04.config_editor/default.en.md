---
title: 'Editor and Image Engine'
slug: config_editor
routes:
    default: /documentation/configbeez/config_editor
date: 06-04-2017
published: true
publish_date: 24-03-2014
template: docs
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration_status: done
    category:
        - docs
    tag: [pro]
module:
    code: 'pro'
    category: [pro]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]   
    pro: 'pro'       
author:
    name: admin
metadata:
    author: admin
---

The module "visual editor" is part of a couple of modules, e.g. Newsletter advanced or template manager.

There are following configuration options:

**Root for image browser**

Here you can enter a path relative to your store root directory. The image browser will then open with this path.

Path relativ to store root  
 empty value: browse all images on shop server


**Root for image cache**

Here you can enter a path relative to your store root directory. The MailBeez Image Engine writes Image files into this directory. The cache can be fully regenerated.

With changing the cache path, the cache will be automatically moved, but you should keep the old cache path containing a .htaccess file to support image generation for in earlier sent emails referenced images.


**Mobile Editor width settings**

To support the creating and editing of responsive emails you can switch the editor into different width.

Only change when necessary.

**Mobile Editor View Width 1**: Width for Mobile Editor View 1, e.g. 320px

**Mobile Editor View Width 2**: Width for Mobile Editor View 2, e.g. 480px

**Mobile Editor View Width 3**: Width for Mobile Editor View 3, e.g. 600px
