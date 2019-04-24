---
title: CbNewFLATENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CbNewFLATENTRY
api_type:
- COM
ms.assetid: 500437a4-e0bc-4368-b572-8aecded2621d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 33c8f1e8b573b5ff0f3d5f53e5b2cf127548688d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331838"
---
# <a name="cbnewflatentry"></a><span data-ttu-id="e3861-103">CbNewFLATENTRY</span><span class="sxs-lookup"><span data-stu-id="e3861-103">CbNewFLATENTRY</span></span>

  
  
<span data-ttu-id="e3861-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3861-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3861-105">Вычисляет количество байтов, которое необходимо выделить для новой структуры [флатентри](flatentry.md) , которая содержит идентификатор записи указанного размера в байтах.</span><span class="sxs-lookup"><span data-stu-id="e3861-105">Computes the number of bytes that should be allocated for a new [FLATENTRY](flatentry.md) structure that contains an entry identifier of a specified byte size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3861-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e3861-106">Header file:</span></span>  <br/> |<span data-ttu-id="e3861-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="e3861-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e3861-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="e3861-108">Related structure:</span></span>  <br/> |<span data-ttu-id="e3861-109">**FLATENTRY**</span><span class="sxs-lookup"><span data-stu-id="e3861-109">**FLATENTRY**</span></span> <br/> |
   
```cpp
CbNewFLATENTRY (_cb)
```

## <a name="parameters"></a><span data-ttu-id="e3861-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3861-110">Parameters</span></span>

 <span data-ttu-id="e3861-111">__CB_</span><span class="sxs-lookup"><span data-stu-id="e3861-111">__cb_</span></span>
  
> <span data-ttu-id="e3861-112">Количество байтов в идентификаторе записи, включаемых в новую структуру **флатентри** .</span><span class="sxs-lookup"><span data-stu-id="e3861-112">Count of bytes in the entry identifier to be included in the new **FLATENTRY** structure.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e3861-113">См. также</span><span class="sxs-lookup"><span data-stu-id="e3861-113">See also</span></span>



[<span data-ttu-id="e3861-114">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="e3861-114">FLATENTRY</span></span>](flatentry.md)


[<span data-ttu-id="e3861-115">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="e3861-115">Macros Related to Structures</span></span>](macros-related-to-structures.md)

