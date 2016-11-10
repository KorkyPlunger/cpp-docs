---
title: "Updating a Column When Another Table Contains a Reference to the Row"
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
  - "rowsets, column updates"
ms.assetid: abb5db69-055d-431f-b12d-ad2940a661ba
caps.latest.revision: 7
ms.author: "mblome"
manager: "ghogen"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Updating a Column When Another Table Contains a Reference to the Row
Some providers can detect which columns in the row change, but many providers cannot. As a result, updating a column can result in an error when there is a reference to the row you are attempting to update. To solve this problem, create a separate accessor containing only the columns you want to change. Pass the number of that accessor to `SetData`.  
  
## See Also  
 [Using Accessors](../data/using-accessors.md)