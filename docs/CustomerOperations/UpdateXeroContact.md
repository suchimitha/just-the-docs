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
	BreadwinnerAPI.RequestObject req = new  BreadwinnerAPI.RequestObject();	
	AccountWrapper str = new AccountWrapper();
	str.name='MY5 NAME Test Create -'; 
	str.contactId ='tempId';		
	req.xeroCustomer = str;

	BreadwinnerAPI.ResponseObject res =  BreadwinnerAPI.call('updateCustomer', req);
	if(res.errors.size()>0){
		for(BreadwinnerAPI.Error er :res.errors){
			System.debug(er); 
		}
	}
	system.debug('created customer' +res.xeroCustomer);
}catch(Exception ex){
	System.debug('Exception occurred while creating customers in Xero.'+ex.getStackTraceString());
}
```