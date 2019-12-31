---
layout: default
title: Fetch Xero Contact
parent: Contact Operations
nav_order: 3
---

# Fetch Xero Contact

## sample code 

```scss
try{
    bw_xero_api01.BreadwinnerAPI.RequestObject req = new  bw_xero_api01.BreadwinnerAPI.RequestObject();
    req.options.put('invoicenumber','INV-0041');
    req.options.put('page','1');

    bw_xero_api01.BreadwinnerAPI.ResponseObject res =  bw_xero_api01.BreadwinnerAPI.call('fetchinvoice', req);
        if(res.errors.size()>0){
            for(bw_xero_api01.BreadwinnerAPI.Error er :res.errors){
                System.debug(er); 
            }
        }
    system.debug('created customer/////////' +res);
}catch(Exception ex){
    System.debug('Exception occurred while creating customers in Stripe.'+ex.getStackTraceString());
}
```