---
title: 'Advanced Configuration'
slug: advanced-configuration
routes:
    aliases:
        - /documentation/installation/config_queen/advanced-configuration
date: 11-08-2011
published: true
publish_date: 11-08-2011
template: docs
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration_status: review
    category:
        - docs
    tag: {  }
author:
    name: admin
metadata:
    author: admin
---

This page is for people having technical issues with MailBeez or want to set up a Cronjob.

When setting up a cronjob, depending on your server configuration, you may need to call the URL exactly like the domain you entered in the order process. Navigate to your MailBeez interface >About tab and look for a box outlined in red. It will contain the correct URL.

If you make changes to a configured cron-job, you will need to clear the template cache to avoid seeing old email templates. Navigate to mailbeez > configuration > template engine and click the “Delete” button.

# Run MailBeez automatically

## the easy way

Purchase (or call it “donation”) and Install the Module “[Run MailBeez automatically](/documentation/configbeez/config_cron_simple/ "Run MailBeez Automatically")“.The Installation is hassle free and the setup very easy.

This module will then process all MailBeez Modules as often as you have configured. Takes only a couple of minutes and works perfectly – if not let me [know](http://www.mailbeez.com/about/contact/ "Contact").

## the crontab way

**Be aware of some merchants have been reporting about issues (have not been able to reproduce these…) running MailBeez with a file-path call!**

The more advanced way is to set up a Cronjob to call the Secure Cronjob-URL. Some Merchants spent a couple of hours to make this work, since you need to learn a couple of things.

You find the Secure Cronjob-URL below the list of installed Modules when the first Module “MailHive – Basic Configuration” is selected.

The Secure Cronjob-URL looks like this:

> http://your-server.com/mailhive.php?57baa03dfcb9b8e33c2a6eb51c9a5147=run

You can execute single MailBeez-Modules by adding

> &module=MODULE

to the Secure Cronjob-URL. However there is no reason for doing so, unless you know what you are doing. You can activate each module in the MailBeez admin, only active modules are processed.

MODULE is the unique name of the MailBeez Module you would like to run e.g. “birthday” or “trustpilot” – you will find it in the URL when selecting the MailBeez Module.

### using crontab

UNIX/BSD/Linux systems have a crontab service. Crontabs are edited using command crontab -e. This will open an editor.

The syntax for crontab file is:

[text]  
 #  
 # declare running tasks in the following pattern:  
 # <minute> <hour> <day-of-month> <month> <day-of-week> <command>  
 # this example will run /home/user/script1.sh every minute:  
 # \* \* \* \* \* /home/user/script1.sh  
 #  
 # this example will run /home/user/script2.sh  
 # every 15 minutes for 3 hours after midnight on weekdays during summer months:  
 # \*/15 0-2 \* 6-8 1-5 /home/user/script2.sh  
 #  
 [/text]

**It is “safe” to run MailBeez a couple of times – since sendings are tracked it will start where the former processing stopped due to e.g. process timeout**

following entry will process all MailBeez Modules starting every day at 17:00:

there are different approaches to call URLs with a cron job, find following a list – what works is highly depending on your server environment.

using wget (recommended)  
 [text]  
 # run MailBeez  
 0 17 \* \* \* wget http://your-server.com/mailhive.php?57baa03dfcb9b8e33c2a6eb51c9a5147=run > /dev/null  
 #  
 [/text]

using lynx (recommended)  
 [text]  
 # run MailBeez  
 0 17 \* \* \* lynx -dump http://your-server.com/mailhive.php?57baa03dfcb9b8e33c2a6eb51c9a5147=run  
 #  
 [/text]

to add “&module” in the cronjob you need to escape the ampersand in the cron-url, e.g. like

http://your-server.com/mailhive.php?57baa03dfcb9b8e33c2a6eb51c9a5147=run\\&module=birthday

**Godaddy Server**

Thanks to [sakwoya](http://forums.oscommerce.com/user/28609-sakwoya/) for the following finding:  
 Godaddy CRON you have to go to their control panel and input the job using their own ‘click to select’ menu – this will give you something like:

(not recommended way of calling the cron url)  
 [text]  
 /web/cgi-bin/php5 “$HOME/html/mailhive.php?[yourid]=run”  
 [/text]

You have to change it to

(not recommended way of calling the cron url)  
 [text]  
 /web/cgi-bin/php5  $HOME/html/mailhive.php [yourid]=run  
 [/text]  
 i.e. remove the quotes and replace ? with [blank].

Thanks to [labrat](http://www.zen-cart.com/forum/member.php?u=2549), on his server the call looks like this:

(not recommended way of calling the cron url)  
 [text]  
 /usr/bin/php -q /home/MYUSERNAME/PATH/mailhive.php [yourid]=run  
 [/text]

## the alternative way

Choose one of the free web-based Cron-Services, e.g.

> <https://www.easycron.com> 
> <http://onlinecronservices.com>  
> <http://cronless.com>  
> <http://www.onlinecronjobs.com>

and configure the automatic call of your Secure Cronjob-URL.

 

# Testing

1. Set everything up, put MailBeez into Simulate Mode, send a copy to yourself
2. open your Secure Cronjob-URL in your browser -> watch how the MailBeez are processed
3. Set MailBeez in Production-Mode and let the Cronjob do the work

## Trouble-Shooting

Official Support Forum:  
<http://forums.oscommerce.com/topic/359282-automatic-trigger-email-campaigns-with-mailbeez-modules/>

### Common Problems:

**Send Test Email works, but no Emails are sent**

Make sure you have a valid email address for “send copy to”

**Pop-Ups are blank – GZIP**

The Pop-Ups are based on CeeBox. CeeBox does show blank when the content is GZIP compressed (took me a couple hours to figure out…)  
 Check if your storefront where mailhive.php is located uses GZIP compression - I tried to override the GZIP compression setting in the code but you might have a different setting.

You can check if your server uses GZIP compression on [http://www.whatsmyip.org/http\_compression/](http://www.whatsmyip.org/http_compression/)

Solution:  
 Deactivated GZIP – is this works, try to figure out how to deactivate GZIP on page-level and apply it to mailhive.php. [Please tell me your solution.](http://localhost/wordpress_mailbeez_EOL/about/contact/)

**Pop-Ups are blank – Ceon URI SEO Zen-Cart**

Blank Page in Mailbeez with Ceon URI Mapping.

Go to Admin / modules / Ceon URI Mapping (SEO) Config  
 Add /shop/mailhive.php to the bottom box (Excluded Files) – Click save. (you may have to edit the path!)  
 Mailbeez popups should now work.

 

**Pop-Ups only of advanced multi-step modules are blank**

Do you have **FWR Security** installed?

Yes: Add “mailhive.php” to the list of excluded pages – this addon removes “/” from the URLs

No: you have some kind of URL rewrite / SEO installed which removes “/” from the URLs. Make sure that URLs containing mailhive.php are not rewritten!

 

**Pop-Ups show wired content**

all Pop-Up windows look like this:

 [![](http://www.mailbeez.com/wp-content/uploads/2010/05/issue_myPreview-300x267.png "issue_myPreview")](http://www.mailbeez.com/wp-content/uploads/2010/05/issue_myPreview.png) issue\_myPreview 

Solution:  
 The content of the pop-up windows is generated in “catalog/mailhive.php” in the storefront.  
 Your probably have installed a config-cache which is not updated – clear your config cache and please let me know which function-call to add in the admin-area to clear the cache when updating config-values

**Pop-Ups and /mailhive.php shows an error**  
 If you get an error like this

 
    Fatal error: require_once() [function.require]: Failed opening required 'DIR_FS_CATALOGmailhive/common/functions/email_engine.php'

please check if you have a SEO addon installed and add mailhive.php as an exception.

**Pop-Ups are not opening – fixed in 1.2**

No Pop-up windows at all when Admin is using HTTPS

Solution: update to MailBeez 1.2 – this fixes HTTP/HTTPS Urls

**more Traps are**

- **Page Caching: **make sure catalog/mailhive.php is not cached!  
 This file is executing MailBeez in the catalog context (which allows you to use everything you can use in your catalog pages)
- **PHP execution time out: **Your Server might stop the execution after reaching the time limit.  
 It is “safe” to run MailBeez a couple of times – since sendings are tracked it will start where the former processing stopped
- **Buggy MailBeez Modules**: Errors in MailBeez will stop the execution  
 Fix the errror!
- **Email Server: **your email server might stop sending after a number of Emails  
 “Email Throttling” is on the roadmap and will allow to control the throughput of sendings
