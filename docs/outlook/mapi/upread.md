---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 887c66277b54e2e14c7f67c76b8e9dd4fa8bc719
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589233"
---
# <a name="upread"></a><span data-ttu-id="e0dba-103">UPREAD</span><span class="sxs-lookup"><span data-stu-id="e0dba-103">UPREAD</span></span>

  
  
<span data-ttu-id="e0dba-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0dba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0dba-105">Информация для загрузки состояние чтения элементов во время [Отправить прочитать состояние состояние](upload-read-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="e0dba-105">Information for uploading the read state of items during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e0dba-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e0dba-106">Quick info</span></span>

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="e0dba-107">Members</span><span class="sxs-lookup"><span data-stu-id="e0dba-107">Members</span></span>

 <span data-ttu-id="e0dba-108">_pupre_</span><span class="sxs-lookup"><span data-stu-id="e0dba-108">_pupre_</span></span>
  
>  <span data-ttu-id="e0dba-109">[out] Вектор **[UPREADE](upreade.md)** записей.</span><span class="sxs-lookup"><span data-stu-id="e0dba-109">[out] Vector of **[UPREADE](upreade.md)** entries.</span></span> 
    
 <span data-ttu-id="e0dba-110">_централизованной_</span><span class="sxs-lookup"><span data-stu-id="e0dba-110">_cEnt_</span></span>
  
>  <span data-ttu-id="e0dba-111">[out] Число записей **UPREADE** .</span><span class="sxs-lookup"><span data-stu-id="e0dba-111">[out] Number of **UPREADE** entries.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e0dba-112">См. также</span><span class="sxs-lookup"><span data-stu-id="e0dba-112">See also</span></span>



[<span data-ttu-id="e0dba-113">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="e0dba-113">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e0dba-114">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="e0dba-114">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e0dba-115">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="e0dba-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e0dba-116">UPREADE</span><span class="sxs-lookup"><span data-stu-id="e0dba-116">UPREADE</span></span>](upreade.md)

