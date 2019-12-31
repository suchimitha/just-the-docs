---
layout: default
title: Invoice Operations
nav_order: 3
has_children: true
permalink: /docs/InvoiceOperations
---

# Invoice Operations

The following is required to create or update a Invoice

| Field  | Type                          | Description|
|:----------|:-------------------------------------|
| InvoiceNumber      | String |	Invoice - Unique alpha numeric code identifying invoice ( when missing will auto-generate from your Organisation Invoice Settings) (max length = 255)	Bill - non-unique alpha numeric code identifying invoice. This value will also display as Reference in the UI. (max length = 255)  |
| Reference   | String  | Invoice only - additional reference number (max length = 255)                 |
| BrandingThemeID  | String  | Branding Theme Id or value (max length = 255)              |
| CurrencyCode  | String | The currency that invoice has been raised in              |
| OpportunityId  | Id | Salesforce opportunity Id to map Invoice              |
| AccountId   | Id | Salesforce Account Id to map Invoice              |
| InvoiceDate | Date | Date invoice was issued - YYYY-MM-DD. If the Date element is not specified it will default to the current date based on the timezone setting of the organisation              |
| DueDate  | String | Date invoice is due - YYYY-MM-DD              |
| ClientId   | String | Xero generated unique identifier for Xero Contact (Xero Id)              |
| Contact  | ContactWrapper | Last name of contact person (max length = 255)              |
| LineItems  | LineItemWrapper| See LineItems. The LineItems collection can contain any number of individual LineItem sub-elements.              |

| AttentionTo  | String | The person that the delivery is going to              |
| DeliveryAddress  | String | The address the goods are to be delivered to              |
| DeliveryInstructions  | String | A free text field for instructions (500 characters max)              |
| Telephone  | String | The phone number for the person accepting the delivery              |
| PurchaseOrderID | String | Xero generated unique identifier for purchase order              |
| PurchaseOrderNumber | String | Last name of contact person (max length = 255)              |
| DeliveryDate | String | Date the goods are to be delivered - YYYY-MM-DD              |
| PurchaseOrderDate | String | Date purchase order was issued - YYYY-MM-DD. If the Date element is not specified then it will default to the current date based on the timezone setting of the organisation              |


| Field  | Type                          | Description|
|:----------|:-------------------------------------|
| ItemCode        | String | Xero generated identifier for an item  |
| Description        | String | The sales description of the item  |
| TaxType        | String | Used as an override if the default Tax Code for the selected AccountCode is not correct   |
| AccountCode        | String | Default account code to be used for purchased/sale. Not applicable to the purchase details of tracked items  |
| LineItemID        | String | Xero generated unique  |
| UnitAmount        | Decimal  | Unit Price of the item. By default UnitPrice is rounded to two decimal places. You can use 4 decimal places by adding the unitdp=4 querystring parameter to your request.  |
| TaxAmount       | Decimal | Full name of contact/organisation (max length = 255)  |
| LineAmount         | Decimal | Full name of contact/organisation (max length = 255)  |
| Quantity         | Decimal | The quantity of the item on hand  |
| DiscountRate            | Decimal | The Discount rate of the item  |
| Tracking        | TrackingItemWrapper | TrackingItemWrapper type  |


| TrackingItemWrapper Field  | Type                          |
|:----------|:-------------------------------------|
| Name         | String | The name of the tracking category (max length = 100)  |
| Option          | String  | |
| TrackingCategoryID         | String | The Xero identifier for a tracking category  |
