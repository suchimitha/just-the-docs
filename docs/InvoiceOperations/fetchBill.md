---
layout: default
title: Fetch Bill
parent: Invoice Operations
nav_order: 6
---
# Fetch Bill

## Sample Code

```scss
try{
    bw_xero_api01.BreadwinnerAPI.RequestObject req = new  bw_xero_api01.BreadwinnerAPI.RequestObject();
    //req.options.put('invoicenumber','INV-0041');
    req.options.put('pagenumber','1');

    bw_xero_api01.BreadwinnerAPI.ResponseObject res =  bw_xero_api01.BreadwinnerAPI.call('fetchBill', req);
    if(res.errors.size()>0){
        for(bw_xero_api01.BreadwinnerAPI.Error er :res.errors){
            System.debug(er); 
        }
    }
    system.debug('Bills '+res);
}catch(Exception ex){
    System.debug('Exception occurred while creating customers in Stripe.'+ex.getStackTraceString());
}
```