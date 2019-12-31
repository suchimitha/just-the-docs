---
layout: default
title: Response
nav_order: 2
---

# Response
{: .no_toc }

This method allows users to retrieve stuff.


### Response
### ResponseObject - Class
When we call “bw_xero_api01.BreadwinnerAPI.call” method, User would get the response in the form of ResponseObject wrapper. It consists of three variables: status: It’s a string, which represents the Response Code/status code of the request. 
Ex: ‘200’ - for success Response.

### Errors:
It is a list of instances of the “Error” class. It will be returned if there are any errors. With these, you can understand the reason for issues while interacting with Xero.

Error class contains the following variables.
<ul>
<li>type: The type of error returned. One of api_connection_error, api_error, authentication_error, card_error, idempotency_error, invalid_request_error, or rate_limit_error.</li>
<li>message: Represents the Error.</li>
<li>elements</li>
<li>code: For some errors that could be handled programmatically, a short string indicating the error code reported.</li>
<li>doc_url: A URL to more information about the error code reported.</li>
<li>description: Represents the extra info regarding the error or exception.</li>
<li>param: If the error is parameter-specific, that parameter related to the error. For example, you can use this to display a message near the correct form field.</li>
<li>xero_type</li>
<li>decline_code</li>

</ul>
Ex: message=REQUIRED_FIELD_MISSING : name, message=Enter the Xero customer name. param=XeroCustomer.name

### xeroCustomer
It’s XeroCustomer wrapper instance which contains created Xero Customer data along with Stipe Id.
Ex: bw_xero_api01.AccountWrapper AC = Response.xeroCustomer;

### xeroInvoice
It’s XeroInvoicewrapper instance which contains created Xero Customer data along with Stipe Id. 
Ex: Invoice sc = Response.XeroInvoice