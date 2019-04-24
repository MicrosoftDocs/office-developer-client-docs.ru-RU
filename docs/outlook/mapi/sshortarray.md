---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8ea7d51b15a6e6acd44a3c0b6158378661f311bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344501"
---
# <a name="sshortarray"></a><span data-ttu-id="5649d-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="5649d-103">SShortArray</span></span>

  
  
<span data-ttu-id="5649d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5649d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5649d-105">Содержит массив целочисленных значений без знака, которые используются для описания свойства типа ПТ_МВ_ШОРТ.</span><span class="sxs-lookup"><span data-stu-id="5649d-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5649d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5649d-106">Header file:</span></span>  <br/> |<span data-ttu-id="5649d-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="5649d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="5649d-108">Members</span><span class="sxs-lookup"><span data-stu-id="5649d-108">Members</span></span>

 <span data-ttu-id="5649d-109">**Квалуес**</span><span class="sxs-lookup"><span data-stu-id="5649d-109">**cValues**</span></span>
  
> <span data-ttu-id="5649d-110">Количество значений в массиве, на которое указывает элемент **LPI** .</span><span class="sxs-lookup"><span data-stu-id="5649d-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="5649d-111">**LPI**</span><span class="sxs-lookup"><span data-stu-id="5649d-111">**lpi**</span></span>
  
> <span data-ttu-id="5649d-112">Указатель на массив значений целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="5649d-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5649d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5649d-113">Remarks</span></span>

<span data-ttu-id="5649d-114">Дополнительные сведения о ПТ_МВ_ШОРТ и других типах свойств приведены в разделе [типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="5649d-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5649d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="5649d-115">See also</span></span>



[<span data-ttu-id="5649d-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5649d-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="5649d-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5649d-117">MAPI Structures</span></span>](mapi-structures.md)

