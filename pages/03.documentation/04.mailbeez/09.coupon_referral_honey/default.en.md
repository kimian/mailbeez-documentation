---
title: 'Coupon Referral Honey'
slug: coupon_referral_honey
date: 10-01-2012
published: true
publish_date: 10-01-2012
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
    tag:
        - pro
        - coupon
module:
    mc_ready: true
    code: coupon_referral_honey
    category:
        - mailbeez
    compatiblity:
        - comp_cre
        - comp_zencart
        - comp_xtc
        - comp_xtcm2        
        - comp_gambio
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2012/01/icon_32.png'
    pro: pro
    cert: 'true'
    price: '299 EUR'
    title_en: 'MailBeez ReferralHoney'
    teaser_en: 'make every customer a markeeter'
    title_de: 'Neu-Kundenspiel "ReferralHoney"'
    teaser_de: 'Viraler Effekt durch Social Sharing bringt Neu-Kunden'
    author: MailBeez.com
author:
    name: admin
metadata:
    author: admin
---

<!--
[Visit the MailBeez ReferralHoney Microsite for more information and screenshots](/download/mailbeez-referral-honey/ "The MailBeez ReferralHoney")
-->

**ReferralHoney is a fully automated customer referral system for the Mailbeez framework. Customers refer friends or family to your store, and get rewarded when one of their referral group makes a purchase, a cycle which truly makes every customer a potential marketeer.**

Take a look at the following flow to see how the ReferralHoney cycle works:

![](referralflow.en.png "referralhoney_flow_de")

ReferralHoney emails a personalized coupon code link to each customer after they have placed an order in your store, which they can then share with friends, family or co-workers, in the knowledge that if one of their contacts places an order with the code, they will automatically receive a store reward. Within the initial referral email, your customers will also find a link that will take them to their own coupon code page hosted at your store’s website, a page that they can share with their contacts on Facebook, Twitter, their blog or personal website.

**Automated and personalized**

A true fit and forget, fully automated and intelligent system, at its heart, ReferralHoney uses your store’s inbuilt coupon system alongside the MailBeez framework to create the basis on which codes are created, tracked, rewarded and ultimately emailed to the participants. Relying on this coupon functionality means that there is nothing to install apart from the module itself, and absolutely no tracking code to add to the front end of your site.

As you may already be aware, a Mailbeez module installation is very easy, and simply requires you to drop the new files into your store’s FTP area. Most importantly, no existing store files need be altered. However for best results we recommend to utilize the MailBeez Service for custimization, configuration and going live.



### General Module Options:

**Order-Status of Customer order to start**  
 Choose the order status on which ReferralHoney will begin the referral cycle – we would recommend ‘despatched’, or your store equivalent.

**Set Order Status for friends order to recognize**  
 Choose the order status on which ReferralHoney will recognize an order from a referrer’s friend – we would recommend ‘despatched’, or your store equivalent.

**Delay after order**  
 The number of days after your customer’s last order before it qualifies for a ReferralHoney invitation.

**Set number of days to skip processing**  
 The number of days after processing is skipped (depending how often you run MailBeez). This number must be bigger then “Delay after order”

**Delay since last invite**  
 Delay since a customer was invited to join the referral scheme – set this to over 7 days if you have customers that order very regularly to ensure that multiple invitations are not sent out.

**Share-Coupon: Expires after days**  
 The number of days after which the initial share coupon expires – calculated from the sending point in time.

**Reward-Coupon: Expires after days**  
 The number of days after which the reward coupon expires – calculated from the sending point of time.

**Length of Coupon Code**  
 Sets the length of the automatically generated coupon code

**Sender email****, Sender name**  
 Sets the from email address and name in each ReferralHoney email. Typically you would want to use your store’s most used email address and name to ensure high delivery rates.

 

### Options for Invite

**Delay after order** (same as in General Options)  
 The number of days since last order

**Coupon Template – Friends Coupon for sharing**  
 Choose the coupon code template you have configured in the coupon system. This coupon will be used as template to generate a personalized, unique coupon. The coupon code must start with ‘*template\_*‘ e.g. ‘*template\_game*‘

>>>>> When setting up the ReferralHoney refer a friend coupon template, please make sure to leave the usage field blank, or for example enter a number of at least 50. If we take this scenario as an example, the customer who receives the coupon to share with their friends is always marked as having used the coupon (so only their friends can use it), leaving 49 more uses available.<br>
 The number of usages per customer field should be set to 1 – the refer a friend coupon is automatically marked as used by the referring customer when it is sent, which makes sure the coupon is only used by newly referred customers and not the initial recipient.

**Share-Coupon: Expires after days** (same as in General Options)  
 The number of days after which the share coupon expires – calculated from the sending point of time.

 

### Options for Order Notification / Recognition

**Set Order Status for friends order to recognize**  
 Set the status of orders to recognize accepted friend orders

 

### Options for Reward

You can set up to 3 levels of rewards, which means that for each level you can define the reward Coupon you would like to give out.

**Delay after Coupon Expiry date**  
 The number of days after the expiry of the friend coupon before sending the reward coupon.

**Number of Orders for Level 1**  
 The number of recognized orders to get reward coupon level 1

**Reward: Choose Coupon as Template for Level 1**  
 Choose the relevant coupon code you have configured in the coupon system. This coupon will be used as template to generate a personalized, unique coupon. The coupon code must start with ‘*template\_*‘ e.g. ‘*template\_reward1*‘

**Number of Orders for Level 2**  
 The number of recognized orders to get reward coupon level 2

**Reward: Choose Coupon as Template for Level 2**  
 Choose the coupon code you have configured in the coupon system. This coupon will be used as template to generate a personalized, unique coupon. The coupon code must start with ‘*template\_*‘ e.g. ‘*template\_reward2*‘

**Number of Orders for Level 3**  
 The number of recognized orders to get reward coupon level 3

**Reward: Choose Coupon as Template for Level 3**  
 Choose the coupon code you have configured in the coupon system. This coupon will be used as template to generate a personalized, unique coupon. The coupon code must start with ‘*template\_*‘ e.g. ‘*template\_reward3*‘

**Reward-Coupon: Expires after days**  
 The number of days after which the coupon expires – calculated from the sending point of time.
 
 
### Customization of sharepage

the sharepage is fully customizable, the default templates (**will be overwritten with updates**) are located in

```

/mailhive/mailbeez/coupon_referral_honey/templates/

```

make a copy of these templates and remove the `default_` from the filenames. Then adopt the templates to your needs

The System will try to load the templates in following order:

```bash
sharepage_<language>.tpl.html
sharepage.tpl.html
default_sharepage_<language>.tpl.html
default_sharepage.tpl.html

```

so if a language specific template is not found the `sharepage.tpl.html` templates will be used.

 
