---
title: 'Shopauskunft Integration Suite'
slug: config_shopauskunft_integration
routes:
    default: /documentation/configbeez/config_shopauskunft_integration
date: 08-02-2012
published: true
publish_date: 08-02-2012
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
    code: config_shopauskunft_integration
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
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2012/02/icon_64.png'
    pro: pro
    cert: 'true'
    price: '159 EUR'
    title_en: 'Shopauskunft Integration Suite'
    teaser_en: 'Integrate your valuable Ratings in MailBeez Campaigs and your Storefront (SEO)'
    title_de: 'Shopauskunft Integration Suite'
    teaser_de: 'Integrieren Sie Ihre wertvollen Bewertungen in MailBeez Kampagnen und den Shop (SEO)'
    author: MailBeez.com
author:
    name: admin
metadata:
    author: admin
---
<div style="float:right" markdown="1">[![](sa_siegel.jpg)](http://www.shopauskunft.de/retailer_process.html)</div>


**For retailers with a paid Shopauskunft.de Enterprise account, this Mailbeez module allows you to easily embed Shopauskunft reviews on your website, and as embedded content within Mailbeez emails; greatly extending the reach of your Shopauskunft investment.**

Like many enterprising retailers, if you have made the investment and signed up for a Shopauskunft Enterprise account for your store, you are probably already looking for extra ways to leverage your subscription in order to maximize the exposure of good reviews to help sales; and this is where this module excels.

The Mailbeez Shopauskunft Integration Suite effectively gives you the tools to publish your Shopauskunft reviews on your website, and within any Mailbeez email via the introduction of a simple tag; greatly increasing review exposure.

**Trust at checkout**

In addition to the core functionality of the module, creative retailers could also create a secondary template to pull in only a handful of reviews at a time, and display them as snippets on the shopping cart or checkout page. As one of the main areas where a sale is decided upon, and where consequently trust is vitally important, this would be a highly effective, yet simple step to alert your customers to the store’s trustworthiness.

**Top features of the Integration Suite**

- Caching of the Shopauskunft Rating Feed for fast page loads
- Template based formatting of the output
- Unlimited number of different templates for page integration, one template for email integration
- Selection of ratings to display e.g. “at least 4 star ratings”
- Random ratings or chronological list of ratings
- Easy drop-in installation into MailBeez
- Easy function call for output in the storefront

### Getting started

Install and activate the module – configure your API feed as described in the Module’s admin interface. You can use the integrated Test-Button to test your settings and check if the API feed is correctly imported.

**Integrate Ratings into the storefront:**

Let’s say you wanted to add the Shopauskunft reviews to your ‘Contact Us’ page. In order to do this, you would simply use the following PHP code and place it into the Contact us’ page.

```php
//include class
require_once(DIR_FS_CATALOG . 'mailhive/configbeez/config_shopauskunft_integration/classes/shopauskunft_integration.php');
// create new instance
$feed = new shopauskunft_integration();
// generate output (template, number of ratings, min stars, shuffle)
echo $feed->output_feed('feed_reviewpage.tpl', 7, 4, 'True');
```

The included DIV/CSS based template “feed\_reviewpage.tpl” generates a default output, which can be customized to match your store’s theme with only a little extra work.

**Integrate Ratings into MailBeez campaigns:**

By adding a simple tag into your MailBeez template you can also show your ratings in all or selected MailBeez generated emails, read more on [integrate Shopauskunft ratings into MailBeez Emails](/documentation/filterbeez/filter_add_shopauskunft_feed)
