---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8439d6609ebece75699a1150a9d0c1a41277fd52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429875"
---
# <a name="srealarray"></a><span data-ttu-id="3d487-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="3d487-103">SRealArray</span></span>

  
  
<span data-ttu-id="3d487-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d487-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d487-105">Содержит массив значений float, используемых для описания свойства типа PT_MV_R4.</span><span class="sxs-lookup"><span data-stu-id="3d487-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3d487-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3d487-106">Header file:</span></span>  <br/> |<span data-ttu-id="3d487-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d487-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="3d487-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="3d487-108">Members</span></span>

 <span data-ttu-id="3d487-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="3d487-109">**cValues**</span></span>
  
> <span data-ttu-id="3d487-110">Количество значений в массиве, на который указывает член **lpflt.**</span><span class="sxs-lookup"><span data-stu-id="3d487-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="3d487-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="3d487-111">**lpflt**</span></span>
  
> <span data-ttu-id="3d487-112">Указатель на массив значений float.</span><span class="sxs-lookup"><span data-stu-id="3d487-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3d487-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="3d487-113">Remarks</span></span>

<span data-ttu-id="3d487-114">Дополнительные сведения о типе PT_MV_R4 см. введите [Типы свойств.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="3d487-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3d487-115">См. также</span><span class="sxs-lookup"><span data-stu-id="3d487-115">See also</span></span>



[<span data-ttu-id="3d487-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3d487-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="3d487-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="3d487-117">MAPI Structures</span></span>](mapi-structures.md)

