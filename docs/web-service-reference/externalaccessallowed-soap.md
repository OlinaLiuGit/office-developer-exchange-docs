---
title: "ExternalAccessAllowed (SOAP)"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
ms.assetid: 967df8c0-ee95-4202-b037-0c4b9fbbf5ee
description: "The ExternalAccessAllowed element indicates whether a document sharing location is available to outside connections."
---

# ExternalAccessAllowed (SOAP)

The **ExternalAccessAllowed** element indicates whether a document sharing location is available to outside connections. 
  
```XML
<ExternalAccessAllowed /> 
```

 **Boolean**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[DocumentSharingLocation (SOAP)](documentsharinglocation-soap.md) <br/> |Represents location and metadata information for a document sharing location.  <br/> |
   
## Text value

The Boolean value of the **ExternalAccessAllowed** element indicates whether the sharing location is available to outside connections. 
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Schema Name  <br/> |Autodiscover schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |True  <br/> |
   
## See also

#### Reference

[GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)
#### Concepts

[Autodiscover web service reference for Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[SOAP Autodiscover XML elements for Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)
