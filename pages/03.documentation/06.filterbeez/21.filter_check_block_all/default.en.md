---
# http://learn.getgrav.org/content/headers
title: Block Customer Administration Check
slug: filter_check_block_all
# menu: Block Customer Administration Check
date: 16-10-2012
published: true
publish_date: 16-10-2012
# unpublish_date: 16-10-2012
template: docs
# theme: false
visible: false
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration_status: done
    category: [docs]
    tag: [pro]
module:
    code: 'config_block_admin'
    category: [filterbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    pro: 'pro'
    cert: 'true'      
# added collection selector

author:
    name: kelly
metadata:
    author: kelly
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

## Ensure Opted-Out Customers Don’t Get Email

Delivered with the [Advanced Opt-Out with Admin](/documentation/configbeez/config_block_admin/) module, this filter checks for customers who have elected to opt-out of all MailBeez generated emails before sending out emails when an email module is run.
