---
title: SYNCSTATE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 63c47e94-f603-aef9-afed-e3819bd79408
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a27f38e759862c7091205a6f9a8aa1cde90c38e3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575534"
---
# <a name="syncstate"></a><span data-ttu-id="70fed-103">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="70fed-103">SYNCSTATE</span></span>

<span data-ttu-id="70fed-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70fed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70fed-105">Эта структура определяет состояния для этого компьютера состояние репликации.</span><span class="sxs-lookup"><span data-stu-id="70fed-105">This structure defines the states for the replication state machine.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="70fed-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="70fed-106">Quick info</span></span>

```cpp
typedef enum { 
    LR_SYNC_IDLE = 0, 
    LR_SYNC, 
    LR_SYNC_UPLOAD_HIERARCHY, 
    LR_SYNC_UPLOAD_FOLDER, 
    LR_SYNC_CONTENTS, 
    LR_SYNC_UPLOAD_TABLE, 
    LR_SYNC_UPLOAD_MESSAGE, 
    LR_SYNC_UPLOAD_MESSAGE_READ = 8, 
    LR_SYNC_UPLOAD_MESSAGE_DEL, 
    LR_SYNC_DOWNLOAD_HIERARCHY, 
    LR_SYNC_DOWNLOAD_TABLE, 
    LR_SYNC_DOWNLOAD_HEADER = 17 
} SYNCSTATE; 

```

## <a name="see-also"></a><span data-ttu-id="70fed-107">См. также</span><span class="sxs-lookup"><span data-stu-id="70fed-107">See also</span></span>

- [<span data-ttu-id="70fed-108">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="70fed-108">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="70fed-109">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="70fed-109">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="70fed-110">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="70fed-110">MAPI Constants</span></span>](mapi-constants.md)

