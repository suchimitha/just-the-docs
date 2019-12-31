---
layout: default
title: Request
nav_order: 2
---

# Request
{: .no_toc }


### RequestObject - Class
You have to create an Instance for RequestObject and pass to the “bw_xero_api01.BreadwinnerAPI.call()” method as one of the parameters. RequestObject req = new RequestObject(); It consists of the following variables:

## Options 
It is a collection of type Map (Map<String, Object>), used to pass any type of config settings that we enable. 
Ex: below options used for fetching records. contactid, ContactNumber, where, pagenumber, modifiedafter, – for contacts Invoicenumber, Invoiceid, where, pagenumber, modifiedafter – for invoices

## xeroCustomer
It is an instance of the bw_xero_api01.AccountWrapper class. To Create/Insert customer we should pass values to variables which are needed.

Ex: 
    bw_xero_api01.BreadwinnerAPI.AccountWrapper sc = new bw_xero_api01.BreadwinnerAPI.AccountWrapper(); 

    sc.name=’Test Customer’; //For all other variables you can refer [here]({{ site.baseurl }}{% link docs/CustomerOperations/CustomerOperations.md %})

    req.xeroCustomer = sc;

## xeroInvoice
It is an instance of the Invoice class. To Create/Insert customer we should pass values to variables which are needed.

Ex: bw_xero_api01.BreadwinnerAPI.Invoice inv = new bw_xero_api01.BreadwinnerAPI.Invoice(); 

    inv.CustomerId=’Test Customer’; //For all other variables you can refer [here]({{ site.baseurl }}{% link docs/InvoiceOperations/InvoiceOperations.md %}) 

    inv.description=’desc’;… 

    req.xeroInvoice = inv;

## Request Actions
It’s a string, used to define the type of action that needs to be performed. We are providing below types of actions.

<ul>

<li>createCustomer - To create the customer in both Xero and Salesforce.</li>
<li>updateCustomer - To update the customer in both Xero and salesforce.</li>
<li>fetchCustomers - To get a list of customers.</li>
<li>createinvoice - To create the Invoice in both Xero and Salesforce..</li>
<li>updateinvoice - To create the Invoice in both Xero and Salesforce.</li>
<li>fetchinvoice - To get a list of Invoice(s).</li>
<li>createbill - To create the Bill in both Xero and Salesforce.</li>
<li>updatebill - To update the Bill in both Xero and salesforce.</li>
<li>fetchbill - To get a list of Bill(s).</li>
<li>createpurchaseorder - To create the Purchase Order in both Xero and Salesforce.</li>
<li>updatepurchaseorder - To update the Purchase Order in both Xero and salesforce.</li>
<li>fetchpurchaseorder - To get a list of Purchase Order(s).</li>

</ul>