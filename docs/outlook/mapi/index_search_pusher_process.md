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
ms.openlocfilehash: ada6d4127d503aae0b068d40d2bb48cb6b833ea0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809436"
---
# <a name="indexsearchpusherprocess"></a>INDEX_SEARCH_PUSHER_PROCESS

  
  
**Относится к**: Outlook 
  
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
    

