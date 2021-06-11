---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 64e5cf31dffdc794a22bcbd6d503a2b688f9c733
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423351"
---
# <a name="index_search_pusher_process"></a>INDEX_SEARCH_PUSHER_PROCESS

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает процесс отправки уведомления обработнику протокола MAPI о том, что объект в этом магазине готов к индексации.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a>Элементы

 *dwPID* 
  
>  Процесс ID для процесса отправки уведомления об индексации в индексер обработщика протокола MAPI. 
    

