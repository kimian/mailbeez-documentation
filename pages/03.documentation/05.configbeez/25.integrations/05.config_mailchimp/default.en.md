---
# http://learn.getgrav.org/content/headers
title: MailChimp Integration
slug: config_mailchimp
routes:
    default: /documentation/configbeez/config_mailchimp
    aliases:
        - /download/the-mailchimp-connector
        - /download/the-mailchimp-connector/oscommerce
        - /download/the-mailchimp-connector/zencart
S# menu: MailChimp Integration
date: 02-03-2012
published: true
publish_date: 02-03-2012
# unpublish_date: 02-03-2012
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
    code: 'config_mailchimp'
    category: [configbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2012/11/icon_64.png'
    pro: 'pro'
    cert: 'true'
    price: '300 EUR'
    title_en: 'MailChimp Integration'
    teaser_en: 'MailBeez unlocks, MailChimp delivers'
    title_de: 'MailChimp Integration'
    teaser_de: 'MailBeez verfasst, MailChimp liefert'
    author: 'MailBeez.com'
author:
    name: admin
metadata:
    author: admin
---

##The MailBeez for MailChimp Connector
<div style="float:right;margin-top: -48px !important" markdown="1">
![](mc_connector_badge.png?resize=380,328)
</div>

Run MailBeez in your MailBeez compatible eCommerce store, but want to deliver its intelligent, personalized content through your MailChimp account?
With our official MailChimp Connector you can do just that.
(The connector was developed in close cooperation with MailChimp)

**What the hey is MailBeez?**

If you run an MailBeez compatible store but don't know MailBeez yet then here’s the skinny. MailBeez is a store admin controlled email eco-system that you can add to over time. From **automating product review requests**, right down to the creation and delivery of **personalized offer coupons**, Mailbeez gets things done, **driving increased revenue** from your existing customer base, and mining the lifecycle of your customer to its fullest potential.

**Hmm, sounds good, and MailChimp?**

For anyone out there who has been hiding under a rock, MailChimp is an awesome email newsletter system that makes it a cinch to design and send stylish, inbox friendly (that’s important) emails.
For these simple reasons, thousands of companies and brands around the world now rely on MailChimp for their email newsletter needs.


**now put the two together.**

You love the way MailBeez automates your eCommerce email marketing, but you also like to use MailChimp for occasional newsletters, and dig the way it makes designing emails so simple, **removes any potential for email blacklisting**, and importantly makes sure each email presents itself perfectly in your customer’s inbox. Combine these two things and you have our new MailChimp Connector – MailBeez intelligence, MailChimp design and sending security.


>>>>>MailChimp is great, but the system comes with a number of headaches like limited number of personalization content fields.  
 Unless you really like to use MailChimp **we recommend** to [configure Newsletter2Go as your Email-Engine](/documentation/configbeez/config_email_engine). You will acchieve comparable delivery-rates but without any limitations.

##Advantages

**DELIVERY!** Improve your delivery-rate by using MailChimps Email System  
 **STAY IN SYNC!** on both sidestrue 2-way synchronisation keeps information up-to-date  
 **AUTOMATIC!** No extra efforts once set up and configured the integration will run on autopilot

Developed in close cooperation with MailChimp: reviewed and approved!  
 New: Works also with lists larger than 15.000 subscribers thanks to fast delta-sync  
 Easy installation: Wizard based, with simulation capabilities




##Mailchimp ready modules:
The MailChimp Integration works with all MailChimp-ready MailBeez Premium Modules:
<ul class="mc_read_list">
    {% for p in page.find('/documentation/mailbeez').children  if p.header.module.mc_ready %}
    <li>
    {# workaround #}
    {{ "[#{p.title}](#{p.url})"|markdown }}
    </li>
    {% endfor %}
</ul>
        
       