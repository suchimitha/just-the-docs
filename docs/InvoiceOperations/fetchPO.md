---
layout: default
title: Fetch Purchase Order
parent: Invoice Operations
nav_order: 9
---

# Fetch Purchase Order

## Sample Code

```scss
try{
             BreadwinnerAPI.RequestObject req = new  BreadwinnerAPI.RequestObject();
 	req.options.put('invoicenumber','INV-0041');
    req.options.put('page','1');
        
     BreadwinnerAPI.ResponseObject res =  BreadwinnerAPI.call('fetchPurchaseOrder', req);
             if(res.errors.size()>0){
                 for(BreadwinnerAPI.Error er :res.errors){
                     System.debug(er); 
                 }
             }
 	system.debug('created customer +res.Invoice);
         }catch(Exception ex){
             System.debug('Exception occurred while creating customers in Stripe.'+ex.getStackTraceString());
         }
```