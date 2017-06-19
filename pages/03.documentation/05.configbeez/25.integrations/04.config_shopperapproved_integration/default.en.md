---
title: 'ShopperApproved Integration Suite'
slug: config_shopperapproved_integration
routes:
    default: /documentation/configbeez/config_shopperapproved_integration
date: 03-05-2011
published: true
publish_date: 03-05-2011
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
    tag: pro
module:
    code: config_shopperapproved_integration
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
    pro: pro
    cert: 'true'
    price: '159 EUR'
    title_en: 'ShopperApproved Integration Suite'
    teaser_en: 'Integrate your valuable ShopperApproved Ratings in MailBeez Campaigs and your Storefront (SEO)'
    title_de: 'ShopperApproved Integration Suite'
    teaser_de: 'Integrieren Sie Ihre wertvollen Bewertungen in MailBeez Kampagnen und den Shop (SEO)'
    author: MailBeez.com
author:
    name: admin
metadata:
    author: admin
---

**For retailers with a paid ShopperApproved.com account, this Mailbeez module allows you to easily embed ShopperApproved reviews - both shop- and product-reviews - on your website, and as embedded content within Mailbeez emails; greatly extending the reach of your ShopperApproved investment.**

Like many enterprising retailers, if you have made the investment and signed up for a ShopperApproved account for your store, you are probably already looking for extra ways to leverage your subscription in order to maximize the exposure of good reviews to help sales; and this is where this module excels.

The Mailbeez ShopperApproved Integration Suite effectively gives you the tools to publish your ShopperApproved reviews on your website, and within any Mailbeez email via the introduction of a simple tag; greatly increasing review exposure.

**Trust at checkout**

In addition to the core functionality of the module, creative retailers could also create a secondary template to pull in only a handful of reviews at a time, and display them as snippets on the shopping cart or checkout page. As one of the main areas where a sale is decided upon, and where consequently trust is vitally important, this would be a highly effective, yet simple step to alert your customers to the store’s trustworthiness.

**Top features of the Integration Suite**

- Caching of the ShopperApproved Rating Feed for fast page loads
- Template based formatting of the output
- Unlimited number of different templates for page integration, one template for email integration
- Selection of ratings to display e.g. “at least 4 star ratings”
- Random ratings or chronological list of ratings
- Easy function call for output in the storefront
- Intelligent handling of incompatibilities and extra fields from the ShopperApproved Rating Feed to utilize all information given in the ShopperApproved Rating Feed

### Getting started

Install and activate the module – configure as described in the Module’s admin interface. 


**Integrate Ratings into the storefront**

You can copy the included default templates located in
`/mailhive/configbeez/config_shopperapproved_integration/templates/`
and rename them into custom templates.



Let’s say you wanted to add the ShopperApproved reviews to your ’Contact Us’ page. In order to do this, you would simply use the following PHP code and place it into the ’Contact us’ page.

```
//include class
require_once(DIR_FS_CATALOG . 'mailhive/configbeez/config_shopperapproved_integration/classes/mh_shopperapproved_integration.php');
$widget = new mh_shopperapproved_integration();

// generate output ($template, $items_limit, $min_stars, $random, $min_chars_comment)
echo $widget->output('default_storefront.html.tpl', 20, 4, true, 10);

```

The included DIV/CSS based template `default_storefront.html.tpl` can be copied to e.g.  `my_shoppingcart.html.tpl`, which can be customized to match your store’s theme with only a little extra work.

**Integrate Ratings into MailBeez campaigns**

By adding a simple tag into your MailBeez template you can also show your ratings in all or selected MailBeez generated emails. Please read more about this on the Filterbeez module page [Add ShopperApproved Rating](/documentation/filterbeez/filter_add_shopperapproved/ "Add ShopperApproved Ratings").

 

Via the introduction of a simple tag within the email body, Always Riding has spiced up the “Nopurchase – Contact customers w/o orders” Mailbeez module with some nice customer quotes, fed directly from the ShopperApproved Integration module.

Of course you can also add this tag into other MailBeez modules and use it in any MailBeez campaign you like.
