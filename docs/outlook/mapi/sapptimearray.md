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
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430387"
---
# <a name="sapptimearray"></a><span data-ttu-id="6b16e-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="6b16e-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="6b16e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b16e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b16e-105">Содержит массив значений времени.</span><span class="sxs-lookup"><span data-stu-id="6b16e-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6b16e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6b16e-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b16e-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="6b16e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="6b16e-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="6b16e-108">Members</span></span>

 <span data-ttu-id="6b16e-109">**квалуес**</span><span class="sxs-lookup"><span data-stu-id="6b16e-109">**cValues**</span></span>
  
> <span data-ttu-id="6b16e-110">Количество значений в массиве, на которое указывает элемент **лпат** .</span><span class="sxs-lookup"><span data-stu-id="6b16e-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="6b16e-111">**лпат**</span><span class="sxs-lookup"><span data-stu-id="6b16e-111">**lpat**</span></span>
  
> <span data-ttu-id="6b16e-112">Указатель на массив значений времени приложения.</span><span class="sxs-lookup"><span data-stu-id="6b16e-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6b16e-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="6b16e-113">Remarks</span></span>

<span data-ttu-id="6b16e-114">Структура **сапптимеаррай** используется для определения свойств типа PT_MV_APPTIME.</span><span class="sxs-lookup"><span data-stu-id="6b16e-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="6b16e-115">Дополнительные сведения о PT_MV_APPTIME приведены в разделе [список типов свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="6b16e-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6b16e-116">См. также</span><span class="sxs-lookup"><span data-stu-id="6b16e-116">See also</span></span>



[<span data-ttu-id="6b16e-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="6b16e-117">MAPI Structures</span></span>](mapi-structures.md)

