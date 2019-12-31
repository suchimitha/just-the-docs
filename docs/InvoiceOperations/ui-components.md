---
layout: default
title: Invoice Operations
nav_order: 3
has_children: true
permalink: /docs/InvoiceOperations
---

# Invoice Operations

The following is required to create or update a Invoice

| Field  | Type                          |
|:----------|:-------------------------------------|
| InvoiceNumber      | 	Invoice - Unique alpha numeric code identifying invoice ( when missing will auto-generate from your Organisation Invoice Settings) (max length = 255)	Bill - non-unique alpha numeric code identifying invoice. This value will also display as Reference in the UI. (max length = 255)  |
| Reference   | Invoice only - additional reference number (max length = 255)                 |
| BrandingThemeID  | Branding Theme Id or value (max length = 255)              |
| CurrencyCode  | The currency that invoice has been raised in              |
| OpportunityId  | Salesforce opportunity Id to map Invoice              |
| AccountId   | Salesforce Account Id to map Invoice              |
| InvoiceDate | Date invoice was issued - YYYY-MM-DD. If the Date element is not specified it will default to the current date based on the timezone setting of the organisation              |
| DueDate  | Date invoice is due - YYYY-MM-DD              |
| ClientId   | Xero Contact Id (Xero Id)              |
| Contact  | Last name of contact person (max length = 255)              |
| LineItems  | See LineItems. The LineItems collection can contain any number of individual LineItem sub-elements.              |

| AttentionTo  | The person that the delivery is going to              |
| DeliveryAddress  | The address the goods are to be delivered to              |
| DeliveryInstructions  | A free text field for instructions (500 characters max)              |
| Telephone  | The phone number for the person accepting the delivery              |
| PurchaseOrderID | Xero generated unique identifier for purchase order              |
| PurchaseOrderNumber | Last name of contact person (max length = 255)              |
| DeliveryDate | Date the goods are to be delivered - YYYY-MM-DD              |
| PurchaseOrderDate | Date purchase order was issued - YYYY-MM-DD. If the Date element is not specified then it will default to the current date based on the timezone setting of the organisation              |


| Field  | Type                          |
|:----------|:-------------------------------------|
| ItemCode        | Xero generated identifier for an item  |
| Description        | The sales description of the item  |
| TaxType        | Used as an override if the default Tax Code for the selected AccountCode is not correct   |
| AccountCode        | Default account code to be used for purchased/sale. Not applicable to the purchase details of tracked items  |
| LineItemID        | Full name of contact/organisation (max length = 255)  |
| UnitAmount        | Unit Price of the item. By default UnitPrice is rounded to two decimal places. You can use 4 decimal places by adding the unitdp=4 querystring parameter to your request.  |
| TaxAmount       | Full name of contact/organisation (max length = 255)  |
| LineAmount         | Full name of contact/organisation (max length = 255)  |
| Quantity         | The quantity of the item on hand  |
| DiscountRate            | The Discount rate of the item  |
| Tracking        | TrackingItemWrapper type  |


| TrackingItemWrapper Field  | Type                          |
|:----------|:-------------------------------------|
| Name         | The name of the tracking category (max length = 100)  |
| Option          |   |
| TrackingCategoryID         | The Xero identifier for a tracking category  |
