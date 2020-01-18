---
layout: default
title: Response
nav_order: 2
---

# Response
{: .no_toc }

This method allows users to retrieve stuff.


### ResponseObject - Class
When we call “BreadwinnerAPI.call()” method, User would get the response in the form of ResponseObject wrapper. It consists of following variables.<br/>

### Status: 
It’s a string, which represents the Response Code/status code of the request. <br/>
Ex: ‘200’ - for success Response.

### xeroCustomer:
It’s XeroCustomer wrapper instance which contains created Xero Customer data along with Xero Id.<br/>
Ex: bw_xero_api01.AccountWrapper AC = Response.xeroCustomer;

### xeroInvoice:
It’s Xero Invoice wrapper instance which contains created Xero Invoice data along with Xero Id. <br/>
Ex: Invoice sc = Response.XeroInvoice

### xeroIdCustomerMap:
    It's a map of Xero Customers wrapper. 

### xeroIdInvoiceMap :
    It's a map of Xero Invoices wrapper.

### rawResponse:
    It's a raw response from Xero. 

### Errors:
It is a list of instances of the “Error” class. You can understand the reason for issues while interacting with Xero based on the error type returned.

Error class contains the following variables.
<ul>
<li><b>type</b>: The type of error returned. One of api_connection_error, api_error, authentication_error, card_error, idempotency_error, invalid_request_error, or rate_limit_error.</li>
<li><b>message</b>: Represents the Error.</li>
<li><b>elements</b>:</li>
<li><b>code</b>: For some errors that could be handled programmatically, a short string indicating the error code reported.</li>
<li><b>doc_url</b>: A URL to more information about the error code reported.</li>
<li><b>description</b>: Represents the extra info regarding the error or exception.</li>
<li><b>param</b>: If the error is parameter-specific, that parameter related to the error is returned. For example, you can use this to display a message near the correct form field.</li>
<li><b>xero_type</b>:</li>
<li><b>decline_code</b>:</li>
</ul>
Ex: message=REQUIRED_FIELD_MISSING : name, message=Enter the Xero customer name. param=XeroCustomer.name