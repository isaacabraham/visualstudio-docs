---
title: "&#39;Catch&#39; cannot catch type &#39;&lt;typename&gt;&#39; because it is not &#39;System.Exception&#39; or a class that inherits from &#39;System.Exception&#39;"
ms.custom: na
ms.date: 10/02/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1d513d1d-38f5-4b4e-95bb-9f1209553803
caps.latest.revision: 7
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
# &#39;Catch&#39; cannot catch type &#39;&lt;typename&gt;&#39; because it is not &#39;System.Exception&#39; or a class that inherits from &#39;System.Exception&#39;
`Catch` can only intercept exceptions, and you have attempted to catch something that is not derived from an exception.  
  
 **Error ID:** BC30392  
  
### To correct this error  
  
1.  Remove the `Catch` statement, or change the target of the `Catch` to an actual exception.  
  
## See Also  
 [Try...Catch...Finally Statement](../Topic/Try...Catch...Finally%20Statement%20\(Visual%20Basic\).md)   
 [Structured Exception Handling Overview for Visual Basic](assetId:///bb81af80-a735-4873-9711-6151a48e418a)