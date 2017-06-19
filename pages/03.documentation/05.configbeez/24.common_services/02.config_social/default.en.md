---
title: Social Sharing
slug: config_social
routes:
    default: /documentation/configbeez/config_social
    aliases:
        - /documentation/configbeez/social-sharing
date: 31-08-2011
published: true
publish_date: 31-08-2011
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

## Social Sharing Links in Email

As a common service the Social Sharing links give your customers the option to share your products on Facebook, Twitter, or Google+ with a single click, enabling you to leverage the power of social media within your eCommerce email marketing campaigns!

![](Screen_social_email.en.jpg?resize=582)


 

Fully configurable, *you* choose which social network links will display to your customers by turning them on and off, thereby controlling the networks they can share with.

>>>>>by default the social sharing link are not include in responsive email template to keep them as clean as possible


The following example shows how to integrate the social sharing - in this case the "tiny" template - elements into your product list template using `{$products[product].social_tiny}`: 

```text
{section name=product loop=$products max=$max_products}
(...)
   {$products[product].social_tiny}
(...)
{/section}
```

**Important**: the `{$products[product].social_tiny}` Tag only works within the `products` loop as product data is added to the share links.