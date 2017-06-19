---
title: 'Trustedshops Integration Suite'
slug: config_trustedshops_rss_importer
routes:
    default: /documentation/configbeez/config_trustedshops_rss_importer
date: 26-10-2011
published: true
publish_date: 26-10-2011
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
    code: config_trustedshops_rss_importer
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
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2011/10/icon_328.png'
    pro: pro
    cert: 'true'
    price: '159 EUR'
    title_en: 'Trustedshops Integration Suite'
    teaser_en: 'Integrate your valuable Trustpilot Ratings in MailBeez Campaigs and your Storefront (SEO)'
    title_de: 'Trustedshops Integration Suite'
    teaser_de: 'Integrieren Sie Ihre wertvollen Bewertungen in MailBeez Kampagnen und den Shop (SEO)'
    author: MailBeez.com
author:
    name: admin
metadata:
    author: admin
---

**For retailers with a paid Trustedshops.com, Trustedshops.co.uk or any other Trustedshops account, this Mailbeez module allows you to easily embed Trustedshops reviews on your website, and as embedded content within Mailbeez emails; greatly extending the reach of your Trustedshops investment.**

Like many enterprising retailers, if you have made the investment and signed up for a Trustedshops account for your store, you are probably already looking for extra ways to leverage your subscription in order to maximize the exposure of good reviews to help sales; and this is where this module excels.

The Mailbeez Trustedshops Integration Suite effectively gives you the tools to publish your Trustedshops reviews on your website, and within any Mailbeez email via the introduction of a simple tag; greatly increasing review exposure.

**Trust at checkout**

In addition to the core functionality of the module, creative retailers could also create a secondary template to pull in only a handful of reviews at a time, and display them as snippets on the shopping cart or checkout page. As one of the main areas where a sale is decided upon, and where consequently trust is vitally important, this would be a highly effective, yet simple step to alert your customers to the store’s trustworthiness.

**Top features of the Integration Suite**

- Caching of the Trustedshops Rating Feed for fast page loads
- Template based formatting of the output
- Unlimited number of different templates for page integration, one template for email integration
- Selection of ratings to display e.g. “at least 4 star ratings”
- Random ratings or chronological list of ratings
- Easy drop-in installation into MailBeez
- Easy function call for output in the storefront
- Intelligent handling of  extra fields from the Trustedshops Rating Feed to utilize all information given in the Trustedshops Rating Feed

### Getting started

Install and activate the module – configure your RSS feed as described in the Module’s admin interface. You can use the integrated Test-Button to test your settings and check if the RSS feed is correctly imported.

**Integrate Ratings into the storefront:**

Let’s say you wanted to add the Trustedshops reviews to your ‘Contact Us’ page. In order to do this, you would simply use the following PHP code and place it into the Contact us’ page.

```
//include class
require_once(DIR_FS_CATALOG . 'mailhive/configbeez/config_trustedshops_rss_importer/classes/trustedshops_import_rss.php');
// create new instance
$rss = new trustedshops_import_rss();
// generate output (template, number of ratings, min stars, shuffle)
echo $rss->output_rss('rss_reviewpage.tpl', 7, 4, 'True');
```

The included DIV/CSS based template “rss\_reviewpage.tpl” generates a default output, which can be customized to match your store’s theme with only a little extra work.

**Integrate Ratings into MailBeez campaigns:**

By adding a simple tag into your MailBeez template you can also show your ratings in all or selected MailBeez generated emails.

![](Screen_trustedshops_rss_email.png "trustedshops_rss_email")