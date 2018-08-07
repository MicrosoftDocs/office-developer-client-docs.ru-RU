---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5cfad1c75aaab9afae47de5798f9e6b7ea530940
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812363"
---
# <a name="sproptagarray"></a><span data-ttu-id="00dd6-103">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="00dd6-103">SPropTagArray</span></span>

  
  
<span data-ttu-id="00dd6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00dd6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00dd6-105">Содержит массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="00dd6-105">Contains an array of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00dd6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="00dd6-106">Header file:</span></span>  <br/> |<span data-ttu-id="00dd6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00dd6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="00dd6-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="00dd6-108">Related macros:</span></span>  <br/> |<span data-ttu-id="00dd6-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md) [SizedSPropTagArray](sizedsproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="00dd6-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a><span data-ttu-id="00dd6-110">Members</span><span class="sxs-lookup"><span data-stu-id="00dd6-110">Members</span></span>

 <span data-ttu-id="00dd6-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="00dd6-111">**cValues**</span></span>
  
> <span data-ttu-id="00dd6-112">Count свойство теги в массиве, указанный в параметре члена **aulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="00dd6-112">Count of property tags in the array indicated by the **aulPropTag** member.</span></span> 
    
 <span data-ttu-id="00dd6-113">**aulPropTag**</span><span class="sxs-lookup"><span data-stu-id="00dd6-113">**aulPropTag**</span></span>
  
> <span data-ttu-id="00dd6-114">Массив, содержащий тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="00dd6-114">Array of property tags.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="00dd6-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="00dd6-115">Remarks</span></span>

<span data-ttu-id="00dd6-116">Свойство tag является целым числом без знака 32-разрядная версия, которая состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="00dd6-116">A property tag is a 32-bit unsigned integer that consists of two parts:</span></span> 
  
- <span data-ttu-id="00dd6-117">Идентификатор в 16 бит высокого приоритета.</span><span class="sxs-lookup"><span data-stu-id="00dd6-117">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="00dd6-118">Тип в 16 бит низкого приоритета.</span><span class="sxs-lookup"><span data-stu-id="00dd6-118">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="00dd6-119">Идентификатор — числовое значение в определенный диапазон.</span><span class="sxs-lookup"><span data-stu-id="00dd6-119">The identifier is a numeric value in a particular range.</span></span> <span data-ttu-id="00dd6-120">Диапазоны идентификаторов для описания, для чего используется свойство и кто несет ответственность за обеспечение его определены MAPI.</span><span class="sxs-lookup"><span data-stu-id="00dd6-120">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="00dd6-121">MAPI определяет ограничения для каждого из тегов свойств, поддерживаемых в файле заголовка Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="00dd6-121">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="00dd6-122">Тип указывает формат, для которых значение свойства.</span><span class="sxs-lookup"><span data-stu-id="00dd6-122">The type indicates the format for the property's value.</span></span> <span data-ttu-id="00dd6-123">MAPI определяет константы для каждого типа свойства, поддерживаемые в файле заголовка Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="00dd6-123">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="00dd6-124">Дополнительные сведения о тегах свойств и их компоненты см.</span><span class="sxs-lookup"><span data-stu-id="00dd6-124">For more information about property tags and their components, see one of the following topics:</span></span> 
  
[<span data-ttu-id="00dd6-125">Теги свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="00dd6-125">MAPI Property Tags</span></span>](mapi-property-tags.md)
  
[<span data-ttu-id="00dd6-126">Обзор свойств идентификатор MAPI</span><span class="sxs-lookup"><span data-stu-id="00dd6-126">MAPI Property Identifier Overview</span></span>](mapi-property-identifier-overview.md)
  
[<span data-ttu-id="00dd6-127">Обзор типов свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="00dd6-127">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)
  
<span data-ttu-id="00dd6-128">Полный список типов одним значением и многозначных свойств содержатся в приложении, [типов и идентификаторы свойств](property-identifiers-and-types.md).</span><span class="sxs-lookup"><span data-stu-id="00dd6-128">For a complete list of the single-valued and multi-valued property types, see the appendix, [Property Identifiers and Types](property-identifiers-and-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00dd6-129">См. также</span><span class="sxs-lookup"><span data-stu-id="00dd6-129">See also</span></span>



[<span data-ttu-id="00dd6-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="00dd6-130">MAPI Structures</span></span>](mapi-structures.md)

