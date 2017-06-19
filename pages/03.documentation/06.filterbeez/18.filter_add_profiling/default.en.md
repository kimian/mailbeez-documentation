---
# http://learn.getgrav.org/content/headers
title: Add Profiling Data 
slug: filterbeez_add_profiling
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
    

this module works in combination with the [profiling engine](/documentation/configbeez/config_profiling_engine) and adds

Orders Profiles

```
{$data.profiles.order.profiles} - CSV string with all assigned profile_ids e.g "2,6,9"
{$data.profiles.order} - array with all assigned profiles
{$data.profiles.order.<profile_id>} - array if profile with <profile_id> is set

```


Customer Profiles
```
{$data.profiles.customer.profiles} - CSV string with all assigned profile_ids e.g "2,6,9"
{$data.profiles.customer} - array with all assigned profiles
{$data.profiles.customer.<profile_id>} - array if profile with <profile_id> is set

```

Example

```
{if is_array($data.profiles.order.6)}
   this order has profile tag 6
{/if}
{if is_array($data.profiles.customer.42)}
   this customer has profile tag 42
{else}
   Hey
{/if}
```
