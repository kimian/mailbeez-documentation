---
title: 'Email Web-view and Archive'
slug: config_email_archive
routes:
    aliases:
        - /documentation/installation/config/config_email_archive

published: true
date: '28-04-2014 00:00'
publish_date: '28-04-2014 00:00'
metadata:
    author: admin
visible: true
template: docs
taxonomy:
    category:
        - docs
    tag: pro
summary:
    enabled: true
    format: short
    size: 128
module:
    code: config_email_archive
    category:
        - configbeez
    compatiblity:
        - comp_osc
        - comp_cre
        - comp_digi
        - comp_zencart
        - comp_xtc
        - comp_xtcm2        
        - comp_gambio
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2014/04/icon_32.png'
    pro: pro
    cert: 'true'
    price: '79 EUR'
    title_en: 'Email Web-view and Archive'
    teaser_en: 'Enrich you MailBeez Emails with a web-view and archive them'
    title_de: 'Email Web-Ansicht und Archiv' 
    teaser_de: 'Erweitern Sie Ihre MailBeez-Emails mit einer Web-Ansicht und archivieren Sie diese.'
    author: MailBeez.com
author:
    name: admin
---

Enhance your MailBeez system with the "Email Web-view and Archive" module:

## Web-view

In the main- or body of your email template, use the variable:

```
<a href="{$webversion_url}">Web-View</a>
```


 When the email recipient clicks this link, they will be redirected to a web version of the email.

## Archive

All Mailbeez generated emails will be automatically archived in both TXT and HTML format. The archived versions can be displayed easily by either the Beez-O-Graph or when working directly with a customer using the free [BeezDesk CRM Customer Insight](/documentation/configbeez/config_customer_insight/) add-on. 

Getting an overview or checking exactly which emails a customer has received has now become a very simple task!


With the help of the integrated "clean-up function", older entries can be deleted in a rule-based manner. This can be performed manually in the module or, if configured accordingly, automatically.

## Configuring an external database

In the default configuration, the e-mail archive is stored in the shop database.
Depending on the email volume, the archive can achieve a size of several GBs despite the automated clean-up function, whereby e.g. backups of the database become more difficult.

In order not to add load to the shop database, a separate database can be configured for the email archive. The steps are quite simple: first, create a new database in the server administration, then configure the access data for this database in the module. In case of connection problems, the module will help you with the appropriate hints.

Since the email archive data are non-critical data, a backup can be omitted. However, the automatic clean-up function should be activated in order to avoid an uncontrolled increase in the database size.