---
title: 'Coupon Engine'
slug: config_coupon_engine
routes:
    default: /documentation/configbeez/config_coupon_engine
    aliases:
        - /documentation/configbeez/coupon-engine
date: 10-04-2012
published: true
publish_date: 10-04-2012
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
    tag: [pro,coupon]
module:
    code: 'pro'
    category: [pro]
    compatiblity: [comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]   
    pro: 'pro'     
author:
    name: admin
metadata:
    author: admin
---

Find an overview of the store compatibility on: [MailBeez Compatibility](/documentation/compatibility/).

The MailBeez Coupon Engine is a sub-module which sends out personalized coupons, and can be utilized by any MailBeez module that allows generation of coupons. 

The Coupon Engine allows you to create persolized coupons that can be sent to specific customers or as part of any email campaign. Personalized coupons offer a number of advantages that result in better control over your coupon offers.

###Coupon basics

Generally, there are two types of coupon codes used within MailBeez - static and personalized. 

Static coupon codes are generic codes that can be redeemed multiple times by any number of customers.  Usually a static coupon uses a single coupon code with no or few restrictions. To redeem the coupon, all that is needed is the coupon code.  Once the code has been distributed e.g. via email, there is not much you can do to control the proliferation of the coupon (viral effect). The unintended consequences can be a coupon that is used many times by the same customer, or redeemed more times than you initialy intended.

These issues can be addressed, in part, with personalized, limited use coupon codes. Rather than releasing a single coupon code to everyone, you can create individual codes for each customer.

###Advantages of personalized coupons

In comparison to static coupon codes, there are a number of advantages to using personlized coupons:

- **No unwanted viral effect**: You can configure exactly how often a coupon can be applied
- **Sense of urgency due to expiry date**: Each generated coupon has an expiry date, e.g. 14 days starting with the day the coupons was sent. The expiry date creates a sense of urgency, leading to more orders. In addition, you can utilize the [Coupon Expiry Reminder](/documentation/mailbeez/coupon_expire) to send a reminder email a couple of days before the expiry date - great for conversion!
- **Traceability**: MailBeez can connect the coupon code to the receiving customer and the email it was sent with. This allows better insight into the effectiveness of your coupons and specific emails.



###Template Coupons

The coupon engine generates personalized coupons based on **template coupons** which are assigned to the respective email modules.
 
A **template coupon** is a "normal" coupon, but is distinguished by the coupon **CODE**, which **MUST** start with the pattern `template_`.

>>>>>>Make sure to view the helper section "How to set up a template coupon" in the Tour tab on your MailBeez admin panel.
 
**Creating a Template Coupon**

As an example, let's create a "[Birthday Coupon](/documentation/mailbeez/coupon_birthday)":

The first step will be to create a new coupon with 

CODE = `template_birthday`

and enter the values accordingly (e.g. 10% off) - the expiry date is not used.

In module [Birthday coupon](/documentation/mailbeez/coupon_birthday) you can now assign this template coupon (remember to save your settings).

During the generation process of birthday emails, a personalized coupon is generated for every recipient based on the settings of the template coupon. In addition, a random coupon code and a dynamic expiry date - e.g. 14 days after date of sending is also generated.

You can test the setup by running a simulation: In Simulation-Mode, execute the module. This will generate "real" emails with "real" coupons, which is sent to the configured email address you entered. This allows you to validate the coupon settings, and to even make a test-order.



###Maintainance features

In this module you'll find a range of features which will help you to maintain your coupons:
 

**Coupon Search**: Find a coupon and edit it, also available as [Dashboard-Widget](/documentation/dashboardbeez/dashboard_coupon_admin) zur Verfügung.

**Delete Simulation Coupons**: When running a simulation "real" coupons are generated. This button allows you to clean up the mess ;)

**Delete expired Coupons**: Clean up expired coupons

**Repair sync**: In case coupons are not assigned to message you can repair this assignment


>>>>>**Please note**: In each module you can configure the length of the coupon code. Long codes (e.g. 8 or 10 characters) can be generated very efficiently. With shorter code lengths (and many existing codes), code generation might take longer until a free code is found. This can cause issues like time-outs during the sending process.

## osCommerce Coupon System support

As the “mother of all eCommerce Systems", osCommerce is kept as a clean core without having addons like a coupon system.  
You probably have already added a coupon system to osCommerce, and MailBeez supports a number of different coupon systems as listed below. The table names listed might help you to identify, which coupon system you are using.

In case you have not yet installed a coupon engine, we recommend a CCGV based addon.

### CCGV based coupon systems

There are a number of coupon system addons based on the “CCGV” coupon system, e.g.:

- [http://addons.oscommerce.com/info/4135](http://addons.oscommerce.com/info/4135)  
- [http://addons.oscommerce.com/info/282](http://addons.oscommerce.com/info/282)  
- [http://addons.oscommerce.com/info/8002](http://addons.oscommerce.com/info/8002)  
- [http://addons.oscommerce.com/info/9020](http://addons.oscommerce.com/info/9020) (osc 2.3.3.4)

These addons utilize an almost identical database structure

**Tables**:

You should find following tables in your table definition in case you are using a CCGV based coupon engine

```bash
TABLE_COUPONS
TABLE_COUPONS_DESCRIPTION
TABLE_COUPON_EMAIL_TRACK
TABLE_COUPON_REDEEM_TRACK
TABLE_COUPON_RESTRICT
 
```

#### Discount Coupon Codes

[http://addons.oscommerce.com/info/4269](http://addons.oscommerce.com/info/4269)

**Tables**:

You should find following tables in your table definition in case you are using a DCC based coupon engine


```bash
TABLE_DISCOUNT_COUPONS
TABLE_DISCOUNT_COUPONS_TO_ORDERS
TABLE_DISCOUNT_COUPONS_TO_CATEGORIES
TABLE_DISCOUNT_COUPONS_TO_PRODUCTS
TABLE_DISCOUNT_COUPONS_TO_MANUFACTURERS
TABLE_DISCOUNT_COUPONS_TO_CUSTOMERS
TABLE_DISCOUNT_COUPONS_TO_ZONES
 
```

#### Discount Coupons by high-quality-php-coding.com

[http://high-quality-php-coding.com](http://high-quality-php-coding.com)



**Tables**:

If you use a DC-based voucher system, you should find the following tables in the table definition:



```bash
TABLE_DISCOUNT_CODES
TABLE_CUSTOMERS_TO_DISCOUNT_CODES

```

In case you are using the fork **Discount Codes BS** 
<http://addons.oscommerce.com/info/9460>:

This module is not using constants to define tables, so please add following definitions to your system by creating a new file

`/mailhive/common/local/dc.php` 

with the content

```php
<?php
define('TABLE_DISCOUNT_CODES', 'discount_codes');
define('TABLE_CUSTOMERS_TO_DISCOUNT_CODES', 'customers_to_discount_codes');
define('FILENAME_DISCOUNT_CODES', 'discount_codes.php');
```
This will define the missing constants.

