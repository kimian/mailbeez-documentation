---
title: How to Use Customer Segmentation
publish_date: '15-02-2017 00:00'
date: '15-02-2017 00:00'
slug: customer-segmentation
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
author: admin
  
---
In this tutorial you will learn how to segment a customer list and apply it to a Mailbeez Newsletter campaign.

### Customer Segmentation

With [MailBeez Newsletter Advanced](/documentation/mailbeez/newsletter), you have many options for customer segmentation. 

There are four main sections that allow you to create segmented lists:
1. Location 
1. Customer
1. Products 
1. Orders

### How it works
Within each of the sections, there are text input fields (find-as-you-type) for nested conditions which you use for more granular segmentation. But the real magic happens when you start combining these sections to create more complex segmentations. 

Here’s an example of the `Products` section and its related input fields.

![image](segmentation.1.png? "products") 

Over time, you’ll develop multiple lists and campaigns. So that it doesn’t get confusing, you have the option to name the list and give it a detailed description. This way you’ll always know what or which customer characteristics the list is targeting.

 In MailBeez, **segmentation parameters are set at the list level**. After you’ve created your list, you then set the segmentation parameters, develop your email messaging, and lastly send out your message to the appropriate list. 


### Creating a segmented list
Let’s walkthrough an example to better understand how we would accomplish a targeted product promotion by creating an email campaign and using the segmentation feature in [Newsletter Advanced](/documentation/mailbeez/newsletter).

##### Promotion A - Bicycle Tire Campaign

We want to send an awesome newsletter with a “sweet deal” for our awesome customers. Our Newsletter is gonna accomplish two things: We’ll be reminding customers who bought a men’s bicycle, that now might be a good time to replace the tires on it. At the same time, we’re gonna promote a sweet deal on a new set of bicycle tires for those customers who bought the bicycle within a a specific time frame. We’ll target customers in the U.S.A., in the southern region specifically, which we know uses their bicycles year around in their daily commute to and from work.  So their tires should be well worn by now. 

### Step 1 - Create a dynamic list of recipients
First, we need to create a list of customers. A list tells us which customers will receive this email. A List in Mailbeez is also the place where you’ll do your segmentation... in other words, which customer characteristics you'll target for this specific messaging.

First, navigate to MailBeez Newsletter Module: `MailBeez > MailBeez Modules > Newsletter Advanced`

On the right side panel, click the button <span style="color:#303030; font-family: 'courier';">Edit Lists</span>.

Then, click on button <span style="color:#303030; font-family: 'courier'; font-weight: bold;">New List</span> to create a new list.

If you already have a list created that you want to use, then all you need to do is click on the list you want to edit, then click the <span style="color:#303030; font-family: 'courier';">Edit List</span> button. 

Next, give the list a Name e.g. `Promotion A.`, and a good description so that you will know what this list is used for. 

![image](segmentation.3.png? "Configure the list")

Now, select the source for the list. On most occasions this will be `All Customers`, but other system generated source options like `Subscribed Customers` or `Prospects` are available. 

Don’t forget to click <span style="color:#303030; font-family: 'courier';">Submit</span> or <span style="color:#303030; font-family: 'courier';">Update</span> to save the list.

### Step 2 - Set segmentation parameters
Now, select the newly created list and click <span style="color:#303030; font-family: 'courier';">Edit Segmentation.</span>  

The list segmentation window will open. 

#####This is where the magic happens! 

Here, you will select the parameters and settings that tells your list which customer characteristics are relevant for including when sending emails for the campaign.

![image](segmentation.4.png? "Segmentation list")

Notice the title of the list you are segmenting is always visible at the top of the window. In this example we are working with `Segmentation for List: Promotion A.`

Using the info from our example campaign above, we will input our segmentation information as shown in the image above.

Scroll down, to configure section Orders.

![image](segmentation.5.png? "Segmentation list")


Click the Update button to save the segmentation.

Now, you’re back on the Edit List page. 

Click on <span style="color:#303030; font-family: 'courier';">Test Segmentation</span>. 

A new window opens listing the customers matching the segmentation criteria. Click on a customer for more details and the [Customer Insight](/documentation/configbeez/config_customer_insight) window opens.


##### What did we do? 

In the `Location` section, we targeted customers in <span style="color:#303030; font-family: 'courier';">United States</span> only. We further limited customers in the U.S. to the regions <span style="color:#303030; font-family: 'courier';">Alabama, Florida, Georgia,</span> and <span style="color:#303030; font-family: 'courier';">South Carolina</span>. 

Because we know that the product is a <span style="color:#303030; font-family: 'courier';">Men’s Touring Bicycle</span>, in the `Customer section`, we will only send to <span style="color:#303030; font-family: 'courier';">male</span> customers. Sure, we could also just send to all customers that has purchased the Men’s bicycle, but I want to show that you do have the option to segment based on `Gender` as well. 

In section `Products`, we decide which products are relevant for this customer group. Again, we want to target customers that purchased the <span style="color:#303030; font-family: 'courier';">Men’s Touring Bicycle</span>. However, we don’t want customers that have recently purchased <span style="color:#303030; font-family: 'courier';">27’ bicycle tires</span> because they may have purchased these to use as replacements already. Besides, this is the product we’ll offer with our “sweet deal”. So we excluded this product in `Products NOT purchased`.

Next, we want our “sweet deal” to go to past customers that have had enough time to use their bicycle and wear the tires a bit. As such, they’re more likely to be ready to replace the original tires. So in the `Orders` section we set the date in `Last Order between` field to <span style="color:#303030; font-family: 'courier';">01-01-2015</span>, to target customers that have purchased a bicycle on or after this date. We then limit it to bicycles purchased before <span style="color:#303030; font-family: 'courier';">01-01-2016</span> which we input into `...and this date` field.

### Step 3 - Create the Newsletter

Next, you’ll create your awesome newsletter and connect it to the list you created in **Step 1**.
1. Navigate to MailBeez Newsletter Module: `MailBeez > MailBeez Modules > Newsletter Advanced`.
1. On the right hand side, click on button <span style="color:#303030; font-family: 'courier';">Edit Campaigns</span>. 
1. Create a new campaign and name it e.g. <span style="color:#303030; font-family: 'courier';">Promotion A</span>. Enter a description, and as `default list`, select the previously created list `Promotion A`. Click <span style="color:#303030; font-family: 'courier';">Insert</span> to save the campaign.
1. Select the newly created campaign and click on <span style="color:#303030; font-family: 'courier';">Edit Campaign items</span>.
1. Create a new Newsletter - select the coupon template - and click <span style="color:#303030; font-family: 'courier';">New newsletter</span>.
1. Scroll down to `Select Coupon-Template for this Newsletter` to select or set-up a new coupon. Click <span style="color:#303030; font-family: 'courier';">Update</span> to save.
1. Configure the `active until` date to <span style="color:#303030; font-family: 'courier';">01/01/2099</span> (sets the newsletter to virtually never expire) and click <span style="color:#303030; font-family: 'courier';">Update</span> to save.
1. Select `inherit from campaign` as the List for this Newsletter .

Now, design the email with your promotion and product info. (Click on the `+` icon in the editor to add layout elements.)

>>>>>If your store is set up for several languages, you need to design the other language templates as well.

Once you are happy with your design and test emails, you can click on `ready for sending` to activate the newsletter.

That’s it.. you’re done!
