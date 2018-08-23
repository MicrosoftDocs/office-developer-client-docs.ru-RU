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
ms.openlocfilehash: 29b26996bc337045489758a14857a30fafe48e54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576437"
---
# <a name="slargeintegerarray"></a><span data-ttu-id="85cfc-103">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="85cfc-103">SLargeIntegerArray</span></span>

  
  
<span data-ttu-id="85cfc-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85cfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85cfc-105">Содержит массив [LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130) структуры, используемые для описания свойства типа PT_MV_I8.</span><span class="sxs-lookup"><span data-stu-id="85cfc-105">Contains an array of [LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130) structures that are used to describe a property of type PT_MV_I8.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85cfc-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="85cfc-106">Header file:</span></span>  <br/> |<span data-ttu-id="85cfc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="85cfc-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a><span data-ttu-id="85cfc-108">Members</span><span class="sxs-lookup"><span data-stu-id="85cfc-108">Members</span></span>

 <span data-ttu-id="85cfc-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="85cfc-109">**cValues**</span></span>
  
> <span data-ttu-id="85cfc-110">Число значений в массиве, на который указывает член **lpli** .</span><span class="sxs-lookup"><span data-stu-id="85cfc-110">Count of values in the array pointed to by the **lpli** member.</span></span> 
    
 <span data-ttu-id="85cfc-111">**lpli**</span><span class="sxs-lookup"><span data-stu-id="85cfc-111">**lpli**</span></span>
  
> <span data-ttu-id="85cfc-112">Указатель на массив структур **LARGE_INTEGER** , сохраняя значения целое число.</span><span class="sxs-lookup"><span data-stu-id="85cfc-112">Pointer to an array of **LARGE_INTEGER** structures holding the integer values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="85cfc-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="85cfc-113">Remarks</span></span>

<span data-ttu-id="85cfc-114">Дополнительные сведения о PT_MV_18 увидеть [Список типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="85cfc-114">For more information about PT_MV_18, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="85cfc-115">См. также</span><span class="sxs-lookup"><span data-stu-id="85cfc-115">See also</span></span>



[<span data-ttu-id="85cfc-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="85cfc-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="85cfc-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="85cfc-117">MAPI Structures</span></span>](mapi-structures.md)

