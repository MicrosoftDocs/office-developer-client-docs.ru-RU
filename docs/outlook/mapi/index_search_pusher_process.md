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
# <a name="indexsearchpusherprocess"></a><span data-ttu-id="631ea-103">INDEX_SEARCH_PUSHER_PROCESS</span><span class="sxs-lookup"><span data-stu-id="631ea-103">INDEX_SEARCH_PUSHER_PROCESS</span></span>

  
  
<span data-ttu-id="631ea-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="631ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="631ea-105">Указывает процесс, который отправляет уведомление обработчик протокола MAPI, что объект в этого хранилища готова для индексации.</span><span class="sxs-lookup"><span data-stu-id="631ea-105">Specifies the process that is sending a notification to the MAPI Protocol Handler that an object in that store is ready for indexing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="631ea-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="631ea-106">Quick info</span></span>

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a><span data-ttu-id="631ea-107">Members</span><span class="sxs-lookup"><span data-stu-id="631ea-107">Members</span></span>

 <span data-ttu-id="631ea-108">*dwPID*</span><span class="sxs-lookup"><span data-stu-id="631ea-108">*dwPID*</span></span> 
  
>  <span data-ttu-id="631ea-109">Идентификатор процесса для процесса, который отправляет уведомление об индексации индексатор обработчик протокола MAPI.</span><span class="sxs-lookup"><span data-stu-id="631ea-109">Process ID for the process that is sending an indexing notification to the indexer of the MAPI Protocol Handler.</span></span> 
    

