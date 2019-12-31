---
layout: default
title: Update Purchase Order
parent: Invoice Operations
nav_order: 8
---

# Update Purchase Order

## Sample Code

```scss
try{
             BreadwinnerAPI.RequestObject req = new  BreadwinnerAPI.RequestObject();
             Invoice xi = new Invoice ();
xi.InvoiceID = '5eac31f6-a05f-4a84-b3aa-47154c82afca';
xi.DueDate = string.valueof(system.today()+30);
Invoice.LineItemWrapper li = new Invoice.LineItemWrapper();
li.ItemCode = ''; li.Description ='li desc';li.UnitAmount=500;li.Quantity=3;li.AccountCode='200';
list<Invoice.LineItemWrapper> lineitems = new list<Invoice.LineItemWrapper>();
lineitems.add(li);
xi.LineItems = lineitems;
xi.ClientId = '39efa556-8dda-4c81-83d3-a631e59eb6d3';
req.xeroInvoice= xi;


             BreadwinnerAPI.ResponseObject res =  BreadwinnerAPI.call('updatePurchaseOrder', req);
             if(res.errors.size()>0){
                 for(BreadwinnerAPI.Error er :res.errors){
                     System.debug(er); 
                 }
             }
 	system.debug('created customer' +res.Invoice);
         }catch(Exception ex){
             System.debug('Exception occurred while creating customers in Stripe.'+ex.getStackTraceString());
         }
```