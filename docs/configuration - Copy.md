---
layout: default
title: Request
nav_order: 2
---

# Request
{: .no_toc }


### RequestObject - Class
You have to create an Instance for RequestObject and pass to the “BreadwinnerAPI.call()” method as one of the parameters. RequestObject req = new RequestObject(); It consists of the following variables:

## Options 
It is a collection of type Map (Map<String, Object>), used to pass any type of config settings that we enable Ex: below options used for fetching records. contactid, ContactNumber, where, pagenumber, modifiedafter, – for contacts Invoicenumber, Invoiceid, where, pagenumber, modifiedafter – for invoices

## xeroCustomer
It is an instance of the AccountWrapper class. To Create/Insert customer we should pass values to variables which are needed.

Ex: BreadwinnerAPI.AccountWrapper sc = new BreadwinnerAPI.AccountWrapper(); sc.name=’Test Customer’; //For all other variables you can refer here req.xeroCustomer = sc;

## xeroInvoice
It is an instance of the Invoice class. To Create/Insert customer we should pass values to variables which are needed.
Ex: BreadwinnerAPI.Invoice sc = new BreadwinnerAPI.Invoice(); sc.CustomerId=’Test Customer’; //For all other variables you can refer here sc.description=’desc’;… req.xeroInvoice = sc;

## Request Actions
It’s a string, used to define the type of action that needs to be performed. We are providing below types of actions.

<ul>

<li>createCustomer - To create the customer in both Xero and Salesforce.</li>
<li>updateCustomer - To update the customer in both Xero and salesforce.</li>
<li>fetchCustomers - To get a list of customers. Ex: req.action = ‘createCustomer’;.</li>
<li>Createinvoice - To create the Invoice in both Xero and Salesforce..</li>
<li>Updateinvoice - To create the Invoice in both Xero and Salesforce.</li>
<li>Fetchinvoice - To get a list of Invoice(s).</li>
<li>Createbill - To create the Bill in both Xero and Salesforce.</li>
<li>Updatebill - To update the Bill in both Xero and salesforce.</li>
<li>Fetchbill - To get a list of Bill(s).</li>
<li>Createpurchaseorder - To create the Purchase Order in both Xero and Salesforce.</li>
<li>Updatepurchaseorder - To update the Purchase Order in both Xero and salesforce.</li>
<li>Fetchpurchaseorder - To get a list of Purchase Order(s).</li>

</ul>