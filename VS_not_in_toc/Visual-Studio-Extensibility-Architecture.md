---
title: "Visual Studio Extensibility Architecture"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 280fdb55-3e70-41fd-8da0-4039bf5d4894
caps.latest.revision: 17
manager: douge
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - ru-ru
  - zh-cn
  - zh-tw
translation.priority.mt: 
  - cs-cz
  - pl-pl
  - pt-br
  - tr-tr
---
# Visual Studio Extensibility Architecture
The Visual Studio integrated development environment (IDE) is a framework for hosting VSPackages and for making it easier to exchange shared services. An example of this is the way the IDE implements the user interface (UI). The IDE provides the container window and the default toolbars and menus. It also provides a rich COM infrastructure that makes the UI programmable. The complete command handling and routing scheme gives users an open framework that offers easy access to both existing and installed command sets.  
  
## Extensibility Architecture  
 The following illustration shows the Visual Studio extensibility architecture. Note that the concept of software application is absent. Instead, the IDE hosts software components, called VSPackages, that provide application functionality. This functionality, in turn, is shared across the IDE as services. VSPackages offer services that they and other VSPackages use. The standard IDE also offers a broad range of services, such as <xref:Microsoft.VisualStudio.Shell.Interop.SVsUIShell?qualifyHint=False>, which provide access to the IDE windowing functionality.  
  
 ![Environment Architecture graphic](../VS_not_in_toc/media/environment.gif "environment")  
Generalized view of the Visual Studio architecture  
  
 Notice that the relationship between VSPackages and services is bidirectional. Although VSPackages use services offered by others, they also can offer services of their own by using the <xref:Microsoft.VisualStudio.Shell.Interop.IProfferService?qualifyHint=False> interface. This service-based architecture grew out of the Microsoft ActiveX Designer implementation, in which a service is a group of related interfaces that perform a task. From a strict COM viewpoint, all the interfaces of a particular service must be implemented in a single COM class.  
  
 The standard IDE offers important services, such as <xref:Microsoft.VisualStudio.Shell.Interop.SVsShell?qualifyHint=False>, <xref:Microsoft.VisualStudio.Shell.Interop.SVsUIShell?qualifyHint=False>, and <xref:Microsoft.VisualStudio.Shell.Interop.SVsSolution?qualifyHint=False>, which are used by VSPackages. The following table lists and describes some of these services. For more information, see [Using and Providing Services](../Topic/Using%20and%20Providing%20Services.md).  
  
|IDE service|Description|  
|-----------------|-----------------|  
|<xref:Microsoft.VisualStudio.Shell.Interop.SVsShell?qualifyHint=False>|Provides access to IDE services dealing with basic functionality, VSPackages, and the registry.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.SVsUIShell?qualifyHint=False>|Provides basic windowing and UI-related functionality in the IDE, such as the ability to create tools and document windows.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.SVsSolution?qualifyHint=False>|Provides basic solution-related functionality, such as the ability to enumerate projects, create new projects, and monitor project changes.|  
  
 Because of their tight integration through the interaction of shared services, the Visual Studio IDE and VSPackages are closely interdependent. However, despite their close interaction they have different responsibilities.  
  
 The Visual Studio IDE is responsible for the following tasks:  
  
-   Providing critical services for use by external VSPackages.  
  
-   Providing a programmable interface, which enables participation with standard UI elements.  
  
-   Creating instances of VSPackages as required by user actions or by other VSPackages requesting services.  
  
-   Providing services that make it possible for communication and coordination between VSPackages.  
  
-   Managing solutions and their required files.  
  
-   Providing window management.  
  
-   Providing command routing and command bars, such as menus, toolbars, and context menus.  
  
-   Coordinating selection, context, and currency.  
  
 VSPackages are responsible for the following tasks:  
  
-   Performing certain initialization and termination routines.  
  
-   Writing information to the registry, which the IDE uses to load the appropriate VSPackages at the appropriate times.  
  
-   Offering the services that are required for communicating with other VSPackages.  
  
-   Providing implementations for new project types, editors, and designers.  
  
-   Providing extensions for built-in UI elements, such as task items, toolbox items, and the Options dialog box.  
  
## See Also  
 [Visual Studio Shell](../Topic/Visual%20Studio%20Shell.md)   
 [VSPackages](../Topic/VSPackages.md)   
 [Using and Providing Services](../Topic/Using%20and%20Providing%20Services.md)   
 [How to: Get a Service](../Topic/How%20to:%20Get%20a%20Service.md)