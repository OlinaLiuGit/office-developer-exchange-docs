---
title: "DeletedEvent"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeletedEvent
api_type:
- schema
ms.assetid: c4565eb4-b537-466c-b1ff-11602533812b
description: "The DeletedEvent element represents an event in which an item or folder is deleted."
---

# DeletedEvent

The **DeletedEvent** element represents an event in which an item or folder is deleted. 
  
```
<DeletedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</DeletedEvent>
```

 **BaseObjectChangedEventType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Represents an event bookmark in the mailbox events table.  <br/> |
|[TimeStamp](timestamp.md) <br/> |Represents the timestamp of a deleted item or folder mailbox event.  <br/> |
|[FolderId](folderid.md) <br/> |Represents the identifier of the deleted folder.  <br/> |
|[ItemId](itemid.md) <br/> |Represents the identifier of the deleted item.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Represents the identifier of the parent folder of the deleted item or folder before deletion.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[Notification](notification-ex15websvcsotherref.md) <br/> |Contains information about the subscription and the events that have occurred since the last notification.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema name  <br/> |Types schema  <br/> |
|Validation file  <br/> |Types.xsd  <br/> |
|Can be empty  <br/> |False  <br/> |
   
## See also

#### Reference

[Subscribe operation](subscribe-operation.md)
  
[GetEvents operation](getevents-operation.md)
  
[Unsubscribe operation](unsubscribe-operation.md)

