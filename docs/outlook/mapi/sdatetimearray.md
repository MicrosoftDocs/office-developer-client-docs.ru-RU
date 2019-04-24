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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339797"
---
# <a name="sdatetimearray"></a><span data-ttu-id="c0c09-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="c0c09-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="c0c09-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0c09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0c09-105">Содержит массив значений времени, которые используются для описания свойства типа ПТ_МВ_СИСТИМЕ.</span><span class="sxs-lookup"><span data-stu-id="c0c09-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0c09-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c0c09-106">Header file:</span></span>  <br/> |<span data-ttu-id="c0c09-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c0c09-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="c0c09-108">Members</span><span class="sxs-lookup"><span data-stu-id="c0c09-108">Members</span></span>

 <span data-ttu-id="c0c09-109">**Квалуес**</span><span class="sxs-lookup"><span data-stu-id="c0c09-109">**cValues**</span></span>
  
> <span data-ttu-id="c0c09-110">Количество значений в массиве, на которое указывает элемент **лпфт** .</span><span class="sxs-lookup"><span data-stu-id="c0c09-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="c0c09-111">**лпфт**</span><span class="sxs-lookup"><span data-stu-id="c0c09-111">**lpft**</span></span>
  
> <span data-ttu-id="c0c09-112">Указатель на массив структуры [fileTime](filetime.md) , который содержит значения времени.</span><span class="sxs-lookup"><span data-stu-id="c0c09-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c0c09-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0c09-113">Remarks</span></span>

<span data-ttu-id="c0c09-114">Дополнительные сведения о ПТ_МВ_СИСТИМЕ приведены в разделе [список типов свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="c0c09-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0c09-115">См. также</span><span class="sxs-lookup"><span data-stu-id="c0c09-115">See also</span></span>



[<span data-ttu-id="c0c09-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="c0c09-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="c0c09-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c0c09-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="c0c09-118">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="c0c09-118">MAPI Structures</span></span>](mapi-structures.md)

