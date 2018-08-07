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
ms.openlocfilehash: c207b1db6a24cc60967735e2f4b1a4aa97007750
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812320"
---
# <a name="slongarray"></a><span data-ttu-id="f9cf9-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="f9cf9-103">SLongArray</span></span>

  
  
<span data-ttu-id="f9cf9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f9cf9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f9cf9-105">Содержит массив типов значение типа LONG, которые используются для описания свойства типа PT_MV_LONG.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f9cf9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f9cf9-106">Header file:</span></span>  <br/> |<span data-ttu-id="f9cf9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f9cf9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="f9cf9-108">Members</span><span class="sxs-lookup"><span data-stu-id="f9cf9-108">Members</span></span>

 <span data-ttu-id="f9cf9-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="f9cf9-109">**cValues**</span></span>
  
> <span data-ttu-id="f9cf9-110">Число значений в массиве, на который указывает член **lpl** .</span><span class="sxs-lookup"><span data-stu-id="f9cf9-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="f9cf9-111">**lpl**</span><span class="sxs-lookup"><span data-stu-id="f9cf9-111">**lpl**</span></span>
  
> <span data-ttu-id="f9cf9-112">Указатель на массив значений времени.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9cf9-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="f9cf9-113">Remarks</span></span>

<span data-ttu-id="f9cf9-114">Дополнительные сведения о PT_MV_LONG увидеть [Список типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="f9cf9-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f9cf9-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f9cf9-115">See also</span></span>



[<span data-ttu-id="f9cf9-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f9cf9-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f9cf9-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="f9cf9-117">MAPI Structures</span></span>](mapi-structures.md)

