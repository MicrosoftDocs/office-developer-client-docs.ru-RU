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
ms.openlocfilehash: 9734adff9c9c7526fc8ff46d17ca913752e104b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812218"
---
# <a name="sdatetimearray"></a><span data-ttu-id="8ad56-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="8ad56-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="8ad56-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ad56-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ad56-105">Содержит массив значений времени, которые используются для описания свойства типа PT_MV_SYSTIME.</span><span class="sxs-lookup"><span data-stu-id="8ad56-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ad56-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8ad56-106">Header file:</span></span>  <br/> |<span data-ttu-id="8ad56-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ad56-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="8ad56-108">Members</span><span class="sxs-lookup"><span data-stu-id="8ad56-108">Members</span></span>

 <span data-ttu-id="8ad56-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="8ad56-109">**cValues**</span></span>
  
> <span data-ttu-id="8ad56-110">Число значений в массиве, на который указывает член **lpft** .</span><span class="sxs-lookup"><span data-stu-id="8ad56-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="8ad56-111">**lpft**</span><span class="sxs-lookup"><span data-stu-id="8ad56-111">**lpft**</span></span>
  
> <span data-ttu-id="8ad56-112">Указатель на массив структур [FILETIME](filetime.md) , содержащих значения времени.</span><span class="sxs-lookup"><span data-stu-id="8ad56-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8ad56-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="8ad56-113">Remarks</span></span>

<span data-ttu-id="8ad56-114">Дополнительные сведения о PT_MV_SYSTIME увидеть [Список типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="8ad56-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8ad56-115">См. также</span><span class="sxs-lookup"><span data-stu-id="8ad56-115">See also</span></span>



[<span data-ttu-id="8ad56-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="8ad56-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="8ad56-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8ad56-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="8ad56-118">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="8ad56-118">MAPI Structures</span></span>](mapi-structures.md)

