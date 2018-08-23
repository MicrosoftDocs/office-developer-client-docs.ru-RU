---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a44974accea30b5d1406c9cc74570012f61639e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580651"
---
# <a name="slongarray"></a><span data-ttu-id="368fa-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="368fa-103">SLongArray</span></span>

  
  
<span data-ttu-id="368fa-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="368fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="368fa-105">Содержит массив типов значение типа LONG, которые используются для описания свойства типа PT_MV_LONG.</span><span class="sxs-lookup"><span data-stu-id="368fa-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="368fa-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="368fa-106">Header file:</span></span>  <br/> |<span data-ttu-id="368fa-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="368fa-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="368fa-108">Members</span><span class="sxs-lookup"><span data-stu-id="368fa-108">Members</span></span>

 <span data-ttu-id="368fa-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="368fa-109">**cValues**</span></span>
  
> <span data-ttu-id="368fa-110">Число значений в массиве, на который указывает член **lpl** .</span><span class="sxs-lookup"><span data-stu-id="368fa-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="368fa-111">**lpl**</span><span class="sxs-lookup"><span data-stu-id="368fa-111">**lpl**</span></span>
  
> <span data-ttu-id="368fa-112">Указатель на массив значений времени.</span><span class="sxs-lookup"><span data-stu-id="368fa-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="368fa-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="368fa-113">Remarks</span></span>

<span data-ttu-id="368fa-114">Дополнительные сведения о PT_MV_LONG увидеть [Список типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="368fa-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="368fa-115">См. также</span><span class="sxs-lookup"><span data-stu-id="368fa-115">See also</span></span>



[<span data-ttu-id="368fa-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="368fa-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="368fa-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="368fa-117">MAPI Structures</span></span>](mapi-structures.md)

