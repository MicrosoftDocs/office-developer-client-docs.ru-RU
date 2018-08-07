---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4d6785783f69857bd93f3c5818983e832e16af05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812328"
---
# <a name="slargeintegerarray"></a><span data-ttu-id="1ce9a-103">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="1ce9a-103">SLargeIntegerArray</span></span>

  
  
<span data-ttu-id="1ce9a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ce9a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ce9a-105">Содержит массив [LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130) структуры, используемые для описания свойства типа PT_MV_I8.</span><span class="sxs-lookup"><span data-stu-id="1ce9a-105">Contains an array of [LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130) structures that are used to describe a property of type PT_MV_I8.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ce9a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1ce9a-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ce9a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ce9a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a><span data-ttu-id="1ce9a-108">Members</span><span class="sxs-lookup"><span data-stu-id="1ce9a-108">Members</span></span>

 <span data-ttu-id="1ce9a-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="1ce9a-109">**cValues**</span></span>
  
> <span data-ttu-id="1ce9a-110">Число значений в массиве, на который указывает член **lpli** .</span><span class="sxs-lookup"><span data-stu-id="1ce9a-110">Count of values in the array pointed to by the **lpli** member.</span></span> 
    
 <span data-ttu-id="1ce9a-111">**lpli**</span><span class="sxs-lookup"><span data-stu-id="1ce9a-111">**lpli**</span></span>
  
> <span data-ttu-id="1ce9a-112">Указатель на массив структур **LARGE_INTEGER** , сохраняя значения целое число.</span><span class="sxs-lookup"><span data-stu-id="1ce9a-112">Pointer to an array of **LARGE_INTEGER** structures holding the integer values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1ce9a-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="1ce9a-113">Remarks</span></span>

<span data-ttu-id="1ce9a-114">Дополнительные сведения о PT_MV_18 увидеть [Список типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="1ce9a-114">For more information about PT_MV_18, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1ce9a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="1ce9a-115">See also</span></span>



[<span data-ttu-id="1ce9a-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1ce9a-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="1ce9a-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="1ce9a-117">MAPI Structures</span></span>](mapi-structures.md)

