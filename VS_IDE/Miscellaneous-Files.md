---
title: "Miscellaneous Files"
ms.custom: na
ms.date: 10/10/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5b96640b-8efe-48a4-8d0a-1ae3f9587e44
caps.latest.revision: 11
manager: ghogen
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
# Miscellaneous Files
You might want to use the Visual Studio editors to work independently on files from a project or from a solution. While you have a solution open, you can open and modify files without adding them to a solution or to a project. Files you want to work with independently from the containers are called miscellaneous files. Miscellaneous files are external to solutions and projects, are not included in builds, and cannot be included with a solution under source control.  
  
 Opening files independently from a container is useful for a variety of reasons. You might have a file that you want to view while developing a project-based solution but that is not integral to the solution's development. Common examples include development notes or instructions, database schema, and code clips. In addition, you might want to create a stand-alone file.  
  
 ![Solutions Projects](../VS_IDE/media/Projects_Solutions_Misc.gif "Projects_Solutions_Misc")  
  
 Solution Explorer can display a Miscellaneous Files folder for the files if the options for the folder are enabled. The options can be set from the [Documents, Environment, Options Dialog Box](../VS_IDE/Documents--Environment--Options-Dialog-Box.md). After you close a miscellaneous file, it is not associated with any particular solution or project unless an option is enabled for that as well.  
  
 The Miscellaneous Files folder represents the files as links. Although this folder is not part of a solution, when you open a solution, some or all of the miscellaneous files that were opened when the solution was last closed are re-opened, depending upon the settings for the folder.  
  
> [!NOTE]
>  Some of the files that do not appear in the Miscellaneous Files folder are files that you cannot modify within the IDE, such as .zip files and .doc files. The IDE will not track files that can only be modified through an external editor.  
  
## Commands Available in the IDE  
 The menus, toolbars, and the commands they contain change based on the format of the file you open. When you open a text file, for example, the Text Editor toolbar appears and its commands are available. If you then open an XML Schema file, the XML Schema toolbar appears. While editing your XML Schema, the Text Editor toolbar's commands (or the toolbar itself) are unavailable. The XML Schema is the active window and as such, has current selection context. When you switch between a project file and a miscellaneous file, all project-related commands disappear and only those that are directly related to the miscellaneous file appear.  
  
## Folder Display Options  
 You can set display options for the Miscellaneous Folder so that the folder appears even though you have not opened any Miscellaneous Files. The solution file does not permanently manage a list of miscellaneous files. It uses an optional feature that allows it to remember a per-user most recently used (MRU) list of files.  
  
## See Also  
 [Solutions and Projects](../VS_IDE/Solutions-and-Projects-in-Visual-Studio.md)   
 [Documents, Environment, Options Dialog Box](../VS_IDE/Documents--Environment--Options-Dialog-Box.md)