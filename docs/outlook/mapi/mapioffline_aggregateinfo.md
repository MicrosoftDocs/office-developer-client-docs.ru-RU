---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4775de0707eb90549f07525e3aa54ec5842f6050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438164"
---
# <a name="mapioffline_aggregateinfo"></a><span data-ttu-id="9e0bc-103">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="9e0bc-103">MAPIOFFLINE_AGGREGATEINFO</span></span>

  
  
<span data-ttu-id="9e0bc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e0bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e0bc-105">Структура используется с [помощью HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="9e0bc-105">The structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span> 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a><span data-ttu-id="9e0bc-106">"Участники"</span><span class="sxs-lookup"><span data-stu-id="9e0bc-106">Members</span></span>

 <span data-ttu-id="9e0bc-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="9e0bc-107">**ulSize**</span></span>
  
> <span data-ttu-id="9e0bc-108">Размер структуры.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-108">The size of the structure.</span></span>
    
 <span data-ttu-id="9e0bc-109">**pOuterObj**</span><span class="sxs-lookup"><span data-stu-id="9e0bc-109">**pOuterObj**</span></span>
  
> <span data-ttu-id="9e0bc-110">Указатель на объект IUnknown, на который этот объект агрегируется.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-110">A pointer to the IUnknown object onto which this object is being aggregated.</span></span> <span data-ttu-id="9e0bc-111">Это позволяет любым вызовам QueryInterface передавать созданный объект.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-111">This allows any QueryInterface calls to pass through to the created object.</span></span>
    
 <span data-ttu-id="9e0bc-112">**pRefTrackRoot**</span><span class="sxs-lookup"><span data-stu-id="9e0bc-112">**pRefTrackRoot**</span></span>
  
> <span data-ttu-id="9e0bc-113">Должно быть NULL.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-113">Must be NULL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e0bc-114">См. также</span><span class="sxs-lookup"><span data-stu-id="9e0bc-114">See also</span></span>



[<span data-ttu-id="9e0bc-115">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="9e0bc-115">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="9e0bc-116">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="9e0bc-116">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

