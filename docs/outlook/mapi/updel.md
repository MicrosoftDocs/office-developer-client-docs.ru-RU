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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436803"
---
# <a name="updel"></a><span data-ttu-id="b2158-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="b2158-103">UPDEL</span></span>

  
  
<span data-ttu-id="b2158-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2158-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2158-105">Сведения об удаленных в локальном хранилище элементов.</span><span class="sxs-lookup"><span data-stu-id="b2158-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="b2158-106">Эти сведения используются во время состояния [отправки удаления.](upload-delete-status-state.md)</span><span class="sxs-lookup"><span data-stu-id="b2158-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b2158-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="b2158-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="b2158-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="b2158-108">Members</span></span>

 <span data-ttu-id="b2158-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="b2158-109">_pupde_</span></span>
  
>  <span data-ttu-id="b2158-110">[out] Вектор [записей UPDELE.](updele.md)</span><span class="sxs-lookup"><span data-stu-id="b2158-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="b2158-111">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="b2158-111">_cEnt_</span></span>
  
> <span data-ttu-id="b2158-112">[out] Количество записей в *pupde.*</span><span class="sxs-lookup"><span data-stu-id="b2158-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b2158-113">См. также</span><span class="sxs-lookup"><span data-stu-id="b2158-113">See also</span></span>



[<span data-ttu-id="b2158-114">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="b2158-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b2158-115">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="b2158-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b2158-116">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="b2158-116">MAPI Constants</span></span>](mapi-constants.md)

