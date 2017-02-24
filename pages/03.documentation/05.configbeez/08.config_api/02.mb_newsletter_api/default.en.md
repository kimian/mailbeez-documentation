---
title: 'Newsletter API'
template: docs
taxonomy:
    category: [docs]
    tag: [pro]
    
---
This API Module groups API calls related to the [MailBeez Newsletter Advanced](/documentation/mailbeez/newsletter/) module.


##Newsletter Subscriber API

The Newsletter Subscriber API allows you to add and opt-in a customer or prospect to the Newsletter-lists.


### Add an Email-Address
Opt-In Email will be send

This API-Call can be used to built a custom sign-up-form e.g. using AJAX or to trigger the subscription process from any other system.


POST `http://<myshop.com>/mailhive.php/api/public/v1.0/newsletter/add/`


#### Mandatory Parameters

| Parameter    	| Type 	| Description                            	|
|--------------	|------	|----------------------------------------	|
| email  	    | text  | Email-Address of Customer or Prospect	    |


#### Optional Parameters

| Parameter    	| Type 	| Description                            	                                |
|--------------	|------	|----------------------------------------	                                |
| firstname 	| text  | Firstname (ignored for customers), default -1	                            |
| lastname 	    | text  | Lastname (ignored for customers), default -1                              |
| gender   	    | text  | gender (ignored for customers)           	                                |
| language_id   | int 	| language-id                            	                                |
| topic_ids     | int / list 	| single or multiple (separated by ,) id of topics to subscribe for |




####Return


The API-Call returns a `JSON-Array` with following values:

**invalid Email Address**  
`{"error":"invalid_email"}`  
The Email-Address seems to be invalid

**Email-Adress exists**  
`{"error":"duplicate"}`  
The Email-Address belongs to a customer with valid newsletter subscription or to an existing prospect with valid subscription

**Successfully added Email-Adress**  
`{"error":false}`  
The Email-Address was successfully added and an opt-in email based on the matching type (customer | prospect) with confirmation-link is sent.



>>>> Check out the built-in signup-forms in `/mailhive/mailbeez/mb_newsletter/includes/templates` how to use the API-Calls with AJAX.


### Customers Confirmation 
Confirmation Message will be shown and Customer Confirmation-Email with coupon will be send.

This API-Call is triggered when a customer clicks on the confirmation link in the customer confirmation email, but can also be used from any other system.

GET `http://<myshop.com>/mailhive.php/api/public/v1.0/newsletter/confirm/customers/[confirmation_code]`


#### Mandatory Parameters

| Parameter    	    | Type 	| Description                            	|
|--------------	    |------	|----------------------------------------	|
| confirmation-code | text  | unique customer confirmation code	        |

you find the customer confirmation-code in table `mailbeez_newsletter_source_customers`.


### Prospect Confirmation
Confirmation Message will be shown and Prospect Confirmation-Email with coupon will be send.

This API-Call is triggered when a prospect clicks on the confirmation link in the prospects confirmation email, but can also be used from any other system.

GET `http://<myshop.com>/mailhive.php/api/public/v1.0/newsletter/confirm/prospects/[confirmation_code]`


#### Mandatory Parameters

| Parameter    	    | Type 	| Description                            	|
|--------------	    |------	|----------------------------------------	|
| confirmation-code | text  | unique prospect confirmation code	        |

you find the prospects confirmation-code in table `mailbeez_newsletter_source_prospects`.



####Example

```
http://<myshop.com>/mailhive.php/api/public/v1.0/newsletter/confirm/customers/53efef14241107e0fbb7750c4d3023a5
```






### Update Prospect Data


>>>>you can only update prospects which are not yet converted into customers

This API-Call can be used to update prospect data.


POST `http://<myshop.com>/mailhive.php/api/public/v1.0/newsletter/prospect/update/[base64_encode(<email>)]`


#### Mandatory Parameters

| Parameter    	| Type 	| Description                            	|
|--------------	|------	|----------------------------------------	|
| base64_encode(email)    | text  | base64_encode of Email-Address of Prospect	    |


#### Optional Parameters

| Parameter    	| Type 	| Description                                                      |
|--------------	|------	|----------------------------------------	                                |
| firstname 	| text  | Firstname, default -1	                            |
| lastname 	    | text  | Lastname, default -1                              |
| gender   	    | text  | gender           	                                |
| language_id   | int 	| language-id                            	                                |
| redirect      | url 	| if set the call redirects to the given URL adding `result` as parameter  |




####Return

With a given redirect URL the API-will redirect adding parameter `result`, otherwise the API-Call returns a `JSON-Array` with following values:

**invalid prospect**  
`{"error":"invalid_prospect"}`  
The Email-Address is not registered as prospect

**is customer**  
`{"error":"is_customer"}`  
The prospect email address belongs to a customer, no update

**Successfully updated prospect data**  
`{"error":false}`  
The Email-Address was successfully added and an opt-in email based on the matching type (customer | prospect) with confirmation-link is sent.
(in redirect mode: `result=OK`)



### Update Subscriber Topics

This API-Call redirects to the form for updating subscriber Topics

GET `http://<myshop.com>/mailhive.php/api/public/v1.0/newsletter/topics/web/[base64_encode(<email>)]`


#### Mandatory Parameters

| Parameter    	| Type 	| Description                            	|
|--------------	|------	|----------------------------------------	|
| [base64_encode(<email>)]    | text  | base64_encode of Email-Address of Subscriber (Customer or Prospect)	    |

