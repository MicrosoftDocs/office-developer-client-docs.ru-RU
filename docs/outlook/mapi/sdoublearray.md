---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6986ed7c9ab9932c5d95fcfb7f74f80088f21971
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580371"
---
# <a name="sdoublearray"></a><span data-ttu-id="f6a68-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="f6a68-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="f6a68-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6a68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6a68-105">Содержит массив типа Double, используемый для описания свойства типа PT_MV_DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="f6a68-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f6a68-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f6a68-106">Header file:</span></span>  <br/> |<span data-ttu-id="f6a68-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6a68-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="f6a68-108">Members</span><span class="sxs-lookup"><span data-stu-id="f6a68-108">Members</span></span>

 <span data-ttu-id="f6a68-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="f6a68-109">**cValues**</span></span>
  
> <span data-ttu-id="f6a68-110">Число значений в массиве, на который указывает член **lpdbl** .</span><span class="sxs-lookup"><span data-stu-id="f6a68-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="f6a68-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="f6a68-111">**lpdbl**</span></span>
  
> <span data-ttu-id="f6a68-112">Указатель на массив значений двойной точности.</span><span class="sxs-lookup"><span data-stu-id="f6a68-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6a68-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="f6a68-113">Remarks</span></span>

<span data-ttu-id="f6a68-114">Дополнительные сведения о PT_MV_DOUBLE увидеть [Список типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="f6a68-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f6a68-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f6a68-115">See also</span></span>



[<span data-ttu-id="f6a68-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f6a68-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f6a68-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="f6a68-117">MAPI Structures</span></span>](mapi-structures.md)

