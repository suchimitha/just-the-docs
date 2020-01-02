---
layout: default
title: Create Purchase Order
parent: Invoice Operations
nav_order: 7
---

# Create Purchase Order

## Sample Code

```scss
try{
	bw_xero_api01.BreadwinnerAPI.RequestObject req = new  bw_xero_api01.BreadwinnerAPI.RequestObject();	
	bw_xero_api01.Invoice xi = new bw_xero_api01.Invoice ();
	xi.DueDate = string.valueof(system.today());
	bw_xero_api01.Invoice.LineItemWrapper li = new bw_xero_api01.Invoice.LineItemWrapper();
	li.ItemCode = ''; 
	li.Description ='li desc'; 
	li.AccountCode='200';
	li.UnitAmount=300;
	li.Quantity=3;
	list<bw_xero_api01.Invoice.LineItemWrapper> lineitems = new list<bw_xero_api01.Invoice.LineItemWrapper>();
	lineitems.add(li);
	xi.LineItems = lineitems;
	xi.ClientId = '39efa556-8dda-4c81-83d3-a631e59eb6d3';
	req.xeroInvoice= xi;
	bw_xero_api01.BreadwinnerAPI.ResponseObject res =  bw_xero_api01.BreadwinnerAPI.call('createPurchaseOrder', req);
	if(res.errors.size()>0){
		for(bw_xero_api01.BreadwinnerAPI.Error er :res.errors){
			System.debug(er); 
		}
	}
	system.debug('created purchase Order' +res.XeroInvoice);
}catch(Exception ex){
	System.debug('Exception occurred while creating customers in Xero.'+ex.getStackTraceString());
}
```