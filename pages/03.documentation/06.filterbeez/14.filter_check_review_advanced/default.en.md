---
# http://learn.getgrav.org/content/headers
title: Review Advanced Cross Check
slug: filter_check_review_advanced
# menu: Review Advanced Cross Check
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
    code: 'review_advanced'
    category: [filterbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    pro: 'pro'
    cert: 'true' 

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

## Don’t Duplicate Your Emails

Delivered with the [Review Reminder Advanced with Autologin](/documentation/mailbeez/review_advanced/) module, this filter checks for customers who have blocked or already received Review Reminder emails from the Review Reminder Simple module before sending out emails when the Review Reminder Advanced module is run.

If you were running the Simple version of the module prior to installing the Advanced version, this filter ensures that customers won’t receive the same email twice (once from each version), or at all if they have opted-out.

If you begin using the Review Reminder Advanced module without ever having run the Review Reminder Simple module, then there is no need to enable this filter.
