---
# http://learn.getgrav.org/content/headers
title: Content Integration Suite
slug: filterbeez_add_content_suite
# menu: Content Integration Suite
date: 11-08-2011
published: true
publish_date: 11-08-2011
# unpublish_date: 11-08-2011
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
    code: 'filterbeez_add_content_suite'
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

**under development**
    

this module works in combination with the [profiling engine](/documentation/configbeez/config_profiling_engine) and the content partials of the [Template Manager with multilanguage Support](/documentation/configbeez/config_tmplmngr_lng) you can personalize the email content by assigned customer and/or order profile tags.


follow this preparation steps:

- create profiles with rules to tag orders / customers
- create content partials

then

configure which tags must or must not be assigned to customer / orders to add the specific content partial. If there are multiple matching content partials all of them are added in the assigned sort order.

finally edit the email template (can be a body template or the main template) and insert the content block "Profiling content" from within the visual editor (move mouse on an element, click on the + icon, select the element to insert)


