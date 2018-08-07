---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 834a7141f0e7150140fa27c21d88db422d6f5561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812171"
---
# <a name="sapptimearray"></a><span data-ttu-id="e61d9-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="e61d9-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="e61d9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e61d9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e61d9-105">Содержит массив значений времени.</span><span class="sxs-lookup"><span data-stu-id="e61d9-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e61d9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e61d9-106">Header file:</span></span>  <br/> |<span data-ttu-id="e61d9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e61d9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="e61d9-108">Members</span><span class="sxs-lookup"><span data-stu-id="e61d9-108">Members</span></span>

 <span data-ttu-id="e61d9-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="e61d9-109">**cValues**</span></span>
  
> <span data-ttu-id="e61d9-110">Число значений в массиве, на который указывает член **lpat** .</span><span class="sxs-lookup"><span data-stu-id="e61d9-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="e61d9-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="e61d9-111">**lpat**</span></span>
  
> <span data-ttu-id="e61d9-112">Указатель на массив значений времени приложения.</span><span class="sxs-lookup"><span data-stu-id="e61d9-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e61d9-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="e61d9-113">Remarks</span></span>

<span data-ttu-id="e61d9-114">Структура **SAppTimeArray** используется для определения свойства типа PT_MV_APPTIME.</span><span class="sxs-lookup"><span data-stu-id="e61d9-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="e61d9-115">Дополнительные сведения о PT_MV_APPTIME увидеть [Список типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="e61d9-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e61d9-116">См. также</span><span class="sxs-lookup"><span data-stu-id="e61d9-116">See also</span></span>



[<span data-ttu-id="e61d9-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="e61d9-117">MAPI Structures</span></span>](mapi-structures.md)

