---
title: "SuggestionsViewOptions"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionsViewOptions
api_type:
- schema
ms.assetid: bb04ae38-e62d-4a69-a479-8ff326ca726e
description: "The SuggestionsViewOptions element contains the options for obtaining meeting suggestion information."
---

# SuggestionsViewOptions

The **SuggestionsViewOptions** element contains the options for obtaining meeting suggestion information. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[SuggestionsViewOptions](suggestionsviewoptions.md)
  
```
<SuggestionsViewOptions>
   <GoodThreshold>...</GoodThreshold>
   <MaximumResultsByDay>...</MaximumResultsByDay>
   <MaximumNonWorkingHourResultsByDay>...</MaximumNonWorkingHourResultsByDay>
   <MeetingDurationInMinutes>...</MeetingDurationInMinutes>
   <MinimumSuggestionQuality>...</MinimumSuggestionQuality>
   <SuggestionIntervalInMinutes>...</SuggestionIntervalInMinutes>
   <DetailedSuggestionsWindow>...</DetailedSuggestionsWindow>
   <CurrentMeetingTime>...</CurrentMeetingTime>
   <GlobalObjectId>...</GlobalObjectId>
</SuggestionsViewOptions>
```

 **SuggestionsViewOptionsType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

None.
  
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[GoodThreshold](goodthreshold.md) <br/> |Specifies the percentage of attendees that must have the time period open for the time period to qualify as a good suggested meeting time.  <br/> |
|[MaximumResultsByDay](maximumresultsbyday.md) <br/> |Specifies the number of suggested meeting times per day returned in the response.  <br/> |
|[MaximumNonWorkHourResultsByDay](maximumnonworkhourresultsbyday.md) <br/> |Specifies the number of suggested results for meeting times outside regular working hours per day.  <br/> |
|[MeetingDurationInMinutes](meetingdurationinminutes.md) <br/> |Specifies the length of the meeting to be suggested.  <br/> |
|[MinimumSuggestionQuality](minimumsuggestionquality.md) <br/> |Specifies the quality of meeting suggestions to be returned in the response.  <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Identifies the time span that is queried for detailed information about suggested meeting times.  <br/> |
|[CurrentMeetingTime](currentmeetingtime.md) <br/> |Represents the start time of a meeting that you want to update with the suggested meeting time results.  <br/> |
|[GlobalObjectId](globalobjectid.md) <br/> |This element is not used.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |Contains the arguments used to obtain user availability information. This is a root element.  <br/> The following is the XPath to this element:  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## Remarks

This element is not required and can only occur once if used. This value can be null if the value of the [FreeBusyViewOptions](freebusyviewoptions.md) element is not null. 
  
> [!NOTE]
> The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed. 
  
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

