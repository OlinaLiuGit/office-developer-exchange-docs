---
title: "Argument"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Argument
api_type:
- schema
ms.assetid: 15b0bfb8-2448-4ceb-aeac-965115e0fb72
description: "The Argument element specifies arguments to the action."
---

# Argument

The **Argument** element specifies arguments to the action. 
  
```
<Argument Value=""/>
```

 **ProtectionRuleArgumentType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**Value** <br/> |A non-empty string value that represents the value of an argument to the action part of a protection rule. This attribute is required.  <br/> |
   
#### Child elements

None.
  
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Action (ProtectionRuleActionType)](action-protectionruleactiontype.md) <br/> |Identifies what action must be executed if the condition part of the rule matches.  <br/> |
   
## Text value

None.
  
## Remarks

The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.
  
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

