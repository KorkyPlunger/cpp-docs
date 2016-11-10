---
title: "Developing Your Own Helper Function"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "helper functions"
ms.assetid: a845429d-68b1-4e14-aa88-f3f5343bd490
caps.latest.revision: 7
ms.author: "corob"
manager: "ghogen"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Developing Your Own Helper Function
You may want to provide your own version of the routine to do specific processing based on the names of the DLL or imports. There are two methods of doing this: coding your own, possibly based on the supplied code, or merely hooking the supplied version using the notification hooks detailed previously.  
  
 Code Your Own  
 This is fairly simple since you can essentially use the supplied code as a guideline for the new one. Of course, it must adhere to the calling conventions and if it returns to the linker-generated thunks, it must return a proper function pointer. Once in your code, you can do pretty much whatever you want in order to satisfy the call or get out of the call.  
  
 Use the Start Processing Notification Hook  
 It will probably be easiest to simply provide a new pointer to a user-supplied notification hook function that receives the same values as the default helper on the notification dliStartProcessing. At that point, the hook function can essentially become the new helper function, as a successful return to the default helper will bypass all further processing in the default helper.  
  
## See Also  
 [Linker Support for Delay-Loaded DLLs](../buildref/linker-support-for-delay-loaded-dlls.md)