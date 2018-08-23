---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 057a1ff38ed3809ce03bce8f820f1d16eea7fb46
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581127"
---
# <a name="updel"></a><span data-ttu-id="ee1d4-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="ee1d4-103">UPDEL</span></span>

  
  
<span data-ttu-id="ee1d4-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee1d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee1d4-105">Сведения для элементов, которые были удалены в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="ee1d4-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="ee1d4-106">Эти сведения используются во время [загрузки удалить состояние состояние](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="ee1d4-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ee1d4-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="ee1d4-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="ee1d4-108">Members</span><span class="sxs-lookup"><span data-stu-id="ee1d4-108">Members</span></span>

 <span data-ttu-id="ee1d4-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="ee1d4-109">_pupde_</span></span>
  
>  <span data-ttu-id="ee1d4-110">[out] Вектор [UPDELE](updele.md) записей.</span><span class="sxs-lookup"><span data-stu-id="ee1d4-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="ee1d4-111">_централизованной_</span><span class="sxs-lookup"><span data-stu-id="ee1d4-111">_cEnt_</span></span>
  
> <span data-ttu-id="ee1d4-112">[out] Число записей в *pupde* .</span><span class="sxs-lookup"><span data-stu-id="ee1d4-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ee1d4-113">См. также</span><span class="sxs-lookup"><span data-stu-id="ee1d4-113">See also</span></span>



[<span data-ttu-id="ee1d4-114">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="ee1d4-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="ee1d4-115">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="ee1d4-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="ee1d4-116">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="ee1d4-116">MAPI Constants</span></span>](mapi-constants.md)

