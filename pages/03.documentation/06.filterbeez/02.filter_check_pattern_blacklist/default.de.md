---
# http://learn.getgrav.org/content/headers
title: Musterbasierte Blacklist
slug: filter_check_pattern_blacklist
routes:
    aliases:
    - /dokumentation/filterbeez/musterbasierte-blacklist
# menu: Musterbasierte Blacklist
date: 26-09-2011
published: true
publish_date: 26-09-2011
# unpublish_date: 26-09-2011
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
   code: 'filter_check_pattern_blacklist'
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

Dieser Filter blockiert MailBeez für alle Email-Adressen, die einem bestimmten Muster entsprechen, z.B. `@marketplace.amazon.de`.

Es können unbegrenzte Muster wie `@marketplace.amazon.de` defniert werden , ein Muster je Linie. Emails, die dieses Muster enthalten, werden blockiert.
