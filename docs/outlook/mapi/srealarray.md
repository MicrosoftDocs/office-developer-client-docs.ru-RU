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
ms.openlocfilehash: c64e9a7497a70ea34dc09a5749dd281a24f9413d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812369"
---
# <a name="srealarray"></a><span data-ttu-id="25824-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="25824-103">SRealArray</span></span>

  
  
<span data-ttu-id="25824-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25824-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25824-105">Содержит массив значений с плавающей запятой, которые используются для описания свойства типа PT_MV_R4.</span><span class="sxs-lookup"><span data-stu-id="25824-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25824-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="25824-106">Header file:</span></span>  <br/> |<span data-ttu-id="25824-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25824-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="25824-108">Members</span><span class="sxs-lookup"><span data-stu-id="25824-108">Members</span></span>

 <span data-ttu-id="25824-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="25824-109">**cValues**</span></span>
  
> <span data-ttu-id="25824-110">Число значений в массиве, на который указывает член **lpflt** .</span><span class="sxs-lookup"><span data-stu-id="25824-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="25824-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="25824-111">**lpflt**</span></span>
  
> <span data-ttu-id="25824-112">Указатель на массив значений с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="25824-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="25824-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="25824-113">Remarks</span></span>

<span data-ttu-id="25824-114">Дополнительные сведения о типе свойства PT_MV_R4 можно [Типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="25824-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="25824-115">См. также</span><span class="sxs-lookup"><span data-stu-id="25824-115">See also</span></span>



[<span data-ttu-id="25824-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="25824-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="25824-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="25824-117">MAPI Structures</span></span>](mapi-structures.md)

