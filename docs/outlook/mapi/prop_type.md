---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332762"
---
# <a name="proptype"></a><span data-ttu-id="55bbc-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="55bbc-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="55bbc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55bbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55bbc-105">Возвращает тип свойства указанного тега свойства.</span><span class="sxs-lookup"><span data-stu-id="55bbc-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55bbc-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="55bbc-106">Header file:</span></span>  <br/> |<span data-ttu-id="55bbc-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="55bbc-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="55bbc-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="55bbc-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="55bbc-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="55bbc-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="55bbc-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="55bbc-110">Parameters</span></span>

 <span data-ttu-id="55bbc-111">_Улпроптаг_</span><span class="sxs-lookup"><span data-stu-id="55bbc-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="55bbc-112">Тег свойства, который содержит возвращаемый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="55bbc-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="55bbc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55bbc-113">Remarks</span></span>

<span data-ttu-id="55bbc-114">Макрос **проп_типе** можно использовать для определения типа свойства.</span><span class="sxs-lookup"><span data-stu-id="55bbc-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="55bbc-115">Например, вызов ПРОП_ТИПЕ (\*\*пр_ентрид\*\* ([PidTagEntryId](pidtagentryid-canonical-property.md))) приводит к возврату значения пт_бинари.</span><span class="sxs-lookup"><span data-stu-id="55bbc-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="55bbc-116">Каждый тег Property содержит тип свойства в младших словах (в битах от 0 до 15) и идентификатор свойства в высоком уровне (биты от 16 до 31).</span><span class="sxs-lookup"><span data-stu-id="55bbc-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="55bbc-117">Макрос **проп_типе** Извлекает тип свойства и преобразует его в двоичные значения, возвращаемые в битах от 0 до 15.</span><span class="sxs-lookup"><span data-stu-id="55bbc-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="55bbc-118">Остальные биты возвращаемого значения задаются нулевыми.</span><span class="sxs-lookup"><span data-stu-id="55bbc-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="55bbc-119">См. также</span><span class="sxs-lookup"><span data-stu-id="55bbc-119">See also</span></span>



[<span data-ttu-id="55bbc-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="55bbc-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="55bbc-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="55bbc-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

