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

## BreadwinnerAPI Class 
This is a global Class where RequestObject and ResponseObject are present. So you can access these Classes from BreadwinnerAPI Class.

### Namespace
"bw_xero_api01" : Use this name space to access BreadwinnerApi class and methods. 

## BreadwinnerAPI Methods
The following are methods for BreadwinnerAPI. All are instance methods.
<ul><li><b>Call()</b></li></ul>
This is a global method present in BreadwinnerAPI’s class and returns list of Customers or Invoices in the form of [BreadwinnerAPI.Response]({{ site.baseurl }}{% link docs/response.md %}). It takes two parameters.

1. <b>Action</b>: Used to define the type of action that needs to be performed.<br/>
E.g : createCustomer, createInvoice,… see [List of actions]({{ site.baseurl }}{% link docs/configuration.md %})
2. <b>Request</b>: An instance of RequestObject is accepted.<br/>
E.g :  BreadwinnerAPI.RequestObject req = new BreadwinnerAPI.RequestObject();

### Signature
global BreadwinnerAPI.Response call('Action', BreadwinnerAPI.Request request)

### BreadwinnerAPI inner classes
<ul>
<li>[RequestObject]({{ site.baseurl }}{% link docs/configuration.md %}) - Class</li>
<li>[ResponseObject]({{ site.baseurl }}{% link docs/response.md %}) - Class</li>
</ul>




---
