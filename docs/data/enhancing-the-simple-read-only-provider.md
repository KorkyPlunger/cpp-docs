---
title: "Enhancing the Simple Read-Only Provider"
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
  - "read-only poviders [C++]"
  - "IRowsetLocate class"
  - "IRowsetLocate class, adding to OLE DB template providers"
  - "simple read-only poviders [C++]"
ms.assetid: cba0e09f-44c1-41c1-9456-332aa13dc158
caps.latest.revision: 8
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
# Enhancing the Simple Read-Only Provider
This section shows how to enhance the [simple read-only provider](../data/implementing-the-simple-read-only-provider.md) created in the previous section. `IRowsetLocateImpl` creates an implementation for the `IRowsetLocate` interface and adds bookmark support for you.  
  
 When you have a working provider, you might want to enhance it to make the provider update, handle transactions, or enhance the performance of the row-fetching algorithm. Most provider enhancements involve adding an interface to an existing COM object.  
  
 The example in the following topics enhances the row-fetching mechanism by adding the `IRowsetLocate` interface to `CAgentRowset`. The topics show you how to:  
  
-   [Make RMyProviderRowset inherit from IRowsetLocate](../data/modifying-the-inheritance-of-rmyproviderrowset.md).  
  
-   [Dynamically determine the columns returned to the consumer](../data/dynamically-determining-columns-returned-to-the-consumer.md).  
  
## See Also  
 [Creating a Simple Read-Only Provider](../data/creating-a-simple-read-only-provider.md)