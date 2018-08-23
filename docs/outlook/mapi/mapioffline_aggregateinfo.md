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
ms.openlocfilehash: eb182d9cc51c196558f9e9192a65352e87372bf0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582520"
---
# <a name="mapiofflineaggregateinfo"></a><span data-ttu-id="0ed7f-103">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="0ed7f-103">MAPIOFFLINE_AGGREGATEINFO</span></span>

  
  
<span data-ttu-id="0ed7f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ed7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ed7f-105">Структура используется с [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="0ed7f-105">The structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span> 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a><span data-ttu-id="0ed7f-106">Members</span><span class="sxs-lookup"><span data-stu-id="0ed7f-106">Members</span></span>

 <span data-ttu-id="0ed7f-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="0ed7f-107">**ulSize**</span></span>
  
> <span data-ttu-id="0ed7f-108">Размер структуры.</span><span class="sxs-lookup"><span data-stu-id="0ed7f-108">The size of the structure.</span></span>
    
 <span data-ttu-id="0ed7f-109">**pOuterObj**</span><span class="sxs-lookup"><span data-stu-id="0ed7f-109">**pOuterObj**</span></span>
  
> <span data-ttu-id="0ed7f-110">Указатель на объект IUnknown, на котором собирается этот объект.</span><span class="sxs-lookup"><span data-stu-id="0ed7f-110">A pointer to the IUnknown object onto which this object is being aggregated.</span></span> <span data-ttu-id="0ed7f-111">Это позволяет вызовы QueryInterface, проходящих через созданный объект.</span><span class="sxs-lookup"><span data-stu-id="0ed7f-111">This allows any QueryInterface calls to pass through to the created object.</span></span>
    
 <span data-ttu-id="0ed7f-112">**pRefTrackRoot**</span><span class="sxs-lookup"><span data-stu-id="0ed7f-112">**pRefTrackRoot**</span></span>
  
> <span data-ttu-id="0ed7f-113">Должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="0ed7f-113">Must be NULL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ed7f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="0ed7f-114">See also</span></span>



[<span data-ttu-id="0ed7f-115">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="0ed7f-115">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="0ed7f-116">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="0ed7f-116">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

