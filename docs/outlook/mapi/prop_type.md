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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412837"
---
# <a name="prop_type"></a><span data-ttu-id="c7f7b-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="c7f7b-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="c7f7b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7f7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7f7b-105">Возвращает тип свойства указанного тега свойства.</span><span class="sxs-lookup"><span data-stu-id="c7f7b-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c7f7b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c7f7b-106">Header file:</span></span>  <br/> |<span data-ttu-id="c7f7b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7f7b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c7f7b-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="c7f7b-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="c7f7b-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c7f7b-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="c7f7b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7f7b-110">Parameters</span></span>

 <span data-ttu-id="c7f7b-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="c7f7b-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="c7f7b-112">Тег свойства, содержащий возвращаемого типа свойства.</span><span class="sxs-lookup"><span data-stu-id="c7f7b-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7f7b-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="c7f7b-113">Remarks</span></span>

<span data-ttu-id="c7f7b-114">Макрос **PROP_TYPE** можно использовать для определения типа свойства.</span><span class="sxs-lookup"><span data-stu-id="c7f7b-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="c7f7b-115">Например, вызов PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) приводит к PT_BINARY возвращаемой.</span><span class="sxs-lookup"><span data-stu-id="c7f7b-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="c7f7b-116">Каждый тег свойства содержит тип свойства в слове низкого порядка (биты от 0 до 15) и идентификатор свойства в слове высокого порядка (биты от 16 до 31).</span><span class="sxs-lookup"><span data-stu-id="c7f7b-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="c7f7b-117">Макрос **PROP_TYPE** извлекает тип свойства и помещает его в биты от 0 до 15 возвращаемого integer.</span><span class="sxs-lookup"><span data-stu-id="c7f7b-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="c7f7b-118">Оставшиеся биты возвращаемого значения имеют нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="c7f7b-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7f7b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c7f7b-119">See also</span></span>



[<span data-ttu-id="c7f7b-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c7f7b-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="c7f7b-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="c7f7b-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

