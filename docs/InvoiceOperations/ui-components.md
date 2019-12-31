---
layout: default
title: Invoice Operations
nav_order: 3
has_children: true
permalink: /docs/InvoiceOperations
---

# Invoice Operations

The following is required to create or update a Invoice

| Field  | Type               | Valid for           | Description|
|:----------|:-------------------------------------|
| InvoiceNumber      | String | All | Invoice - Unique alpha numeric code identifying invoice ( when missing will auto-generate from your Organisation Invoice Settings) (max length = 255)	Bill - non-unique alpha numeric code identifying invoice. This value will also display as Reference in the UI. (max length = 255)  |
| Reference   | String  |  All | Invoice only - additional reference number (max length = 255)                 |
| BrandingThemeID  | String  | All | Branding Theme Id or value (max length = 255)              |
| CurrencyCode  | String |  All | The currency that invoice has been raised in              |
| OpportunityId  | Id |  All | Salesforce opportunity Id to map Invoice              |
| AccountId   | Id |  All | Salesforce Account Id to map Invoice              |
| InvoiceDate | Date |  Invoice, Bill | Date invoice was issued - YYYY-MM-DD. If the Date element is not specified it will default to the current date based on the timezone setting of the organisation              |
| DueDate  | String |  Invoice, Bill |Date invoice is due - YYYY-MM-DD              |
| ClientId   | String |  All | Xero generated unique identifier for Xero Contact (Xero Id)              |
| Contact  | ContactWrapper |  All | Last name of contact person (max length = 255)              |
| LineItems  | LineItemWrapper|  All | See LineItems. The LineItems collection can contain any number of individual LineItem sub-elements.              |
| AttentionTo  | String |  Purchase Order | The person that the delivery is going to              |
| DeliveryAddress  | String | Purchase Order | The address the goods are to be delivered to              |
| DeliveryInstructions  | String | Purchase Order | A free text field for instructions (500 characters max)              |
| Telephone  | String | Purchase Order | The phone number for the person accepting the delivery              |
| PurchaseOrderID | String | Purchase Order | Xero generated unique identifier for purchase order              |
| PurchaseOrderNumber | String | Purchase Order | Last name of contact person (max length = 255)              |
| DeliveryDate | String | Purchase Order | Date the goods are to be delivered - YYYY-MM-DD              |
| PurchaseOrderDate | String | Purchase Order | Date purchase order was issued - YYYY-MM-DD. If the Date element is not specified then it will default to the current date based on the timezone setting of the organisation              |


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
