---
title: CSP customer web storefront
description: This site shows a working online store that your customers could use to buy subscriptions to Microsoft products. To make it work for you, configure the offers, add branding, and add a payment method.
ms.assetid: 0726B1CA-97A1-42E6-92AD-25787BFE0C67
ms.date: 10/23/2018
ms.localizationpriority: medium
---

# CSP customer web storefront

**Applies To**

- Partner Center

This site shows a working online store that your customers could use to buy subscriptions to Microsoft products. To make it work for you, configure the offers, add branding, and add a payment method.

> [!NOTE]
> This sample applies only to the global instance of Partner Center. It does not apply to Partner Center for Microsoft Cloud Germany or to Partner Center for Microsoft Cloud for US Government.

## <span id="Get_the_code"/><span id="get_the_code"/><span id="GET_THE_CODE"/>Get the code

[Download the sample code](https://github.com/Microsoft/Partner-Center-Storefront)

## <span id="What_to_change"/><span id="what_to_change"/><span id="WHAT_TO_CHANGE"/>What to change

**Authentication** Before you build the application, update the values in the Web.config file to reflect the Azure AD authentication information you created in [Partner Center authentication](partner-center-authentication.md). Specifically, you should use your integration sandbox account settings during early development or for testing in production (TiP).

- partnerCenter.applicationId
- partnerCenter.applicationSecret
- partnerCenter.domain
- webPortal.clientId
- webPortal.clientSecret
- webPortal.domain
- webPortal.azureStorageConnectionString

**Branding**

The app currently tracks the following company and brand information in BrandingConfiguration.cs and PortalBranding.cs:

- Organization name
- Organization logo
- Header image
- Privacy agreement
- Contact email
- Contact phone number
- Support email
- Support phone number

**Offers**

These are stored as a set of **MicrosoftOffer**s in the **OfferCatalogViewModel**.

**Payment types**

The app currently uses a PayPal gateway, implemented in PayPalGateway.cs.