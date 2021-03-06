---
title: "Exporting and importing items by using EWS in Exchange"
 
 
manager: sethgros
ms.date: 3/9/2015
ms.audience: Developer
 
 
localization_priority: Normal
ms.assetid: ad5f75f9-47c3-4f51-a535-80cba4243683
description: "Learn about exporting and importing appointments, emails, contacts, tasks, and other mailbox items by using the EWS Managed API or EWS in Exchange."
---

# Exporting and importing items by using EWS in Exchange

Learn about exporting and importing appointments, emails, contacts, tasks, and other mailbox items by using the EWS Managed API or EWS in Exchange. 
  
Exchange is a gold mine of important information: email, contacts, tasks, and calendars are core to an organization's functions. EWS enables you to export and import core item types via three different approaches:
  
- Exchange item types. We recommend this approach for importing and exporting items to and from other systems and files.
    
- Item-level capability (EWS only). We recommend this option for exporting or copying from one Exchange server or mailbox and importing to another.
    
- MIME streams in the form of common standard file formats such as iCalendar and vCard. Because the property set is limited and MIME conversion is costly, we recommend the approach only for importing or exporting a small amount of data.
    
> [!IMPORTANT]
> EWS is not designed for mailbox backup and restore. To back up and restore databases, use the [backup and restore API](http://msdn.microsoft.com/library/329902d9-0ecb-4cfb-86dd-5ce863deff3f%28Office.15%29.aspx). See also [Backup, restore, and disaster recovery](http://technet.microsoft.com/en-us/library/dd876874%28v=exchg.150%29.aspx) on TechNet. 
  
**Table 1. Exporting and importing contact, email, and calendar items**

|**Task**|**EWS Managed API method**|**EWS operation**|**Notes**|
|:-----|:-----|:-----|:-----|
|Export a copy of a contact, email, task, or calendar item with a [specified property set](properties-and-extended-properties-in-ews-in-exchange.md).  <br/> |[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) <br/> [EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> [Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> [Task.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.task.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |We recommend this option if you're exporting mailbox items to another non-Exchange system or file (including vCard and iCal file types). Because you have control over the exported property set, and because performance is better for the Exchange server, this is generally the best option.  <br/> Depending on the properties set on a mailbox item, and whether your application is aware of all of the non-schematized property identifiers (extended properties) that might be set on an item, this option might not produce a full-fidelity copy.  <br/> These methods and operation provide the schematized set of properties for an item plus any requested extended properties. The **Bind** method or **GetItem** operation can only provide full-fidelity export of items if you know the extended properties that are set on an item. You can request all the known [extended properties](properties-and-extended-properties-in-ews-in-exchange.md) to enable full fidelity.  <br/> > [!TIP]> You can use the tracing feature in the EWS Managed API to get the XML representation of exported items.           For more information, see [Export an item into a custom format](how-to-export-items-by-using-ews-in-exchange.md#bk_exportcustom).  <br/> |
|Import a copy of a contact, email, task, or calendar item with a [specified property set](properties-and-extended-properties-in-ews-in-exchange.md).  <br/> |[Contact.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) <br/> [EmailMessage.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) <br/> [Appointment.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) <br/> [Task.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.task.save%28v=exchg.80%29.aspx) <br/> |[CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |We recommend this option for importing mailbox items into Exchange. You might have to set special properties on some item types in order to maintain the state of the imported item. Because some properties are only set by Exchange and not by clients, it's not always possible to have a full-fidelity import.  <br/> For example, you cannot import a meeting with attendees into a mailbox because Exchange sets the relationships between the organizer and attendees. This relationship can only be established by organizers sending and attendees receiving and responding to the meeting request.  <br/> **Appointment** objects in Exchange can have complex relationships and settings. Appointments that have attendees (meetings) have settings that tie together the meeting organizer and meeting attendees. These settings are not maintained when you export and import appointments. Programmatically reestablishing meeting organizer/attendee relationships directly on the appointments is not supported. An option you do have for reestablishing those relationships is to perform post-processing after an import, then have an organizer resend the meetings and have the attendees accept the meetings. You can use Exchange impersonation to make the calls for both the organizer and the attendees. You should change the UID property of the **Appointment** object before you import to avoid having meetings be incorrectly related to other meetings in a mailbox.  <br/> |
|Export a copy of a contact, email, task, or calendar item in full-fidelity.  <br/> |Not applicable  <br/> |[ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) <br/> |This is the best option for exporting mailbox items that you want to import back into an Exchange mailbox. You can also use this option to copy items between mailboxes. The **ExportItems** operation provides an opaque stream that represents the item that you can use to move information between mailboxes. You can use **ExportItems** with the [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) operation to make an index for finding the items in another system. You cannot change the export stream.  <br/> For more information, see [Export items with full fidelity](how-to-export-items-by-using-ews-in-exchange.md#bk_exportfullfidelity).  <br/> |
|Import a copy of a contact, email, task, or calendar item in full-fidelity.  <br/> |Not applicable  <br/> |[UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) <br/> |This is the only option for importing items that were exported by the **ExportItems** operation.  <br/> |
|Export a copy of a contact, email, or calendar item as a MIME stream for a common file type.  <br/> |[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) <br/> [EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> [Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |**GetItem** <br/> |You can use the [MimeContent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) property to get the MIME stream representation of an item.  <br/> This will provide a basic subset of all the properties on an item. As a best practice, only use the MIME stream for one-off operations. Do not rely on MIME for large and frequent importing/exporting of items, because Exchange performs content conversion for the MIME and this can affect performance.  <br/> The **Contact** MIME stream is a [vCard](http://www.faqs.org/rfcs/rfc2426.mdl) (.vcf) file. Depending on the properties set on a contact, this might not produce a full-fidelity copy. Note that you cannot import a contact by using the vCard MIME stream. To learn more, see [Export a contact into a vCard file](how-to-export-items-by-using-ews-in-exchange.md#bk_exportvcardmime).  <br/> The **EmailMessage** MIME stream is an .eml file. The .eml format is convenient because Outlook and other email clients can identify it. You can also use the MIME stream to create an .mht file, which is convenient because many browsers can use that file type. EWS doesn't provide a .msg file stream for exporting an email to a .msg file. Your options for exporting an .msg file are to either [construct an .MSG file](http://msdn.microsoft.com/en-us/library/cc463912%28v=EXCHG.80%29.aspx) from the results of an **EmailMessage.Bind** method or **GetItem** operation call, or use a third-party API that calls EWS and constructs the .msg file from the results. For more information, see [Export an email as an .eml file](how-to-export-items-by-using-ews-in-exchange.md#bk_exportemailmime).  <br/> The **Appointment** MIME stream is an iCal (.ics) file. The .ics format is convenient because Outlook and other email clients can identify it. This is not a viable option for exporting meetings because attendee information is not provided in the MIME stream. Attachments and other properties might not be included in the MIME stream. Consider constructing the iCal format from either the [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object or from the XML returned by the **GetItem** operation. This way, you can capture more of the Exchange properties with extended properties ("X-' properties) in the iCal file. You can also export an appointment in XML form. Call the **GetItem** operation and save the XML in your system. You can also use the [tracing functionality](how-to-trace-requests-and-responses-to-troubleshoot-ews-managed-api-applications.md) in the EWS Managed API to capture the XML to put in an XML database. For more information, see [Exporting an appointment as an iCal file](how-to-export-items-by-using-ews-in-exchange.md#bk_exporticalmime).  <br/> |
|Import a copy of an email or calendar item as a MIME stream for a common file type.  <br/> |[EmailMessage.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) <br/> [Appointment.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) <br/> |**CreateItem** <br/> |You can import an .eml or .ics file by using the **MimeContent** property on an **EmailMessage** or **Appointment** object. You will need to set the [PidTagMessageFlags (0x0E07)](http://msdn.microsoft.com/en-us/library/office/cc839733%28v=office.15%29.aspx) extended property if the email is not a draft.  <br/> You cannot use this approach to import meetings.  <br/> |
   
## Alternatives to exporting and importing items by using EWS
<a name="alternatives"> </a>

Other options are available for exporing and importing items to and from an Exchange mailbox. The following are some ideas to consider when you design your import and export strategy:
  
- Use PowerShell to call EWS and format the output into a .csv file.
    
- Use third-party libraries that implement MAPI to export and import items. Third-party libraries that convert EWS to .msg files are available too.
    
- Use the Exchange Management Shell and the [MailboxImportRequest](http://technet.microsoft.com/en-us/library/ff607310%28v=exchg.150%29.aspx) and [MailboxExportRequest](http://technet.microsoft.com/en-us/library/ff607299%28v=exchg.150%29.aspx) cmdlets to [fulfill mailbox import and export requests](http://technet.microsoft.com/en-us/library/ee633455%28v=exchg.150%29.aspx). 
    
- Use [Outlook's import options](http://office.microsoft.com/en-us/outlook-help/import-outlook-items-from-an-outlook-data-file-pst-HA102505743.aspx) to import and export items. 
    
## In this section
<a name="alternatives"> </a>

- [How to: Export items by using EWS in Exchange](how-to-export-items-by-using-ews-in-exchange.md)
    
- [How to: Import items by using EWS in Exchange](how-to-import-items-by-using-ews-in-exchange.md)
    
## Additional resources
<a name="bk_addresources"> </a>

- [Backup, Restore, and Disaster Recovery](http://technet.microsoft.com/en-us/library/dd876874%28v=exchg.150%29.aspx)
    
- [Journaling](http://technet.microsoft.com/en-us/library/aa998649%28v=exchg.150%29.aspx)
    
- [Internet Calendaring and Scheduling Core Object Specification (RFC 5545)](http://tools.ietf.org/html/rfc5545)
    
- [Mailbox synchronization and EWS in Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    

