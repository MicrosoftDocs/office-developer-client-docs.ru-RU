---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9d9fd04776742383f40c6989bcf588b24b33d84b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406782"
---
# <a name="sdatetimearray"></a><span data-ttu-id="19ab4-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="19ab4-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="19ab4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19ab4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19ab4-105">Содержит массив значений времени, используемых для описания свойства типа PT_MV_SYSTIME.</span><span class="sxs-lookup"><span data-stu-id="19ab4-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19ab4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="19ab4-106">Header file:</span></span>  <br/> |<span data-ttu-id="19ab4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19ab4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="19ab4-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="19ab4-108">Members</span></span>

 <span data-ttu-id="19ab4-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="19ab4-109">**cValues**</span></span>
  
> <span data-ttu-id="19ab4-110">Количество значений в массиве, на который указывает **член lpft.**</span><span class="sxs-lookup"><span data-stu-id="19ab4-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="19ab4-111">**lpft**</span><span class="sxs-lookup"><span data-stu-id="19ab4-111">**lpft**</span></span>
  
> <span data-ttu-id="19ab4-112">Указатель на массив структур [FILETIME,](filetime.md) содержащих значения времени.</span><span class="sxs-lookup"><span data-stu-id="19ab4-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="19ab4-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="19ab4-113">Remarks</span></span>

<span data-ttu-id="19ab4-114">Дополнительные сведения о PT_MV_SYSTIME [см. в списке типов свойств.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="19ab4-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="19ab4-115">См. также</span><span class="sxs-lookup"><span data-stu-id="19ab4-115">See also</span></span>



[<span data-ttu-id="19ab4-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="19ab4-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="19ab4-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="19ab4-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="19ab4-118">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="19ab4-118">MAPI Structures</span></span>](mapi-structures.md)

