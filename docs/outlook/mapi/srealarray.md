---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8439d6609ebece75699a1150a9d0c1a41277fd52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344382"
---
# <a name="srealarray"></a><span data-ttu-id="4630f-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="4630f-103">SRealArray</span></span>

  
  
<span data-ttu-id="4630f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4630f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4630f-105">Содержит массив значений float, которые используются для описания свойства типа PT_MV_R4.</span><span class="sxs-lookup"><span data-stu-id="4630f-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4630f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4630f-106">Header file:</span></span>  <br/> |<span data-ttu-id="4630f-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="4630f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="4630f-108">Members</span><span class="sxs-lookup"><span data-stu-id="4630f-108">Members</span></span>

 <span data-ttu-id="4630f-109">**Квалуес**</span><span class="sxs-lookup"><span data-stu-id="4630f-109">**cValues**</span></span>
  
> <span data-ttu-id="4630f-110">Количество значений в массиве, на которое указывает элемент **лпфлт** .</span><span class="sxs-lookup"><span data-stu-id="4630f-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="4630f-111">**лпфлт**</span><span class="sxs-lookup"><span data-stu-id="4630f-111">**lpflt**</span></span>
  
> <span data-ttu-id="4630f-112">Указатель на массив значений с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4630f-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4630f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4630f-113">Remarks</span></span>

<span data-ttu-id="4630f-114">Более подробную информацию о типе свойства PT_MV_R4 можно узнать в статье [типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="4630f-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4630f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="4630f-115">See also</span></span>



[<span data-ttu-id="4630f-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4630f-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="4630f-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="4630f-117">MAPI Structures</span></span>](mapi-structures.md)

