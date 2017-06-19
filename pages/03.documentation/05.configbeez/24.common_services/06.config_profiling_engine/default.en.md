---
title: Profiling Engine
slug: config_profiling_engine
routes:
    default: /documentation/configbeez/config_profiling_engine
        
published: true
template: docs
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
    code: 'pro'
    category: [pro]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]   
    pro: 'pro'

# added collection selector

author:
    name: admin
metadata:
    author: admin

---

Under development - The MailBeez profiling engine allows you to add rule-based tags to customer profiles and orders. 

These tags can be utilized by other control-modules to control the behaviour and content of email modules, creating rich relationships between content and customer segments. This allows for even more effective targeting of your email campaigns.


Examples

- Tag all customers, who've never purchased product B, with tag "upsell-B"
- Tag all customers, who've only purchased from category X, with tag "only-cat-X"
- Tag all orders containing product H with tag "product-H"



Modules utilizing tags are:

- [Profile Filter](/documentation/filterbeez/filter_check_profile)  
 Examples
      - only send Birthday coupons to customers tagged with "upsell-B"
      - never send a product review reminder to customer orders containing "product H"
    

- [Profile Content](/documentation/filterbeez/filter_add_profiling_content)  
 Examples
      - insert upsell content promoting product B in all emails for customers tagged with "upsell-B"



- [Profile Information](/documentation/filterbeez/filter_add_profiling)  
 Examples
      - build custom logic code using order characteristics and/or parameters found in the customer profile.


