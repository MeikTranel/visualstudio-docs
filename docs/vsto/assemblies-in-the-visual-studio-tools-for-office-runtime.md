---
title: "Assemblies in the Visual Studio Tools for Office Runtime | Microsoft Docs"
ms.custom: ""
ms.date: "02/02/2017"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "office-development"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
helpviewer_keywords: 
  - "Visual Studio Tools for Office runtime, assemblies"
ms.assetid: d2b7f8f4-0f41-4943-bca5-48c520748b7e
caps.latest.revision: 29
author: "kempb"
ms.author: "kempb"
manager: "ghogen"
---
# Assemblies in the Visual Studio Tools for Office Runtime
  When you create an Office project, Visual Studio automatically adds references to the [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] assemblies that are used for the project type and the target .NET Framework of the project. There are different assemblies in the Office extensions for the .NET Framework 3.5, [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)], and [!INCLUDE[net_v45](../vsto/includes/net-v45-md.md)]. For more information about the Office extensions, see [Visual Studio Tools for Office Runtime Overview](../vsto/visual-studio-tools-for-office-runtime-overview.md).  
  
## Assemblies in the Office Extensions for the .NET Framework 4 and the [!INCLUDE[net_v45](../vsto/includes/net-v45-md.md)]  
 The following table lists the assemblies that are included in Office extensions for the [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] and the [!INCLUDE[net_v45](../vsto/includes/net-v45-md.md)]. For documentation about the namespaces and types in these assemblies, see [Managed Reference &#40;Office Development in Visual Studio&#41;](../vsto/managed-reference-office-development-in-visual-studio.md).  
  
|Assembly name|Description|  
|-------------------|-----------------|  
|Microsoft.Office.Tools.Common.dll|Provides the following types:<br /><br /> -   Types for creating Ribbon customizations and smart tags. **Note:**      Smart tags are deprecated in [!INCLUDE[Excel_14_short](../vsto/includes/excel-14-short-md.md)] and [!INCLUDE[Word_14_short](../vsto/includes/word-14-short-md.md)].<br />-   Types for creating actions panes in document-level customizations and custom task panes in VSTO Add-Ins.|  
|Microsoft.Office.Tools.Excel.dll|Provides interfaces that represent host items and host controls for Excel projects, and supporting types. For more information, see [Automating Excel by Using Extended Objects](../vsto/automating-excel-by-using-extended-objects.md).|  
|Microsoft.Office.Tools.Outlook.dll|Provides types that you can use to create custom form regions in Outlook VSTO Add-ins.|  
|Microsoft.Office.Tools.Word.dll|Provides interfaces that represent host items and host controls for Word projects, and supporting types. For more information, see [Automating Word by Using Extended Objects](../vsto/automating-word-by-using-extended-objects.md).|  
|Microsoft.Office.Tools.v4.0.Framework.dll|Provides the following types:<br /><br /> -   Exceptions that can be thrown by the Visual Studio Tools for Office runtime.<br />-   Attributes you can use when creating Outlook form regions.|  
|Microsoft.Office.Tools.dll|Provides types that are part of the Visual Studio Tools for Office runtime infrastructure, and are not intended to be used directly from your code.|  
|Microsoft.VisualStudio.Tools.Applications.Runtime.dll|Provides the following types:<br /><br /> -   The <xref:Microsoft.VisualStudio.Tools.Applications.Runtime.CachedAttribute> attribute and <xref:Microsoft.VisualStudio.Tools.Applications.Runtime.ICachedType> interface, which you can use to cache data objects in a document-level customization. For more information, see [Caching Data](../vsto/caching-data.md).<br />-   The <xref:Microsoft.VisualStudio.Tools.Applications.Deployment.IAddInPostDeploymentAction> interface, which you can implement to run additional installation steps as the final step of the ClickOnce installer for an Office solution. For more information, see [Deploying an Office Solution by Using ClickOnce](../vsto/deploying-an-office-solution-by-using-clickonce.md).<br />-   Exceptions that can be thrown by the Visual Studio Tools for Office runtime.<br />-   Other types that are part of the Visual Studio Tools for Office runtime infrastructure, and are not intended to be used directly from your code.|  
|Microsoft.VisualStudio.Tools.Applications.ServerDocument.dll|Provides the following types:<br /><br /> -   The <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> class, which you can use to attach customization assemblies to documents and to access the cached data in documents. For more information, see [Managing Documents on a Server by Using the ServerDocument Class](../vsto/managing-documents-on-a-server-by-using-the-serverdocument-class.md).<br />-   Several classes that represent the hierarchy of cached data in a document-level customization. For more information, see [Accessing Data in Documents on the Server](../vsto/accessing-data-in-documents-on-the-server.md).|  
  
 Projects that target the [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] or the [!INCLUDE[net_v45](../vsto/includes/net-v45-md.md)] also reference the following assemblies. These assemblies are not part of the [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] redistributable. Instead, they are dependent assemblies that must be deployed with your solution. By default, they are copied to the build output folder for your project (the **Copy Local** property for these assemblies are set to **True**). If you deploy your project by using ClickOnce, these assemblies are included in the generated package.  
  
|Assembly name|Description|  
|-------------------|-----------------|  
|Microsoft.Office.Tools.Common.v4.0.Utilities.dll|Provides the base classes for the generated `ThisAddIn` class in VSTO Add-In projects and the generated Ribbon class in all projects.|  
|Microsoft.Office.Tools.Excel.v4.0.Utilities.dll|Provides the following types:<br /><br /> -   Base classes for the generated `ThisWorkbook` and `Sheet` classes in document-level projects for Excel.<br />-   Windows Forms controls that you can use on worksheets in Excel projects.|  
|Microsoft.Office.Tools.Outlook.v4.0.Utilities.dll|Provides base classes for the generated `ThisAddIn` and form region classes in Outlook projects.|  
|Microsoft.Office.Tools.Word.v4.0.Utilities.dll|Provides the following types:<br /><br /> -   Base classes for the generated `ThisDocument` class in document-level projects for Word.<br />-   Windows Forms controls that you can use on documents in Word projects.|  
  
## Assemblies in the Office Extensions for the .NET Framework 3.5  
 The following table lists the assemblies that are included in the Office extensions for the .NET Framework 3.5. For documentation about the namespaces and classes in these assemblies, see the following reference section in the Visual Studio 2008 documentation: [http://go.microsoft.com/fwlink/?LinkId=160658](http://go.microsoft.com/fwlink/?LinkId=160658).  
  
|Assembly name|Description|  
|-------------------|-----------------|  
|Microsoft.Office.Tools.Common.v9.0.dll|Provides the following types:<br /><br /> -   The Microsoft.Office.Tools.AddIn base class for VSTO Add-Ins.<br />-   Classes for creating Ribbon customizations and smart tags. **Note:**      Smart tags are deprecated in [!INCLUDE[Excel_14_short](../vsto/includes/excel-14-short-md.md)] and [!INCLUDE[Word_14_short](../vsto/includes/word-14-short-md.md)].<br />-   Classes for creating actions panes in document-level customizations and custom task panes in VSTO Add-Ins.|  
|Microsoft.Office.Tools.Excel.v9.0.dll|Provides host items and host controls for Excel solutions. For more information, see [Automating Excel by Using Extended Objects](../vsto/automating-excel-by-using-extended-objects.md).|  
|Microsoft.Office.Tools.Outlook.v9.0.dll|Provides classes that you can use to create custom form regions in Outlook VSTO Add-ins.|  
|Microsoft.Office.Tools.Word.v9.0.dll|Provides host items and host controls for Word solutions. For more information, see [Automating Word by Using Extended Objects](../vsto/automating-word-by-using-extended-objects.md).|  
|Microsoft.Office.Tools.v9.0.dll|Provides the following types:<br /><br /> -   The Microsoft.VisualStudio.Tools.Office.RemoteBindableComponent class, which provides the data binding capabilities for host controls in document-level customizations.<br />-   Other types that are part of the Visual Studio Tools for Office runtime infrastructure, and are not intended to be used directly from your code.|  
|Microsoft.VisualStudio.Tools.Applications.Runtime.v9.0.dll|Provides the following types:<br /><br /> -   The Microsoft.VisualStudio.Tools.Applications.Runtime.CachedAttribute attribute and Microsoft.VisualStudio.Tools.Applications.Runtime.ICachedType interface, which you can use to cache data objects in a document-level customization. For more information, see [Caching Data](../vsto/caching-data.md).<br />-   Exceptions that can be thrown by the Visual Studio Tools for Office runtime.<br />-   Other types that are part of the Visual Studio Tools for Office runtime infrastructure, and are not intended to be used directly from your code.|  
|Microsoft.VisualStudio.Tools.Applications.Runtime.v10.0.dll|Provides the Microsoft.VisualStudio.Tools.Applications.Deployment.IAddInPostDeploymentAction interface, which you can implement to run additional installation steps as the final step of the ClickOnce installer for an Office solution. For more information, see [Advanced Office Solution Deployment](http://msdn.microsoft.com/en-us/9147b6f6-849f-4cb1-b2c5-e22658d74b02).|  
|Microsoft.VisualStudio.Tools.Applications.ServerDocument.v10.0.dll|Provides the following types:<br /><br /> -   The Microsoft.VisualStudio.Tools.Applications.ServerDocument class, which you can use to programmatically attach customization assemblies to documents and to access the cached data in documents. For more information, see [Managing Documents on a Server by Using the ServerDocument Class](../vsto/managing-documents-on-a-server-by-using-the-serverdocument-class.md).<br />-   Several classes that represent the hierarchy of cached data in a document-level customization. For more information, see [Accessing Data in Documents on the Server](../vsto/accessing-data-in-documents-on-the-server.md).|  
|Microsoft.VisualStudio.Tools.Office.Runtime.v10.0.dll|Provides the following types:<br /><br /> -   The Microsoft.VisualStudio.Tools.Office.Runtime.Security.AddInSecurityEntry and Microsoft.VisualStudio.Tools.Office.Runtime.Security.UserInclusionList classes, which you can use to create user inclusion list entries to grant trust to Office solutions that target the .NET Framework 3.5.<br />-   Other types that are part of the Visual Studio Tools for Office runtime infrastructure, and are not intended to be used directly from your code.|  
  
## See Also  
 [Visual Studio Tools for Office Runtime Overview](../vsto/visual-studio-tools-for-office-runtime-overview.md)   
 [Visual Studio Tools for Office Runtime Installation Scenarios](../vsto/visual-studio-tools-for-office-runtime-installation-scenarios.md)  
  
  