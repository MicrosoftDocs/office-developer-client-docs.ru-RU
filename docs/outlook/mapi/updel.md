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
ms.openlocfilehash: c9d2ec7f1970e3d1cadb65ab9af360b5c01c6844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360489"
---
# <a name="updel"></a><span data-ttu-id="e1355-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="e1355-103">UPDEL</span></span>

  
  
<span data-ttu-id="e1355-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1355-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1355-105">Сведения об элементах, удаленных в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="e1355-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="e1355-106">Эти сведения используются в состоянии состояния [отправки для удаления](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="e1355-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e1355-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e1355-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="e1355-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="e1355-108">Members</span></span>

 <span data-ttu-id="e1355-109">_пупде_</span><span class="sxs-lookup"><span data-stu-id="e1355-109">_pupde_</span></span>
  
>  <span data-ttu-id="e1355-110">вышли Вектор записей [](updele.md) .</span><span class="sxs-lookup"><span data-stu-id="e1355-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="e1355-111">_Центов_</span><span class="sxs-lookup"><span data-stu-id="e1355-111">_cEnt_</span></span>
  
> <span data-ttu-id="e1355-112">вышли Количество записей в *пупде* .</span><span class="sxs-lookup"><span data-stu-id="e1355-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e1355-113">См. также</span><span class="sxs-lookup"><span data-stu-id="e1355-113">See also</span></span>



[<span data-ttu-id="e1355-114">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="e1355-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e1355-115">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="e1355-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e1355-116">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="e1355-116">MAPI Constants</span></span>](mapi-constants.md)

