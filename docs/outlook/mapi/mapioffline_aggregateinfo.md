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
ms.openlocfilehash: 24e16aeb1bbee1c35cf8fbd5813fb3e83b762187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809881"
---
# <a name="mapiofflineaggregateinfo"></a><span data-ttu-id="935a9-103">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="935a9-103">MAPIOFFLINE_AGGREGATEINFO</span></span>

  
  
<span data-ttu-id="935a9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="935a9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="935a9-105">Структура используется с [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="935a9-105">The structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span> 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a><span data-ttu-id="935a9-106">Members</span><span class="sxs-lookup"><span data-stu-id="935a9-106">Members</span></span>

 <span data-ttu-id="935a9-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="935a9-107">**ulSize**</span></span>
  
> <span data-ttu-id="935a9-108">Размер структуры.</span><span class="sxs-lookup"><span data-stu-id="935a9-108">The size of the structure.</span></span>
    
 <span data-ttu-id="935a9-109">**pOuterObj**</span><span class="sxs-lookup"><span data-stu-id="935a9-109">**pOuterObj**</span></span>
  
> <span data-ttu-id="935a9-110">Указатель на объект IUnknown, на котором собирается этот объект.</span><span class="sxs-lookup"><span data-stu-id="935a9-110">A pointer to the IUnknown object onto which this object is being aggregated.</span></span> <span data-ttu-id="935a9-111">Это позволяет вызовы QueryInterface, проходящих через созданный объект.</span><span class="sxs-lookup"><span data-stu-id="935a9-111">This allows any QueryInterface calls to pass through to the created object.</span></span>
    
 <span data-ttu-id="935a9-112">**pRefTrackRoot**</span><span class="sxs-lookup"><span data-stu-id="935a9-112">**pRefTrackRoot**</span></span>
  
> <span data-ttu-id="935a9-113">Должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="935a9-113">Must be NULL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="935a9-114">См. также</span><span class="sxs-lookup"><span data-stu-id="935a9-114">See also</span></span>



[<span data-ttu-id="935a9-115">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="935a9-115">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="935a9-116">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="935a9-116">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

