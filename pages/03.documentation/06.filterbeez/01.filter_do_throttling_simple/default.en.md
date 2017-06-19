---
# http://learn.getgrav.org/content/headers
title: Simple Throttling
slug: filter_do_throttling_simple
routes:
    - aliases: /documentation/filterbeez/simple-throttling
# menu: Simple Throttling
date: 08-04-2011
published: true
publish_date: 08-04-2011
# unpublish_date: 08-04-2011
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
   code: 'filter_do_throttling_simple'
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

**Control Your Email Send Rate**

>>>>>>We strongly recommend to [ configure Newsletter2Go as your  Email-Engine](/documentation/configbeez/config_email_engine). Then you don't have to worry about any sending limits.



Simple Throttling allows you to configure the **hourly rate** and **total number of emails** that MailBeez sends . This is useful because many hosting companies place a limit on how many emails can be sent out at once and in total. Accounts exceeding these limits can trigger automatic spam alerts that hosting companies have in place to protect their servers.

Simple Throttling keeps you in good standing with your hosting service provider and helps you ensure that your site is still responsive to visitors while sending out emails behind the scenes.

Just drop-in the module, activate it and configure the hourly rate and total number of emails to sent – done.
