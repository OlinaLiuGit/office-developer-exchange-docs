---
title: "Time (TimeChangeType)"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Time
api_type:
- schema
ms.assetid: be12e41e-6871-4f6b-b2d4-3dfa404f9ea1
description: "The Time element describes the time when the time changes between standard time and daylight saving time."
---

# Time (TimeChangeType)

The **Time** element describes the time when the time changes between standard time and daylight saving time. 
  
```
<Time/>
```

 **Time**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Daylight](daylight.md) <br/> |Represents the date and time when the time changes from daylight saving time to standard time.  <br/> |
|[Standard](standard.md) <br/> |Represents the date and time when the time changes from daylight saving time to standard time.  <br/> |
   
## Text value

The text value represents the time when the time changes between standard time and daylight saving time.
  
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

