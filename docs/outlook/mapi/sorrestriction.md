---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 06b9b6a046aaa0f16418f75d402cc5be44f845a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812351"
---
# <a name="sorrestriction"></a><span data-ttu-id="a8d6f-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="a8d6f-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="a8d6f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8d6f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8d6f-105">Описание ограничений **или** , в которой используется для применения логической операции **или** ограничение.</span><span class="sxs-lookup"><span data-stu-id="a8d6f-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8d6f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a8d6f-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8d6f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8d6f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="a8d6f-108">Members</span><span class="sxs-lookup"><span data-stu-id="a8d6f-108">Members</span></span>

 <span data-ttu-id="a8d6f-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="a8d6f-109">**cRes**</span></span>
  
> <span data-ttu-id="a8d6f-110">Число структур в массиве, на который указывает член **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="a8d6f-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="a8d6f-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="a8d6f-111">**lpRes**</span></span>
  
> <span data-ttu-id="a8d6f-112">Указатель на структуру [SRestriction](srestriction.md) , описывающий ограничения для объединения с помощью логической операции **или** .</span><span class="sxs-lookup"><span data-stu-id="a8d6f-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a8d6f-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="a8d6f-113">Remarks</span></span>

<span data-ttu-id="a8d6f-114">Дополнительные сведения о структуре **SOrRestriction** [О ограничения](about-restrictions.md)см.</span><span class="sxs-lookup"><span data-stu-id="a8d6f-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8d6f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a8d6f-115">See also</span></span>



[<span data-ttu-id="a8d6f-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="a8d6f-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="a8d6f-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a8d6f-117">MAPI Structures</span></span>](mapi-structures.md)

