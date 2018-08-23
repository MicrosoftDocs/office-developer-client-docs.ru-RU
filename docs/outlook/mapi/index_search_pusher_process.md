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
ms.openlocfilehash: 9495caecd514656f6fd62fb5db6cd8ac2faf4b50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581743"
---
# <a name="indexsearchpusherprocess"></a>INDEX_SEARCH_PUSHER_PROCESS

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает процесс, который отправляет уведомление обработчик протокола MAPI, что объект в этого хранилища готова для индексации.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a>Members

 *dwPID* 
  
>  Идентификатор процесса для процесса, который отправляет уведомление об индексации индексатор обработчик протокола MAPI. 
    

