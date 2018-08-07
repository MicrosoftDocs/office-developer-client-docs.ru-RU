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
ms.openlocfilehash: cde59b73381458533910dc8f0a728cc4e6ca0c01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812230"
---
# <a name="sdoublearray"></a><span data-ttu-id="47c2f-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="47c2f-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="47c2f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47c2f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47c2f-105">Содержит массив типа Double, используемый для описания свойства типа PT_MV_DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="47c2f-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47c2f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="47c2f-106">Header file:</span></span>  <br/> |<span data-ttu-id="47c2f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47c2f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="47c2f-108">Members</span><span class="sxs-lookup"><span data-stu-id="47c2f-108">Members</span></span>

 <span data-ttu-id="47c2f-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="47c2f-109">**cValues**</span></span>
  
> <span data-ttu-id="47c2f-110">Число значений в массиве, на который указывает член **lpdbl** .</span><span class="sxs-lookup"><span data-stu-id="47c2f-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="47c2f-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="47c2f-111">**lpdbl**</span></span>
  
> <span data-ttu-id="47c2f-112">Указатель на массив значений двойной точности.</span><span class="sxs-lookup"><span data-stu-id="47c2f-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47c2f-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="47c2f-113">Remarks</span></span>

<span data-ttu-id="47c2f-114">Дополнительные сведения о PT_MV_DOUBLE увидеть [Список типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="47c2f-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="47c2f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="47c2f-115">See also</span></span>



[<span data-ttu-id="47c2f-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="47c2f-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="47c2f-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="47c2f-117">MAPI Structures</span></span>](mapi-structures.md)

