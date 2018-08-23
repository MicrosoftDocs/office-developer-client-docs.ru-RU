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
ms.openlocfilehash: e3f53a894b7f7cdaa68e66530c7bd99bf49b9ed0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581358"
---
# <a name="swstringarray"></a><span data-ttu-id="9a959-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="9a959-103">SWStringArray</span></span>

  
  
<span data-ttu-id="9a959-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a959-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a959-105">Содержит массив строк символов, которые используются для описания свойства типа PT_MV_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="9a959-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a959-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9a959-106">Header file:</span></span>  <br/> |<span data-ttu-id="9a959-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9a959-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="9a959-108">Members</span><span class="sxs-lookup"><span data-stu-id="9a959-108">Members</span></span>

 <span data-ttu-id="9a959-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="9a959-109">**cValues**</span></span>
  
> <span data-ttu-id="9a959-110">Количество строк в массиве, на который указывает член **lppszW** .</span><span class="sxs-lookup"><span data-stu-id="9a959-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="9a959-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="9a959-111">**lppszW**</span></span>
  
> <span data-ttu-id="9a959-112">Указатель на массив строк символ Unicode завершен null.</span><span class="sxs-lookup"><span data-stu-id="9a959-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a959-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="9a959-113">Remarks</span></span>

<span data-ttu-id="9a959-114">Дополнительные сведения о PT_MV_UNICODE можно [Типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="9a959-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a959-115">См. также</span><span class="sxs-lookup"><span data-stu-id="9a959-115">See also</span></span>



[<span data-ttu-id="9a959-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9a959-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="9a959-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="9a959-117">MAPI Structures</span></span>](mapi-structures.md)

