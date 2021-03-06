---
title: "Migrating to Exchange Online and Exchange 2013 technologies"

manager: sethgros
ms.date: 3/9/2015
ms.audience: Developer

localization_priority: Normal
ms.assetid: 946a722f-0892-4a59-9e58-a291bfb6834a

description: "If you're migrating from an earlier version of Exchange, use the information in this article to find out which development technologies are supported in current product versions, and which technology to migrate to."
---

# Migrating to Exchange Online and Exchange 2013 technologies

If you're migrating from an earlier version of Exchange, use the information in this article to find out which development technologies are supported in current product versions, and which technology to migrate to.
  
## Determine whether your development technology is available in current versions of Exchange

Use the following table to determine whether a technology is supported in Exchange Online or Exchange 2013. If the technology is not supported, see [Choose a development technology to migrate to](#bk_choose).
  
**Exchange development technologies and product versions**

|**Technology**|**Office 365 and Exchange Online**|**Exchange 2013**|**Exchange 2010**|**Exchange 2007**|
|:-----|:-----|:-----|:-----|:-----|
|[Office 365 APIs platform overview](http://msdn.microsoft.com/library/16fbf0c0-5470-466b-aab8-a0c9074c94e2%28Office.15%29.aspx) <br/> |X  <br/> ||||
|[EWS Managed API](http://msdn.microsoft.com/library/53553207-ff98-4fdb-8716-4ae02fee83bf%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange Web Services (EWS)](http://msdn.microsoft.com/library/53553207-ff98-4fdb-8716-4ae02fee83bf%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Mail apps for Outlook](http://msdn.microsoft.com/library/821c8eb9-bb58-42e8-9a3a-61ca635cba59%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |||
|[Outlook Object Model (OOM)](http://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange Management Shell](http://msdn.microsoft.com/library/8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Backup and restore](http://msdn.microsoft.com/library/329902d9-0ecb-4cfb-86dd-5ce863deff3f%28Office.15%29.aspx) <br/> ||X  <br/> |X  <br/> |X  <br/> |
|[Transport agents](http://msdn.microsoft.com/library/36d63aa6-1b72-4670-b5c3-da685f3017cb%28Office.15%29.aspx) <br/> ||X  <br/> |X  <br/> |X  <br/> |
|Active Directory Services Interface (ADSI)  <br/> ||||X  <br/> |
|Collaborative Data Objects for Exchange (CDOEX)  <br/> ||||X  <br/> |
|Collaborative Data Objects for Windows 2000 (CDOSYS)  <br/> ||||X  <br/> |
|Exchange OLE DB Provider (EXOLEDB)  <br/> ||||X  <br/> |
|Exchange Store Event Sinks  <br/> ||||X  <br/> |
|Incremental Change Synchronization (ICS)  <br/> ||||X  <br/> |
|Lightweight Directory Access Protocol (LDAP)  <br/> ||||X  <br/> |
|[Messaging API (MAPI)](http://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Outlook Web App customization  <br/> |||X  <br/> ||
|Web Distributed Authoring and Versioning (WebDAV)  <br/> ||||X  <br/> |
   
## Choose a development technology to migrate to
<a name="bk_choose"> </a>

If the technology your application uses is not supported or deemphasized in Exchange Online or Exchange 2013, use the following table to decide which technology to migrate to.
  
**Recommended technology migration paths**

|**Technology**|**Supported in Office 365, Exchange Online, and Exchange 2013?**|**Migrate to**|**More info**|
|:-----|:-----|:-----|:-----|
|ADSI  <br/> |Yes, but deemphasized  <br/> |[Exchange Management Shell](http://msdn.microsoft.com/library/8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0%28Office.15%29.aspx) <br/> |None.  <br/> |
|CDOEX  <br/> |No  <br/> |[EWS Managed API or EWS](http://msdn.microsoft.com/library/53553207-ff98-4fdb-8716-4ae02fee83bf%28Office.15%29.aspx) <br/> |The EWS Managed API and EWS can access the same Exchange store that CDOEX provides. Unlike client applications built by using CDOEX, you can run EWS applications on a local or remote computer.  <br/> |
|CDOEXM  <br/> |No  <br/> |[Exchange Management Shell](http://msdn.microsoft.com/library/8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0%28Office.15%29.aspx) <br/> |Exchange Management Shell commands control Exchange servers, storage groups, databases, and users more simply than the corresponding CDOEXM APIs. Plus, you can easily migrate your CDOEXM applications to Exchange Management Shell commands.  <br/> |
|CDOSYS  <br/> |No  <br/> |[Transport agents](http://msdn.microsoft.com/library/36d63aa6-1b72-4670-b5c3-da685f3017cb%28Office.15%29.aspx) <br/> |Use transport agents for notification-based applications that work with versions of Exchange starting with Exchange 2010.  <br/> CDOSYS is included in current versions of Windows. The functionality in CDOSYS is available in the .NET Framework.  <br/> |
|CDOWF  <br/> |No  <br/> |[Windows Workflow Foundation (WWF)](http://msdn.microsoft.com/en-us/library/vstudio/ms735967%28v=vs.90%29.aspx) or [BizTalk Server](http://msdn.microsoft.com/library/abcc1da8-9ccc-41b8-b614-3a9bd8f2d0bd%28Office.15%29.aspx) <br/> |You can use WWF to create advanced workflow applications that work with Exchange 2007. For more complicated workflow systems, use BizTalk Server.  <br/> |
|ExOLEDB  <br/> |No  <br/> |[EWS Managed API or EWS](http://msdn.microsoft.com/library/53553207-ff98-4fdb-8716-4ae02fee83bf%28Office.15%29.aspx) <br/> |The EWS Managed API and EWS provide the same access to the Exchange store that ExOLEDB provides. Unlike client applications built by using ExOLEDB, You can run EWS applications on a local or remote computer.  <br/> |
|ICS  <br/> |Yes, but deemphasized  <br/> |[EWS Managed API or EWS](http://msdn.microsoft.com/library/76136f28-0dad-4ecc-9dd7-a45a1861e4b0%28Office.15%29.aspx) <br/> |You can use the EWS Managed API or EWS to [subscribe to notifications](http://msdn.microsoft.com/library/76136f28-0dad-4ecc-9dd7-a45a1861e4b0%28Office.15%29.aspx) and [synchronize mailbox data](http://msdn.microsoft.com/library/decf1eee-9743-44f3-9333-b3a01af3683e%28Office.15%29.aspx).  <br/> |
|LDAP  <br/> |Yes, but deemphasized  <br/> |[Exchange Management Shell](http://msdn.microsoft.com/library/8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0%28Office.15%29.aspx) <br/> |None.  <br/> |
|MAPI  <br/> |Yes, but deemphasized  <br/> |[Office 365 APIs platform overview](http://msdn.microsoft.com/library/16fbf0c0-5470-466b-aab8-a0c9074c94e2%28Office.15%29.aspx), [EWS Managed API, EWS](http://msdn.microsoft.com/library/53553207-ff98-4fdb-8716-4ae02fee83bf%28Office.15%29.aspx) <br/> |Although MAPI is currently a supported development technology, you will eventually have to redesign your MAPI applications to use a newer technology.  <br/> If your MAPI application is performing simple read, write, and update operations on mail, calendar, or contact objects, and targets Office 365, you can use the [Office 365 REST APIs Preview for mail, calendars, and contacts](http://msdn.microsoft.com/library/3b2e71a6-5fa5-4008-b243-d3a6e9173b3d%28Office.15%29.aspx). If you are targeting Exchange on-premises and you need to access all the properties that MAPI can access, you use the EWS Managed API or EWS and either [schematized properties or extended properties](http://msdn.microsoft.com/library/68623048-060e-4602-b3fa-62617a94cf72%28Office.15%29.aspx).  <br/> > [!NOTE]> The [ExtendedPropertyDefinition](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) class provides access to MAPI from the EWS Managed API, and the [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element provides access to MAPI properties from EWS.           |
|Outlook Web App customization  <br/> |No  <br/> |[Mail apps](http://msdn.microsoft.com/library/821c8eb9-bb58-42e8-9a3a-61ca635cba59%28Office.15%29.aspx) <br/> |None.  <br/> |
|Store event sinks  <br/> |No  <br/> |[EWS Managed API or EWS](http://msdn.microsoft.com/library/53553207-ff98-4fdb-8716-4ae02fee83bf%28Office.15%29.aspx) <br/> |You can use the EWS Managed API or EWS to [subscribe to notifications](http://msdn.microsoft.com/library/76136f28-0dad-4ecc-9dd7-a45a1861e4b0%28Office.15%29.aspx) and [synchronize mailbox data](http://msdn.microsoft.com/library/decf1eee-9743-44f3-9333-b3a01af3683e%28Office.15%29.aspx). The notifications in EWS provide the same access to the Exchange store that store event sinks provide. You can use Visual Studio tools to streamline the development of store event-aware client applications that use EWS.  <br/> |
|Streaming backup and restore  <br/> |No  <br/> |[Volume Shadow Copy Service (VSS) writer](http://msdn.microsoft.com/library/329902d9-0ecb-4cfb-86dd-5ce863deff3f%28Office.15%29.aspx) <br/> |None.  <br/> |
|WebDAV  <br/> |No  <br/> |[Office 365 APIs platform overview](http://msdn.microsoft.com/library/16fbf0c0-5470-466b-aab8-a0c9074c94e2%28Office.15%29.aspx), [EWS Managed API, or EWS](http://msdn.microsoft.com/library/53553207-ff98-4fdb-8716-4ae02fee83bf%28Office.15%29.aspx) <br/> |If your WebDAV application is performing simple read, write, and update operations on mail, calendar, or contact objects, and you will be targeting Office 365, use the [Office 365 REST APIs Preview for mail, calendars, and contacts](http://msdn.microsoft.com/library/3b2e71a6-5fa5-4008-b243-d3a6e9173b3d%28Office.15%29.aspx). Otherwise, if you are targeting Exchange on-premises and you need access to the same properties in the Exchange store that WebDAV provides, use the EWS Managed API or EWS.  <br/> |
|WebDAV notifications  <br/> |No  <br/> |[EWS Managed API or EWS](http://msdn.microsoft.com/library/53553207-ff98-4fdb-8716-4ae02fee83bf%28Office.15%29.aspx) <br/> |You can use the EWS Managed API or EWS to [subscribe to notifications](http://msdn.microsoft.com/library/76136f28-0dad-4ecc-9dd7-a45a1861e4b0%28Office.15%29.aspx).  <br/> |
|Web forms  <br/> |No  <br/> |[ASP.NET](http://www.asp.net/web-forms) <br/> |Switch to ASP.NET and update applications to access mailbox and server information by using EWS.  <br/> |
|WMI providers  <br/> |No  <br/> |[Exchange Management Shell](http://msdn.microsoft.com/library/8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0%28Office.15%29.aspx) <br/> |None.  <br/> |
   
## Additional resources
<a name="bk_addresources"> </a>

- [Office 365 APIs platform overview](http://msdn.microsoft.com/library/16fbf0c0-5470-466b-aab8-a0c9074c94e2%28Office.15%29.aspx)
    
- [Explore the EWS Managed API, EWS, and web services in Exchange](http://msdn.microsoft.com/library/53553207-ff98-4fdb-8716-4ae02fee83bf%28Office.15%29.aspx)
    
- [Exchange Management Shell](http://msdn.microsoft.com/library/8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0%28Office.15%29.aspx)
    
- [Transport agents in Exchange 2013](http://msdn.microsoft.com/library/36d63aa6-1b72-4670-b5c3-da685f3017cb%28Office.15%29.aspx)
    
- [Backup and restore for Exchange 2013](http://msdn.microsoft.com/library/329902d9-0ecb-4cfb-86dd-5ce863deff3f%28Office.15%29.aspx)
    
- [Selecting an API or technology for developing solutions for Outlook](http://msdn.microsoft.com/library/01a46083-03d0-4333-920c-01a9f17f68cb%28Office.15%29.aspx)
    

