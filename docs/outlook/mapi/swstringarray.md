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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413607"
---
# <a name="swstringarray"></a><span data-ttu-id="b4bba-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="b4bba-103">SWStringArray</span></span>

  
  
<span data-ttu-id="b4bba-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4bba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4bba-105">Содержит массив строк символов, используемых для описания свойства типа PT_MV_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="b4bba-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4bba-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b4bba-106">Header file:</span></span>  <br/> |<span data-ttu-id="b4bba-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4bba-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="b4bba-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="b4bba-108">Members</span></span>

 <span data-ttu-id="b4bba-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="b4bba-109">**cValues**</span></span>
  
> <span data-ttu-id="b4bba-110">Количество строк в массиве, на который указывает член **lppszW.**</span><span class="sxs-lookup"><span data-stu-id="b4bba-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="b4bba-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="b4bba-111">**lppszW**</span></span>
  
> <span data-ttu-id="b4bba-112">Указатель на массив строк символов Юникода с нулью.</span><span class="sxs-lookup"><span data-stu-id="b4bba-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b4bba-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4bba-113">Remarks</span></span>

<span data-ttu-id="b4bba-114">Дополнительные сведения о PT_MV_UNICODE см. [в подгонах "Типы свойств".](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="b4bba-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b4bba-115">См. также</span><span class="sxs-lookup"><span data-stu-id="b4bba-115">See also</span></span>



[<span data-ttu-id="b4bba-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b4bba-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="b4bba-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="b4bba-117">MAPI Structures</span></span>](mapi-structures.md)

