---
layout: default
title: Home
nav_order: 1
description: "Just the Docs is a responsive Jekyll theme with built-in search that is easily customizable and hosted on GitHub Pages."
permalink: /
---

# Breadwinner API for Xero
{: .fs-9 }


---

## Introduction
Users can use this Breadwinner global API and make requests to Xero. Request & responses are defined in such a way that, you can make use of them and form the required things for the request and also to handle the response.

We have created two Handlers, one is for Request and another is for Response. They are named as RequestObject and ResponseObject respectively.

Currently, we are providing API to create, update and fetching of Xero Contacts, Invoices, Bills, and Purchase Orders from Salesforce to Xero.

Breadwinner Provides Apex classes and methods. Users can use these, in their own custom Apex code. The following are the classes and methods.

BreadwinnerAPI - Class This is a global Class where RequestObject and ResponseObject are present. So you can access these Classes from BreadwinnerAPI Class.

## Methods
Call - call(String action, RequestObject request) This is a global method present in BreadwinnerAPI’s class. It takes two parameters. 
### 1. Action: Used to define the type of action that needs to be performed. 
E.g.: createCustomer, createInvoice,… 
### 2. Request: An instance of RequestObject is accepted.

### Signature
global static bw_xero_api01.BreadwinnerAPI.Response call(‘Action’,bw_xero_api01.BreadwinnerAPI.Request request)

### BreadwinnerAPI inner classes
<ul>
<li>RequestObject - Class</li>
<li>ResponseObject - Class</li>
</ul>




---
