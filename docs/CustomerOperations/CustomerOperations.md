---
layout: default
title: Contact Operations
nav_order: 5
has_children: true
permalink: docs/CustomerOperations
---

# Contact Operations


The following is required to create or update a contact

| Field  | Type                          |
|:----------|:-------------------------------------|
| Name      | Full name of contact/organisation (max length = 255)  |
| FirstName | First name of contact person (max length = 255)                 |
| LastName  | Last name of contact person (max length = 255)              |
| EmailAddress  | Email address of contact person (umlauts not supported) (max length = 255)             |
| TaxNumber | Tax number of contact - this is also known as the ABN (Australia), GST Number (New Zealand), VAT Number (UK) or Tax ID Number (US and global) in the Xero UI depending on which regionalized version of Xero you are using (max length = 50)                |
| AccountsReceivableTaxType      | Default tax type used for contact on AR invoices              |
| `PaymentTerms`      | The default payment terms for the contact - see  PaymentTermWrapper fields below             |
| BillingAttentionTo      | max length = 255              |
| BillingStreet      | max length = 500              |
| BillingCity       | max length = 255              |
| BillingState      | max length = 255              |
| BillingCountry      | max length = 50, [A-Z], [a-z] only              |
| BillingPostalCode      | max length = 50             |
| Phone      |        Phone number of contact       |
| ContactID      | Xero identifier              |


| PaymentTermWrapper Fields  | Type                          |
|:----------|:-------------------------------------|
| `Sales`      | BillsOrSalesWrapper   |

| BillsOrSalesWrapper Fields  | Type                          |
|:----------|:-------------------------------------|
| Day       |   |
| Type       | Payment Terms (DAYSAFTERBILLDATE, DAYSAFTERBILLMONTH, OFCURRENTMONTH, OFFOLLOWINGMONTH)  |

{: .fs-6 .fw-300 }
