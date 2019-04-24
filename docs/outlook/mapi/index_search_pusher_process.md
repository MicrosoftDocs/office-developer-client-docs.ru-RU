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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332209"
---
# <a name="indexsearchpusherprocess"></a><span data-ttu-id="ba7d5-103">INDEX_SEARCH_PUSHER_PROCESS</span><span class="sxs-lookup"><span data-stu-id="ba7d5-103">INDEX_SEARCH_PUSHER_PROCESS</span></span>

  
  
<span data-ttu-id="ba7d5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba7d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba7d5-105">Задает процесс, который отправляет уведомление обработчику протокола MAPI о том, что объект в этом хранилище готов к индексированию.</span><span class="sxs-lookup"><span data-stu-id="ba7d5-105">Specifies the process that is sending a notification to the MAPI Protocol Handler that an object in that store is ready for indexing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ba7d5-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="ba7d5-106">Quick info</span></span>

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a><span data-ttu-id="ba7d5-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="ba7d5-107">Members</span></span>

 <span data-ttu-id="ba7d5-108">*Двпид*</span><span class="sxs-lookup"><span data-stu-id="ba7d5-108">*dwPID*</span></span> 
  
>  <span data-ttu-id="ba7d5-109">Идентификатор процесса, который отправляет уведомление индексирования обработчику протокола MAPI.</span><span class="sxs-lookup"><span data-stu-id="ba7d5-109">Process ID for the process that is sending an indexing notification to the indexer of the MAPI Protocol Handler.</span></span> 
    

