---
layout: default
title: Update Xero Contact
parent: Contact Operations
nav_order: 2
---

# Update Xero Contact

## sample code 

```scss
try{
	bw_xero_api01.BreadwinnerAPI.RequestObject req = new  bw_xero_api01.BreadwinnerAPI.RequestObject();	
	bw_xero_api01.AccountWrapper str = new bw_xero_api01.AccountWrapper();
	str.name='MY5 NAME Test Create -'; 
	str.contactId ='tempId';		
	req.xeroCustomer = str;

	bw_xero_api01.BreadwinnerAPI.ResponseObject res =  bw_xero_api01.BreadwinnerAPI.call('updateCustomer', req);
	if(res.errors.size()>0){
		for(bw_xero_api01.BreadwinnerAPI.Error er :res.errors){
			System.debug(er); 
		}
	}
	system.debug('created customer' +res.xeroCustomer);
}catch(Exception ex){
	System.debug('Exception occurred while creating customers in Xero.'+ex.getStackTraceString());
}
```