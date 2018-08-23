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
ms.openlocfilehash: 7bcaf230eed9cf21388b68f06ab678dc143f64ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571824"
---
# <a name="proptype"></a><span data-ttu-id="68014-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="68014-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="68014-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68014-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68014-105">Возвращает тип свойства тега указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="68014-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68014-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="68014-106">Header file:</span></span>  <br/> |<span data-ttu-id="68014-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="68014-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="68014-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="68014-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="68014-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="68014-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="68014-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="68014-110">Parameters</span></span>

 <span data-ttu-id="68014-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="68014-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="68014-112">Свойство tag, которая содержит тип свойства которого требуется получить.</span><span class="sxs-lookup"><span data-stu-id="68014-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68014-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="68014-113">Remarks</span></span>

<span data-ttu-id="68014-114">Макрос **PROP_TYPE** можно использовать для определения типа свойства.</span><span class="sxs-lookup"><span data-stu-id="68014-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="68014-115">Например вызов результаты PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) в значении PT_BINARY, возвращаемых.</span><span class="sxs-lookup"><span data-stu-id="68014-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="68014-116">Каждого свойства тега содержит тип свойства в word низкого приоритета (бит 0 до 15) и идентификатор свойства в word высокого приоритета (bits 16 до 31).</span><span class="sxs-lookup"><span data-stu-id="68014-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="68014-117">Макрос **PROP_TYPE** извлекает тип свойства и помещает его в бит 0 до 15 целое число должно быть возвращено.</span><span class="sxs-lookup"><span data-stu-id="68014-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="68014-118">Оставшиеся биты возвращаемое значение устанавливаются нули.</span><span class="sxs-lookup"><span data-stu-id="68014-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="68014-119">См. также</span><span class="sxs-lookup"><span data-stu-id="68014-119">See also</span></span>



[<span data-ttu-id="68014-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="68014-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="68014-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="68014-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

