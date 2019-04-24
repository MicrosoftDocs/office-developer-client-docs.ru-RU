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
ms.openlocfilehash: 9a5be98298ab1f9333ac1c223a6ef594e60dd86a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344438"
---
# <a name="sproptagarray"></a><span data-ttu-id="989da-103">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="989da-103">SPropTagArray</span></span>

  
  
<span data-ttu-id="989da-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="989da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="989da-105">Содержит массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="989da-105">Contains an array of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="989da-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="989da-106">Header file:</span></span>  <br/> |<span data-ttu-id="989da-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="989da-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="989da-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="989da-108">Related macros:</span></span>  <br/> |<span data-ttu-id="989da-109">[Кбневспроптагаррай](cbnewsproptagarray.md), [кбспроптагаррай](cbsproptagarray.md), [сизедспроптагаррай](sizedsproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="989da-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a><span data-ttu-id="989da-110">Members</span><span class="sxs-lookup"><span data-stu-id="989da-110">Members</span></span>

 <span data-ttu-id="989da-111">**Квалуес**</span><span class="sxs-lookup"><span data-stu-id="989da-111">**cValues**</span></span>
  
> <span data-ttu-id="989da-112">Количество тегов свойств в массиве, указанном элементом **аулпроптаг** .</span><span class="sxs-lookup"><span data-stu-id="989da-112">Count of property tags in the array indicated by the **aulPropTag** member.</span></span> 
    
 <span data-ttu-id="989da-113">**Аулпроптаг**</span><span class="sxs-lookup"><span data-stu-id="989da-113">**aulPropTag**</span></span>
  
> <span data-ttu-id="989da-114">Массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="989da-114">Array of property tags.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="989da-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="989da-115">Remarks</span></span>

<span data-ttu-id="989da-116">Тег свойства — это 32-разрядное целое число без знака, которое состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="989da-116">A property tag is a 32-bit unsigned integer that consists of two parts:</span></span> 
  
- <span data-ttu-id="989da-117">Идентификатор в высоком порядке 16 бит.</span><span class="sxs-lookup"><span data-stu-id="989da-117">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="989da-118">Тип в 16 младших битах.</span><span class="sxs-lookup"><span data-stu-id="989da-118">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="989da-119">Идентификатор — это числовое значение в определенном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="989da-119">The identifier is a numeric value in a particular range.</span></span> <span data-ttu-id="989da-120">MAPI определяет диапазоны для идентификаторов, описывающих, для чего используется свойство и кто отвечает за его обслуживание.</span><span class="sxs-lookup"><span data-stu-id="989da-120">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="989da-121">MAPI определяет ограничения для каждого из тегов свойств, которые он поддерживает, в файле заголовка Мапитагс. h.</span><span class="sxs-lookup"><span data-stu-id="989da-121">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="989da-122">Тип указывает формат значения свойства.</span><span class="sxs-lookup"><span data-stu-id="989da-122">The type indicates the format for the property's value.</span></span> <span data-ttu-id="989da-123">MAPI определяет константы для каждого из типов свойств, поддерживаемых в файле заголовка MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="989da-123">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="989da-124">Для получения дополнительных сведений о тегах свойств и их компонентах см один из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="989da-124">For more information about property tags and their components, see one of the following topics:</span></span> 
  
[<span data-ttu-id="989da-125">Теги свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="989da-125">MAPI Property Tags</span></span>](mapi-property-tags.md)
  
[<span data-ttu-id="989da-126">Обзор идентификаторов свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="989da-126">MAPI Property Identifier Overview</span></span>](mapi-property-identifier-overview.md)
  
[<span data-ttu-id="989da-127">Обзор типов свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="989da-127">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)
  
<span data-ttu-id="989da-128">Полный список типов свойств с одним и несколькими значениями можно посмотреть в приложении, [идентификаторах и типах свойств](property-identifiers-and-types.md).</span><span class="sxs-lookup"><span data-stu-id="989da-128">For a complete list of the single-valued and multi-valued property types, see the appendix, [Property Identifiers and Types](property-identifiers-and-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="989da-129">См. также</span><span class="sxs-lookup"><span data-stu-id="989da-129">See also</span></span>



[<span data-ttu-id="989da-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="989da-130">MAPI Structures</span></span>](mapi-structures.md)

