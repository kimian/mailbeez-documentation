---
# http://learn.getgrav.org/content/headers
title: Setting up the module templates
slug: setting-up-module-templates
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

## Template Structure

MailBeez generates all Emails based on a common main template and a module body template. In this tutorial you can learn, how to edit the templates of the installed modules.

<div style="padding: 30px; border: 1px solid #c0c0c0; background-color: #FFFFFF; width: 100%; max-width: 600px; margin:auto" markdown="1">
[Common Main-Template](/documentation/tutorials/setting-up-main-template)

<div style="padding: 30px; border: 1px solid #c0c0c0; background-color: #E7F2FA;" markdown="1">Module specific template
<br>
Placeholder `{$body}`
<div style="padding: 30px; border: 1px solid #c0c0c0;" markdown="1">productlist template<br>
Placeholder e.g. `{$list_engine.productlist}`
</div>
</div>
</div>


## Open the template for editing

The visual editor comes with any Pro subscription and allows you to edit the module-specific body template in a compfortable and visual way.

You can edit the module template from within each modules, e.g. for module  "[Coupon: Birthday](/documentation/mailbeez/coupon_birthday)" go to  

`MailBeez > MailBeez Modules > Coupon: Birthday > Template Manager Button "edit"` 

for editing in the visual editor


## Import a template

On the right hand site you find the button `select Layout-Template` to import a template. Please select the matching "**responsive**" module to import the latest version of the mobile-friendly module template.

## Editing the content

Each module template is composed from a number of blocks, which you can edit, move or delete. As soon as you move your mouse pointer towards one of these blocks you will see its reaction.

### Edit text

You see a pencil symbol on the left? Just click and the editor view for the current block will open


### Move element

In the context menue on the right you will see two arrow buttons - just click an the current element will move up or down

### Delete element

The trashcan button in the context menue does what it says - it deletes the current element

### Insert element

A click on the + symbol in the context menue opens a dialog to select an element to insert. Just click on the element and it will be inserted after the current one.

## Test your template

In the top area of the editor you find Buttons like "320px", "480px" - they allow you to test how the emails will reformat on e.g. mobile devices. If you find issues with the email to adopt to the width very likely there is an element (e.g. an images) with a fixed width-setting. In this case use "100%" as width. Also long links can cause issues - try to shorten the linked text.

As soon as you are happy with the changes, try the "mobil" preview - in the upper right area you find a Button "mobil" which allows you to select a module template (e.g. birthday greetings) for the devices preview.

Thanks to the "send test-email" feature you can easily send an email with some test-content for a quick layout check to any email address.
 

## Text-Version

To reduce the risk of spam ratings and to support older email clients you can configure a text version. With click on button "**TXTMODE**" an editor for the text-version opens and allows you to automatically generate a text version you afterwards can tweak.

## Saving a template

You are happy with your work? Then it is a good idea to save your work as a template. On the right hand site you find a button `save as Layout Template`. Just click on this button, enter a name for the template and save it. At any time you can restore this version by `select Layout-Template > User`.

 
## Heads-up: Nerd-Mode

The "**Nerd-Mode**" allows you to edit the code of the module template. You have full access to the code and experts can perform complex customizations - but handle with care: you easliy can tweak your template in a way, which causes unwanted results in the different email clients (e.g. Outlook is quite picky).
