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
    ContactId, ContactNumber, where, PageNumber, ModifiedAfter – for Contacts <br/>
    InvoiceNumber, InvoiceId, where, PageNumber, ModifiedAfter – for Invoices, Bills <br/>
    PurchaseOrderNumber, PurchaseOrderID, where, PageNumber, ModifiedAfter – for PurchaseOrders <br/>
Ex: req.options.put('PageNumber','1');

## 2. xeroCustomer
It is an instance of the AccountWrapper (Xero Contact Wrapper) class. To Create/Insert customer we should pass values to variables which are needed. For all xeroCustomer variables you can refer [here]({{ site.baseurl }}{% link docs/CustomerOperations/CustomerOperations.md %})
```yaml
Ex: bw_xero_api01.BreadwinnerAPI.AccountWrapper XContact = new bw_xero_api01.BreadwinnerAPI.AccountWrapper();
    XContact.name=’Test Customer’; 
    req.xeroCustomer = sXContactc;
```

## 3. xeroInvoice
It is an instance of the Invoice wrapper class. To Create/Insert customer we should pass values to variables which are needed. For all Invoice variables you can refer [here]({{ site.baseurl }}{% link docs/InvoiceOperations/InvoiceOperations.md %}) 
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
<li><b>createInvoice</b> To create the Invoice in both Xero and Salesforce..</li>
<li><b>updateInvoice</b>: To create the Invoice in both Xero and Salesforce.</li>
<li><b>fetchInvoice</b>: Use this action to retrieve one or many Invoices.</li>
<li><b>createBill</b>: To create the Bill in both Xero and Salesforce.</li>
<li><b>updateBill</b>: To update the Bill in both Xero and salesforce.</li>
<li><b>fetchBill</b>: Use this action to retrieve one or many Bills.</li>
<li><b>createPurchaseOrder</b>: To create the Purchase Order in both Xero and Salesforce.</li>
<li><b>updatePurchaseOrder</b>: To update the Purchase Order in both Xero and salesforce.</li>
<li><b>fetchPurchaseOrder</b>: Use this action to retrieve one or many purchase orders.</li>

</ul>