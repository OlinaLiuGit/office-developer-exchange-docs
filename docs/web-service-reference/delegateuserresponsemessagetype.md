---
title: "DelegateUserResponseMessageType"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegateUserResponseMessageType
api_type:
- schema
ms.assetid: 3dc9552c-1e2d-40ac-a137-827883c2bb88
description: "The DelegateUserResponseMessageType element contains the response message for a single delegate user."
---

# DelegateUserResponseMessageType

The **DelegateUserResponseMessageType** element contains the response message for a single delegate user. 
  
```
<DelegateUserResponseMessageType>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DelegateUser/>
</DelegateUserResponseMessageType>
```

 **DelegateUserResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides an error code that identifies the specific error that the request encountered.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and is reserved for future use. It contains a value of 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
|[DelegateUser](delegateuser.md) <br/> |Identifies a single delegate that is returned in a delegate management response.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages (ArrayOfDelegateUserResponseMessageType)](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |Contains the response messages for an Exchange Web Services delegate management request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[AddDelegate operation](adddelegate-operation.md)
  
[GetDelegate operation](getdelegate-operation.md)
  
[UpdateDelegate operation](updatedelegate-operation.md)
  
[RemoveDelegate operation](removedelegate-operation.md)
#### Concepts

[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)

