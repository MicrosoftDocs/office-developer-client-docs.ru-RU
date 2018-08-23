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
ms.openlocfilehash: 8c7ce2805248bf91ce7da071c67ece28a5b8ca07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564285"
---
# <a name="srealarray"></a><span data-ttu-id="d000a-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="d000a-103">SRealArray</span></span>

  
  
<span data-ttu-id="d000a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d000a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d000a-105">Содержит массив значений с плавающей запятой, которые используются для описания свойства типа PT_MV_R4.</span><span class="sxs-lookup"><span data-stu-id="d000a-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d000a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d000a-106">Header file:</span></span>  <br/> |<span data-ttu-id="d000a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d000a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="d000a-108">Members</span><span class="sxs-lookup"><span data-stu-id="d000a-108">Members</span></span>

 <span data-ttu-id="d000a-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="d000a-109">**cValues**</span></span>
  
> <span data-ttu-id="d000a-110">Число значений в массиве, на который указывает член **lpflt** .</span><span class="sxs-lookup"><span data-stu-id="d000a-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="d000a-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="d000a-111">**lpflt**</span></span>
  
> <span data-ttu-id="d000a-112">Указатель на массив значений с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="d000a-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d000a-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="d000a-113">Remarks</span></span>

<span data-ttu-id="d000a-114">Дополнительные сведения о типе свойства PT_MV_R4 можно [Типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="d000a-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d000a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d000a-115">See also</span></span>



[<span data-ttu-id="d000a-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d000a-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d000a-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="d000a-117">MAPI Structures</span></span>](mapi-structures.md)

