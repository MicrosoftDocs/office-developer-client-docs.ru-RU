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
ms.openlocfilehash: 6d2bb6bdb934e0b02831b813b1246a3df4193e0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812326"
---
# <a name="slpstrarray"></a><span data-ttu-id="04814-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="04814-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="04814-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="04814-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="04814-105">Содержит массив строковых значений, которые используются для описания свойства типа PT_MV_STRING8.</span><span class="sxs-lookup"><span data-stu-id="04814-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="04814-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="04814-106">Header file:</span></span>  <br/> |<span data-ttu-id="04814-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="04814-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="04814-108">Members</span><span class="sxs-lookup"><span data-stu-id="04814-108">Members</span></span>

 <span data-ttu-id="04814-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="04814-109">**cValues**</span></span>
  
> <span data-ttu-id="04814-110">Число значений в массиве, на который указывает член **lppszA** .</span><span class="sxs-lookup"><span data-stu-id="04814-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="04814-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="04814-111">**lppszA**</span></span>
  
> <span data-ttu-id="04814-112">Указатель на массив строк завершен null 8-разрядных символов.</span><span class="sxs-lookup"><span data-stu-id="04814-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04814-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="04814-113">Remarks</span></span>

<span data-ttu-id="04814-114">Дополнительные сведения о PT_MV_STRING8 увидеть [Список типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="04814-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="04814-115">См. также</span><span class="sxs-lookup"><span data-stu-id="04814-115">See also</span></span>



[<span data-ttu-id="04814-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="04814-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="04814-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="04814-117">MAPI Structures</span></span>](mapi-structures.md)

