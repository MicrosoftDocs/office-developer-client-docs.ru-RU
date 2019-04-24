---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 44e3613338c8932bc80dd1150392033dfa3cd050
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278738"
---
# <a name="isequalmapiuid"></a><span data-ttu-id="e011f-103">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="e011f-103">IsEqualMAPIUID</span></span>

  
  
<span data-ttu-id="e011f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e011f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e011f-105">Тестирует две структуры [мапиуид](mapiuid.md) , чтобы определить, содержат ли они один и тот же идентификатор.</span><span class="sxs-lookup"><span data-stu-id="e011f-105">Tests two [MAPIUID](mapiuid.md) structures to determine whether they contain the same identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e011f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e011f-106">Header file:</span></span>  <br/> |<span data-ttu-id="e011f-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="e011f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e011f-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="e011f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="e011f-109">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="e011f-109">**MAPIUID**</span></span> <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a><span data-ttu-id="e011f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e011f-110">Parameters</span></span>

 <span data-ttu-id="e011f-111">_lpuid1_</span><span class="sxs-lookup"><span data-stu-id="e011f-111">_lpuid1_</span></span>
  
> <span data-ttu-id="e011f-112">Указатель на первую структуру **мапиуид** , которую необходимо протестировать.</span><span class="sxs-lookup"><span data-stu-id="e011f-112">Pointer to the first **MAPIUID** structure to be tested.</span></span> 
    
 <span data-ttu-id="e011f-113">_lpuid2_</span><span class="sxs-lookup"><span data-stu-id="e011f-113">_lpuid2_</span></span>
  
> <span data-ttu-id="e011f-114">Указатель на вторую структуру **мапиуид** , которую необходимо протестировать.</span><span class="sxs-lookup"><span data-stu-id="e011f-114">Pointer to the second **MAPIUID** structure to be tested.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e011f-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="e011f-115">Remarks</span></span>

<span data-ttu-id="e011f-116">Макрос **исекуалмапиуид** ВОЗВРАЩАЕТ значение true, если две структуры **мапиуид** содержат один и тот же идентификатор, и значение false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e011f-116">The **IsEqualMAPIUID** macro returns TRUE if the two **MAPIUID** structures contain the same identifier and FALSE if they do not.</span></span> 
  
<span data-ttu-id="e011f-117">Для макроса **исекуалмапиуид** необходимо включить файл заголовков Memory. h.</span><span class="sxs-lookup"><span data-stu-id="e011f-117">The **IsEqualMAPIUID** macro requires that the header file Memory.h be included.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e011f-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e011f-118">See also</span></span>



[<span data-ttu-id="e011f-119">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e011f-119">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="e011f-120">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="e011f-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

