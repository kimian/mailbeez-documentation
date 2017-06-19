---
# http://learn.getgrav.org/content/headers
title: Add ShopperApproved Ratings to Emails
menu: Add ShopperApproved Ratings
slug: filter_add_shopperapproved
published: true
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
    tag: [pro]
module:
    code: 'config_shopperapproved_integration'
    category: [filterbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    pro: 'pro'
    cert: 'true'       
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

Automatically add your store’s ShopperApproved reviews into any MailBeez email campaign with this filter, part of the [ShopperApproved Integration Suite](/documentation/configbeez/config_shopperapproved_integration/ "ShopperApproved Integration Suite"); perfect for spicing up the [Winback](/documentation/mailbeez/winback_advanced/ "Winback Advanced Module") and [No Purchase](/documentation/mailbeez/nopurchase_advanced/ "Mailbeez No Purchase Modules") Mailbeez modules.

### Usage

Install and activate this Module – you need to have the [ShopperApproved Integration Suite](/documentation/configbeez/config_shopperapproved_integration/ "ShopperApproved Integration Suite") configured.

By adding the following tags into your MailBeez templates you will be able to show a configured number of ShopperApproved ratings in your MailBeez generated emails. You can place the tags wherever you want, so for example if you place them within your main template the ratings will be shown in all emails, but if you place them only in your content template, you are able control exactly in which emails the ratings will be visible:

Place this into the HTML-Version of your MailBeez template:

```
{$content.shopperapproved.html}
```

Place his into the TXT-Version of your MailBeez template:

```
{$content.shopperapproved.txt}
```



More advanced users can also directly access the data object holding the ratings in the email template using following code example.


```
{assign var=feed_feed value=$data.shopperapproved}
{section name=item loop=$feed_feed}
  {$feed_feed[item].stars_overall}
  {$feed_feed[item].customers_textcomments}</br>
  {$feed_feed[item].customers_fullurl}</br>
  {$feed_feed[item].customers_displaydate|date_format}
{/section}
```


 