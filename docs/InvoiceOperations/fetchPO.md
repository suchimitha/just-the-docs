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
    bw_xero_api01.BreadwinnerAPI.RequestObject req = new  bw_xero_api01.BreadwinnerAPI.RequestObject();
    req.options.put('page','1');

    bw_xero_api01.BreadwinnerAPI.ResponseObject res =  bw_xero_api01.BreadwinnerAPI.call('fetchPurchaseOrder', req);
    if(res.errors.size()>0){
        for(bw_xero_api01.BreadwinnerAPI.Error er :res.errors){
            System.debug(er); 
        }
    }
    system.debug('Purchase Orders '+res);
}catch(Exception ex){
    System.debug('Exception occurred while creating customers in Stripe.'+ex.getStackTraceString());
}
```