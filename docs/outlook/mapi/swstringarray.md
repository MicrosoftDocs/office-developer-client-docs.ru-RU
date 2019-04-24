---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ff69981e83d42e439936a3e4be47eabfd811b310
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349555"
---
# <a name="swstringarray"></a><span data-ttu-id="7d690-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="7d690-103">SWStringArray</span></span>

  
  
<span data-ttu-id="7d690-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d690-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d690-105">Содержит массив строк символов, которые используются для описания свойства типа ПТ_МВ_УНИКОДЕ.</span><span class="sxs-lookup"><span data-stu-id="7d690-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d690-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7d690-106">Header file:</span></span>  <br/> |<span data-ttu-id="7d690-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="7d690-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="7d690-108">Members</span><span class="sxs-lookup"><span data-stu-id="7d690-108">Members</span></span>

 <span data-ttu-id="7d690-109">**Квалуес**</span><span class="sxs-lookup"><span data-stu-id="7d690-109">**cValues**</span></span>
  
> <span data-ttu-id="7d690-110">Количество строк в массиве, на которое указывает элемент **лппсзв** .</span><span class="sxs-lookup"><span data-stu-id="7d690-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="7d690-111">**Лппсзв**</span><span class="sxs-lookup"><span data-stu-id="7d690-111">**lppszW**</span></span>
  
> <span data-ttu-id="7d690-112">Указатель на массив строк Юникода с символами NULL.</span><span class="sxs-lookup"><span data-stu-id="7d690-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d690-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="7d690-113">Remarks</span></span>

<span data-ttu-id="7d690-114">Дополнительные сведения о ПТ_МВ_УНИКОДЕ можно найти в статье [типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="7d690-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7d690-115">См. также</span><span class="sxs-lookup"><span data-stu-id="7d690-115">See also</span></span>



[<span data-ttu-id="7d690-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7d690-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7d690-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="7d690-117">MAPI Structures</span></span>](mapi-structures.md)

