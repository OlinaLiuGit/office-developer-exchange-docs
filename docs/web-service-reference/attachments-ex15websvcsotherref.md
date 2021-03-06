---
title: "Attachments"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Attachments
api_type:
- schema
ms.assetid: b470e614-34bb-44f0-8790-7ddbdcbbd29d
description: "The Attachments element contains the items or files that are attached to an item in the Exchange store."
---

# Attachments

The **Attachments** element contains the items or files that are attached to an item in the Exchange store. 
  
```
<Attachments>
   <ItemAttachment/>
   <FileAttachment/>
</Attachments>
```

 **ArrayOfAttachmentsType** and **NonEmptyArrayOfAttachmentsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |Represents an Exchange item that is attached to another Exchange item.  <br/> |
|[FileAttachment](fileattachment.md) <br/> |Represents a file that is attached to an item in the Exchange store.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[CreateAttachment](createattachment.md) <br/> |Defines a request to create an attachment to an item in the Exchange store.  <br/> The following is the XPath expression to this element:  `/CreateAttachment` <br/> |
|[AcceptItem](acceptitem.md) <br/> | Represents an Accept reply to a meeting request.  <br/>  The following are some of the XPath expressions to this element:  <br/>  `/CreateItem/Items` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[DeclineItem](declineitem.md) <br/> |Represents a Decline reply to a meeting request.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Represents a Tentative reply to a meeting request.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Removes an item from the Exchange store.  <br/> |
|[Item](item.md) <br/> |Represents a generic Exchange item.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Represents a meeting in the Exchange store.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Represents a meeting request in the Exchange store.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Represents a meeting response in the Exchange store.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Represents a meeting cancellation in the Exchange store.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Represents an Exchange e-mail message.  <br/> |
|[Task](task.md) <br/> |Represents a task in the Exchange store.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Represents an Exchange calendar item.  <br/> |
|[Contact](contact.md) <br/> |Represents an Exchange contact item.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Represents a distribution list.  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |Contains the status and result of a single CreateAttachment request.  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |Contains the status and result of a GetAttachment request.  <br/> |
   
## Remarks

The **Attachments** elements have the same child elements but are based on different types: **ArrayOfAttachmentsType** and **NonEmptyArrayOfAttachmentsType**. The types define whether a child element is required. The **ArrayOfAttachmentsType** is only used in the response message. It is also important to note that these elements occur in both the messages and types namespaces. 
  
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

