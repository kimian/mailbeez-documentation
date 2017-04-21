---
# http://learn.getgrav.org/content/headers
title: Automating MailBeez
slug: automating-mailbeez
# menu: Automating MailBeez
date: 28-04-2016
published: false
template: tutorial
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration_status: review
    category: [docs]
    tag: []
# added collection selector

author:
    name: Stanley
metadata:
    author: Stanley

---

[TOC]

**The magic of Mailbeez is that it does alot of the heavy lifting behind the scenes while you focus on your business. When installed, MailBeez can be run daily by processing each MailBeez module manually -- which might become quite time consuming. To run Mailbeez modules automatically and on set schedules, you need to set up automation.**

This guide will cover several ways to set-up the automation function for MailBeez using add-on functionality and with **Cronjobs**. This will allow you to set your email sends to begin automatically at set intervals and within certain time-frames, giving you full control over your email send loads!

There are three ways to setup MailBeez to run automatically:

* Use the MailBeez Auto-run plug-in
* Use the MailBeez Auto-run Advanced plug-in
* Set up a Cronjob

We'll cover each of these methods in the following sections.

## MailBeez Auto-run

With this simple Mailbeez plug-in, you can do away with the need to configure a cronjob to intiate email sends for your installed Mailbeez modules. 

### How it works
The plugin cleverly utilizes your store’s traffic to trigger Mailbeez to begin sending emails as often as you have configured it run. 

### Who should use it?
For store owners looking to get up and running quickly, or who do not wish to enter the backend server environment to setup a Cronjob, this is a very handy feature.

>>>>> A "real" Cronjob is the most reliable way to automize MailBeez. This module is a simple alternative solution.


### How to set it up

To get started, first download the module, then follow the easy installation instructions for your system.

[How to Install MailBeez Auto-run](/documentation/configbeez/config_cron_simple)

Set “time between running MailBeez (hours)” to “12″. Now your MailBeez modules will be processed twice a day, managing the optimum amount of customers for each active module!

 


## MailBeez Auto-run Advanced
As with the basic MailBeez Auto-run plug-in, this advanced plug-in allows you do away with the need to configure a cronjob to run MailBeez modules automatically. This plug-in adds powerful timing control that allows you to define run timing for each module individually. 

### How it works
As with "MailBeez Auto-run", this module utilises the traffic on your website to trigger the sending process. This happens asynchronous, which means the visitor will not experience any delay in page load times.

### Who should use it?
For store owners looking to get up and running quickly, or who do not wish to enter the backend server environment to setup a Cronjob. But also for those needing a more granular control over which emails go out when, and to reduce sending load.

>>>>> A "real" Cronjob is the most reliable and preferred way to automate MailBeez. This module is a simple alternative solution.

### How to set it up

To get started, first download the module, then follow the easy installation instructions for your system.

[How to Install MailBeez Auto-run](/documentation/configbeez/config_cron_simple)

Set “time between running MailBeez (hours)” to “12″. Now your MailBeez will be processed twice a day, managing the optimum amount of customers for each active module!




## Cronjob
It is much better to set up a traditional cronjob to run Mailbeez each day, allowing you to truly ‘set and forget’ Mailbeez once it is installed. 

### How it works
You can setup a Cronjob to make a request to the MailBeez Cronjob-URL, for example, every 5 minutes and then configure other timing parameters for each module.

### How to set it up

You need to use/have Cronjob scheduler software installed on your server.

In the scheduler software, enter the full Cronjob URL for your system, and set the timing parameters that you need.

You can find your Cronjob-URL at the bottom of your MailBeez Admin dashboard panel.

Secure Cronjob-URL (will immediately execute all active modules - but respects Mode).

>>>>> TIP: If you don’t want to spend hours learning how to set up a Cronjob, then the “MailBeez Auto-run” module is perhaps the ideal solution for most _smaller_ stores to automate MailBeez.


## Module timing and Cronjob 
After having set up the automatic sending process by either setting up a server Cronjob or by installing the MailBeez Auto-run plug-in frontend code, you can configure the behaviour for each module.

The Module timing and Cronjob configuration allows you to set the behavior mode for individual modules. There are three modes: 

#### Default 
The module will be executed every time the sending process runs. 

#### Direct 
The module will only be executed when the given Cronjob URL is called. So you need to set up a dedicated Cronjob for each module you have configured with "Direct". 

#### Timed 
The module will be executed on the configured weekdays within the configured timeframe. 

You need to make sure that the sending process is run within the configured timeframes. 

Also when you decide to run e.g. the module to ask customers to give a review only once a week, you need to make sure the timeframe within the module is configured correctly, so at least covering 1 week: "Find all orders between 5 and 5+7 days old". 
