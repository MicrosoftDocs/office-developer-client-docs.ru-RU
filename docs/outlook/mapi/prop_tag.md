---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cbead0a9953ae5106e1fcc7d07d965d4dc7bacb9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570991"
---
# <a name="proptag"></a><span data-ttu-id="639d1-103">PROP_TAG</span><span class="sxs-lookup"><span data-stu-id="639d1-103">PROP_TAG</span></span>

<span data-ttu-id="639d1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="639d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="639d1-105">Возвращает свойство тег, созданные путем объединения тип указанного свойства и идентификатор.</span><span class="sxs-lookup"><span data-stu-id="639d1-105">Returns a property tag created by combining a specified property type and identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="639d1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="639d1-106">Header file:</span></span>  <br/> |<span data-ttu-id="639d1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="639d1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="639d1-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="639d1-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="639d1-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="639d1-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a><span data-ttu-id="639d1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="639d1-110">Parameters</span></span>

<span data-ttu-id="639d1-111">_ulPropType_</span><span class="sxs-lookup"><span data-stu-id="639d1-111">_ulPropType_</span></span>
  
> <span data-ttu-id="639d1-112">Тип свойства для нового свойства тега.</span><span class="sxs-lookup"><span data-stu-id="639d1-112">Property type for the new property tag.</span></span>
    
<span data-ttu-id="639d1-113">_ulPropID_</span><span class="sxs-lookup"><span data-stu-id="639d1-113">_ulPropID_</span></span>
  
> <span data-ttu-id="639d1-114">Идентификатор свойства для нового свойства тега.</span><span class="sxs-lookup"><span data-stu-id="639d1-114">Property identifier for the new property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="639d1-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="639d1-115">Remarks</span></span>

<span data-ttu-id="639d1-116">**Свойства\_ТЕГА** макрос создает тег свойства для свойства типа _ulPropType_ и идентификатор, который указан в _ulPropID_.</span><span class="sxs-lookup"><span data-stu-id="639d1-116">The **PROP\_TAG** macro creates a property tag for a property of type  _ulPropType_ and the identifier that is specified in  _ulPropID_.</span></span> <span data-ttu-id="639d1-117">Например тег свойства для идентификатора записи могут создаваться с помощью макроса **PROP_TAG** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="639d1-117">For example, a property tag for an entry identifier can be created by using the **PROP_TAG** macro as follows:</span></span> 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

<span data-ttu-id="639d1-118">16 бит низкого приоритета возвращаемого свойства тега содержит тип свойства, PT_BINARY, и старшие 16 бит содержит идентификатор свойства 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="639d1-118">The low-order 16 bits of the returned property tag contain the property type, PT_BINARY, and the high-order 16 bits contain the property identifier, 0xFFFF.</span></span>
  
<span data-ttu-id="639d1-119">Дополнительные сведения о тегах свойств можно [Тегов свойств MAPI](mapi-property-tags.md).</span><span class="sxs-lookup"><span data-stu-id="639d1-119">For more information about property tags, see [MAPI Property Tags](mapi-property-tags.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="639d1-120">См. также</span><span class="sxs-lookup"><span data-stu-id="639d1-120">See also</span></span>

- [<span data-ttu-id="639d1-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="639d1-121">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="639d1-122">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="639d1-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

