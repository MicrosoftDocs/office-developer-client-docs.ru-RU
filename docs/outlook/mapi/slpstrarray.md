---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ccad74a9f2553bf29af124821c6d6a87dcde3303
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572874"
---
# <a name="slpstrarray"></a><span data-ttu-id="44ee5-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="44ee5-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="44ee5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44ee5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44ee5-105">Содержит массив строковых значений, которые используются для описания свойства типа PT_MV_STRING8.</span><span class="sxs-lookup"><span data-stu-id="44ee5-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44ee5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="44ee5-106">Header file:</span></span>  <br/> |<span data-ttu-id="44ee5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44ee5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="44ee5-108">Members</span><span class="sxs-lookup"><span data-stu-id="44ee5-108">Members</span></span>

 <span data-ttu-id="44ee5-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="44ee5-109">**cValues**</span></span>
  
> <span data-ttu-id="44ee5-110">Число значений в массиве, на который указывает член **lppszA** .</span><span class="sxs-lookup"><span data-stu-id="44ee5-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="44ee5-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="44ee5-111">**lppszA**</span></span>
  
> <span data-ttu-id="44ee5-112">Указатель на массив строк завершен null 8-разрядных символов.</span><span class="sxs-lookup"><span data-stu-id="44ee5-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44ee5-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="44ee5-113">Remarks</span></span>

<span data-ttu-id="44ee5-114">Дополнительные сведения о PT_MV_STRING8 увидеть [Список типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="44ee5-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="44ee5-115">См. также</span><span class="sxs-lookup"><span data-stu-id="44ee5-115">See also</span></span>



[<span data-ttu-id="44ee5-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="44ee5-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="44ee5-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="44ee5-117">MAPI Structures</span></span>](mapi-structures.md)

