---
title: "ResourcesGenerator Task | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: msbuild
ms.topic: "reference"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
  - "jsharp"
helpviewer_keywords: 
  - "embedding resources into a .resources file [WPF MSBuild]"
  - "ResourcesGenerator task [WPF MSBuild]"
  - "ResourcesGenerator task [WPF MSBuild], parameters"
ms.assetid: e782bbac-9ee6-472b-8171-3ee008c77b4e
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload: 
  - "multiple"
---
# ResourcesGenerator task
The <xref:Microsoft.Build.Tasks.Windows.ResourcesGenerator> task embeds one or more resources (*.jpg*, *.ico*, *.bmp*, [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] in binary format, and other extension types) into a *.resources* file.  
  
## Task parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`OutputPath`|Required **String** parameter.<br /><br /> Specifies the path of the output directory. If the path isn't an absolute path, it's treated as a path that is relative to the root project directory.|  
|`OutputResourcesFile`|Required **ITaskItem[]** output parameter.<br /><br /> Specifies the path and name of the generated *.resources* file. If the path isn't an absolute path, the *.resources* file is generated relative to the root project directory.|  
|`ResourcesFiles`|Required **ITaskItem[]** parameter.<br /><br /> Specifies one or more resources to embed in the generated *.resources* file.|  
  
## Example  
 The following example generates a *.resources* file with a single *.bmp* resource. The *.bmp* resource is generated to a directory that is relative to the project root directory.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  <UsingTask   
    TaskName="Microsoft.Build.Tasks.Windows.ResourcesGenerator"   
    AssemblyFile="C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\PresentationBuildTasks.dll" />  
  <Target Name="ResourcesGeneratorTask">  
    <ResourcesGenerator  
      ResourceFiles="Resource1.bmp"  
      OutputPath="myresources"  
      OutputResourcesFile="myresources\my.resources" />  
  </Target>  
</Project>  
```  
  
## See also  
 [WPF MSBuild reference](../msbuild/wpf-msbuild-reference.md)   
 [Task reference](../msbuild/wpf-msbuild-task-reference.md)   
 [MSBuild reference](../msbuild/msbuild-reference.md)   
 [Task reference](../msbuild/msbuild-task-reference.md)   
 [Build a WPF application (WPF)](/dotnet/framework/wpf/app-development/building-a-wpf-application-wpf)