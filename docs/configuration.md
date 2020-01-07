---
layout: default
title: Request
nav_order: 2
---

# Request
{: .no_toc }


### RequestObject - Class
You have to create an Instance for RequestObject and pass to the "BreadwinnerAPI.call()” method as one of the parameters. <br/>
RequestObject req = new RequestObject(); 

It consists of the following variables:
## 1. Options 
It is a collection of type Map (Map<String, Object>), used to pass any type of config settings that we enable.
    below options used for fetching records. <br/>
    contactid, ContactNumber, where, pagenumber, modifiedafter, – for contacts <br/>
    Invoicenumber, Invoiceid, where, pagenumber, modifiedafter – for invoices <br/>
Ex:  req.options.put('pagenumber','1');

## 2. xeroCustomer
It is an instance of the bw_xero_api01.AccountWrapper class. To Create/Insert customer we should pass values to variables which are needed. For all xeroCustomer variables you can refer [here]({{ site.baseurl }}{% link docs/CustomerOperations/CustomerOperations.md %})
```yaml
Ex: bw_xero_api01.BreadwinnerAPI.AccountWrapper XContact = new bw_xero_api01.BreadwinnerAPI.AccountWrapper();
    XContact.name=’Test Customer’; 
    req.xeroCustomer = sXContactc;
```

## 3. xeroInvoice
It is an instance of the Invoice class. To Create/Insert customer we should pass values to variables which are needed. For all xeroInvoice variables you can refer [here]({{ site.baseurl }}{% link docs/InvoiceOperations/InvoiceOperations.md %}) 
```yaml
Ex: bw_xero_api01.BreadwinnerAPI.Invoice inv = new bw_xero_api01.BreadwinnerAPI.Invoice();
    inv.CustomerId=’Test Customer’; 
    inv.description=’desc’;… 
    req.xeroInvoice = inv;
```
## Request Actions
It’s a string, used to define the type of action that needs to be performed. We are providing below types of actions.

<ul>

<li><b>createCustomer</b>: To create the customer in both Xero and Salesforce.</li>
<li><b>updateCustomer</b>: To update the customer in both Xero and salesforce.</li>
<li><b>fetchCustomers</b>: To get a list of customers.</li>
<li><b>createinvoice</b> To create the Invoice in both Xero and Salesforce..</li>
<li><b>updateinvoice</b>: To create the Invoice in both Xero and Salesforce.</li>
<li><b>fetchinvoice</b>: Use this action to retrieve one or many Invoices.</li>
<li><b>createbill</b>: To create the Bill in both Xero and Salesforce.</li>
<li><b>updatebill</b>: To update the Bill in both Xero and salesforce.</li>
<li><b>fetchbill</b>: Use this action to retrieve one or many Bills.</li>
<li><b>createpurchaseorder</b>: To create the Purchase Order in both Xero and Salesforce.</li>
<li><b>updatepurchaseorder</b>: To update the Purchase Order in both Xero and salesforce.</li>
<li><b>fetchpurchaseorder</b>: Use this action to retrieve one or many purchase orders.</li>

</ul>