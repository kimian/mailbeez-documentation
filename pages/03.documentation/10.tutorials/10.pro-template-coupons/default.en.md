---
# http://learn.getgrav.org/content/headers
title: Creating template coupons
slug: creating-template-coupons
published: true
template: tutorial

visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration_status: done
    category: [docs]
    tag: [pro]
---

[TOC]

>>>>>> use the tour within MailBeez to see how it works in your Store

In this tutorial you will learn how to create template coupons and configure the appropriate modules.


## Personalized Coupons

The MailBeez [Coupon Engine](/documentation/configbeez/config_coupon_engine) is a sub-module of all MailBeez coupon modules. It allows you to generate and send personalized coupons.

We'll use the module [Birthday Greetings Coupon](/documentation/mailbeez/coupon_birthday) as an example, to show the configuration steps for setting up coupons. This procedure can be applied to all other MailBeez modules with a couponing function.

## How it works

The MailBeez Coupon Engine generates new coupons based on a configured template. The generated coupon is a copy of this template coupon, but the **expiration date** and **coupon code** are generated individually. This ensures that every customer receives a unique coupon code that is only valid as long as has been configured in the respective module (for example, "Birthday Greetings Coupon"). 

## Creating a template coupon

>>>>> Please ensure that the coupon system is activated (osCommerce: a [compatible coupon addon](/documentation/configbeez/config_coupon_engine) must be installed)

From your shopping-cart's admin panel, navigate to the main configuration settings for "coupons" or "vouchers".

Then click on "New coupon".

Find input field **Coupon Code** (not name), then enter the following: `template_birthday`.

It is important that the **coupon code** starts with `template_` , as this identifies template couponsrs. Otherwise, the template's coupon will not be allocated in the following section.

Configure the template coupon according to your wishes by adding discount amount etc.. All info, except the expiration date, will be transferred to the coupon that's generated.

Now, save the coupon promo. (Important: after one click, a page to verify the information is shown, then click again to confirm.)

## Assigning the template coupon

Make sure that the newly created template coupons can be seen in the coupon system of your shopping-cart.

Navigate to `MailBeez > MailBeez Modules > Birthday Greetings Coupon` and click the **Edit** button at the top right side of the screen to open the Configuration view for this module. Further down the right side you will find a **Coupon Template** selection list, from which you can select the coupon template you just created.

Now, save the configuration for this module.

In the view of the right you see at the bottom that the template coupon has been activated.

## Find out more

### Testing coupon generation

You can test the generation of coupons using the "Simulation" mode. Ensure that MailBeez is in simulation mode by clicking the button in the upper right corner of the window. Now run the module "Birthday Greetings Coupon". There are "real" emails generated, but they are all configured and sent to the simulation e-mail address and marked with **[SIM]** in the subject.

In the coupon system you will find for each email a generated coupon. The simulation coupons are marked with **[SIM]** in the coupon code. These coupons are fully functional, and you can now make test orders.

### Deleting Simulation coupons

In simulation mode, coupons can be deleted in their respective modules with the structure appearing button. Alternatively, you can use the delete function in `MailBeez > Configuration > Certificate` .

### Deleting old coupons

Over time, thousands of coupons will be generated. Under `MailBeez > Configuration > Coupon Engine` contains a handy "cleanup" function to delete expired coupons.

### Find coupons

On the MailBeez Dashboard you can find a search function (eventually you'll need to install on `MailBeez > Configuration > Dashboard Configuration` ) that lets you quickly find templates or coupons and then to open it for editing.

>>>>>> Search for **template_** to find all template coupons and open directly to the editor
