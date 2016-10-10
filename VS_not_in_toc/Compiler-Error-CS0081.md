---
title: "Compiler Error CS0081"
ms.custom: na
ms.date: 10/01/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a5649abc-89ea-4f64-8c3c-eb36df926561
caps.latest.revision: 9
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
# Compiler Error CS0081
Type parameter declaration must be an identifier not a type  
  
 When you declare a generic method or type, specify the type parameter as an identifier, for example "T" or "inputType". When client code calls the method, it supplies the type, which replaces each occurrence of the identifier in the method or class body. For more information, see [Generic Type Parameters](../Topic/Generic%20Type%20Parameters%20\(C%23%20Programming%20Guide\).md).  
  
```  
// CS0081.cs  
class MyClass  
{  
   public void F<int>() {}   // CS0081  
   public void F<T>(T input) {}   // OK  
  
   public static void Main()  
   {  
      MyClass a = new MyClass();  
      a.F<int>(2);  
      a.F<double>(.05);  
   }  
}  
```  
  
## See Also  
 [Generics](../Topic/Generics%20\(C%23%20Programming%20Guide\).md)