---
title: Trustpilot
slug: trustpilot
routes:
    default: /documentation/mailbeez/trustpilot
date: 22-05-2010
published: true
publish_date: 22-05-2010
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
        - ce
module:
    code: trustpilot
    category:
        - mailbeez
    compatiblity:
        - comp_osc
        - comp_cre
        - comp_digi
        - comp_zencart
        - comp_xtc
        - comp_xtcm2        
        - comp_gambio
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2011/03/top_64.png'
    pro: ''
    cert: ''
    price: ''
    title_en: Trustpilot
    teaser_en: ''
    title_de: Trustpilot
    teaser_de: 'Trustpilot macht mehr Besucher zu Kunden. Bis zu 100x mehr Bewertungen auf Trustpilot - arbeitet mit dem Trustpilot Feedback service, welcher eine Email mit Autologin-Link an die Kunden verschickt.'
    author: MailBeez.com
author:
    name: admin
metadata:
    author: admin
---

This free module, when installed, automatically asks your customers to rate your store on Trustpilot. For professional application, we recommend the [Trustpilot Advanced](/documentation/mailbeez/trustpilot_advanced) module which comes with any Pro Plan!


**Proactively and intelligently request store reviews from your customers, and significantly increase your Trustpilot ratings over the same time frame compared to the standard Trustpilot review email with the Mailbeez Trustpilot module.**

Developed in close cooperation with Trustpilot, and officially sanctioned as their recommended partner solution, the Mailbeez Trustpilot module intelligently enhances the default Trustpilot review collection email. Utilizing customer specific order data to dynamically pre-fill the Trustpilot review email link, this module enables your customers to write their review in a “one-click” Trustpilot review environment, which, with its incredibly easy review process, can help to harvest up to 10 times more customer reviews for your store.

**Here’s how the whole system works:**

- Trustpilot provides you with a unique Automatic Feedback Service email address, which they host for you on a secure, neutral server.
- When a customer makes a purchase from your website, the MailBeez Trustpilot Module will send an email to your unique Trustpilot email address after a given time frame, while respecting the configured order status (e.g. “delivered”)
- When the Trustpilot system receives this email, it automatically extracts the key information (customer email,order ID, name) and creates a review invitation email.
- The system sends this email to the customer from your store’s order e-mail address, so it appears that you have sent the email.
- The customer receives the email and clicks on the unique link which takes them directly to the** ‘one-click’** review page.
- The provided link identifies the customer to Trustpilot so they do not need to enter personal information or confirm their email address. As soon as they press ‘Submit’, the review goes live.
- The feedback system has multi-language recognition, so a French order confirmation triggers a French template and a French version of Trustpilot etc. You can decide if you select the language manually or let the Trustpilot Service choose automatically.
 

If you are using customer-based languages, you need to modify your trustpilot-mailbeez. Find the assignment:

```
‘language’ => MAILBEEZ_TRUSTPILOT_LANGUAGE
```


and assign the language based on how it is done in your system.

