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
ms.openlocfilehash: 1578e26ec96f69975c2304cb185f352193a52c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812438"
---
# <a name="swstringarray"></a><span data-ttu-id="49f7a-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="49f7a-103">SWStringArray</span></span>

  
  
<span data-ttu-id="49f7a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="49f7a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="49f7a-105">Содержит массив строк символов, которые используются для описания свойства типа PT_MV_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="49f7a-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49f7a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="49f7a-106">Header file:</span></span>  <br/> |<span data-ttu-id="49f7a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49f7a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="49f7a-108">Members</span><span class="sxs-lookup"><span data-stu-id="49f7a-108">Members</span></span>

 <span data-ttu-id="49f7a-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="49f7a-109">**cValues**</span></span>
  
> <span data-ttu-id="49f7a-110">Количество строк в массиве, на который указывает член **lppszW** .</span><span class="sxs-lookup"><span data-stu-id="49f7a-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="49f7a-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="49f7a-111">**lppszW**</span></span>
  
> <span data-ttu-id="49f7a-112">Указатель на массив строк символ Unicode завершен null.</span><span class="sxs-lookup"><span data-stu-id="49f7a-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49f7a-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="49f7a-113">Remarks</span></span>

<span data-ttu-id="49f7a-114">Дополнительные сведения о PT_MV_UNICODE можно [Типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="49f7a-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="49f7a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="49f7a-115">See also</span></span>



[<span data-ttu-id="49f7a-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="49f7a-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="49f7a-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="49f7a-117">MAPI Structures</span></span>](mapi-structures.md)

