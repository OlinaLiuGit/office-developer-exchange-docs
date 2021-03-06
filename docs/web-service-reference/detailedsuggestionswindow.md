---
title: "DetailedSuggestionsWindow"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DetailedSuggestionsWindow
api_type:
- schema
ms.assetid: 7b348d63-6a7d-45f4-9562-5c42243d63a5
description: "The DetailedSuggestionsWindow element identifies the time span that is queried for detailed information about suggested meeting times."
---

# DetailedSuggestionsWindow

The **DetailedSuggestionsWindow** element identifies the time span that is queried for detailed information about suggested meeting times. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[SuggestionsViewOptions](suggestionsviewoptions.md)
  
[DetailedSuggestionsWindow](detailedsuggestionswindow.md)
  
```
<DetailedSuggestionsWindow>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
</DetailedSuggestionsWindow>
```

 **Duration**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[StartTime](starttime.md) <br/> |Represents the start of the time span queried for detailed information about suggested meeting times.  <br/> |
|[EndTime](endtime.md) <br/> |Represents the end of the time span queried for detailed information about suggested meeting times.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[SuggestionsViewOptions](suggestionsviewoptions.md) <br/> |Contains the options for obtaining meeting suggestion information.  <br/> The following is the XPath to this element:  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## Remarks

This element is not required.
  
> [!NOTE]
> The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed. 
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Schema Name  <br/> |Types schema  <br/> |
|Validation File  <br/> |Types.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[GetUserAvailability operation](getuseravailability-operation.md)
#### Other resources

[Getting User Availability](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

