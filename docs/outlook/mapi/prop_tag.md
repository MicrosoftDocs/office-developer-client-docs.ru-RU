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
ms.openlocfilehash: 7ab4e4e9e51849037a91a071f16294cfdf10870c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425885"
---
# <a name="prop_tag"></a><span data-ttu-id="911fb-103">PROP_TAG</span><span class="sxs-lookup"><span data-stu-id="911fb-103">PROP_TAG</span></span>

<span data-ttu-id="911fb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="911fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="911fb-105">Возвращает тег свойства, созданный путем объединения указанного типа свойства и идентификатора.</span><span class="sxs-lookup"><span data-stu-id="911fb-105">Returns a property tag created by combining a specified property type and identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="911fb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="911fb-106">Header file:</span></span>  <br/> |<span data-ttu-id="911fb-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="911fb-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="911fb-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="911fb-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="911fb-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="911fb-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a><span data-ttu-id="911fb-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="911fb-110">Parameters</span></span>

<span data-ttu-id="911fb-111">_улпроптипе_</span><span class="sxs-lookup"><span data-stu-id="911fb-111">_ulPropType_</span></span>
  
> <span data-ttu-id="911fb-112">Тип свойства для нового тега свойства.</span><span class="sxs-lookup"><span data-stu-id="911fb-112">Property type for the new property tag.</span></span>
    
<span data-ttu-id="911fb-113">_улпропид_</span><span class="sxs-lookup"><span data-stu-id="911fb-113">_ulPropID_</span></span>
  
> <span data-ttu-id="911fb-114">Идентификатор свойства для нового тега свойства.</span><span class="sxs-lookup"><span data-stu-id="911fb-114">Property identifier for the new property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="911fb-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="911fb-115">Remarks</span></span>

<span data-ttu-id="911fb-116">Макрос **тега\_Prop** создает тег свойства для свойства типа _улпроптипе_ и идентификатор, указанный в _улпропид_.</span><span class="sxs-lookup"><span data-stu-id="911fb-116">The **PROP\_TAG** macro creates a property tag for a property of type  _ulPropType_ and the identifier that is specified in  _ulPropID_.</span></span> <span data-ttu-id="911fb-117">Например, тег свойства для идентификатора записи можно создать с помощью макроса **PROP_TAG** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="911fb-117">For example, a property tag for an entry identifier can be created by using the **PROP_TAG** macro as follows:</span></span> 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

<span data-ttu-id="911fb-118">Младшие 16 бит возвращаемого тега свойства содержат тип свойства, PT_BINARY, а старшие 16 бит содержат идентификатор свойства, 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="911fb-118">The low-order 16 bits of the returned property tag contain the property type, PT_BINARY, and the high-order 16 bits contain the property identifier, 0xFFFF.</span></span>
  
<span data-ttu-id="911fb-119">Более подробную информацию о тегах свойств можно узнать в статье [теги свойств MAPI](mapi-property-tags.md).</span><span class="sxs-lookup"><span data-stu-id="911fb-119">For more information about property tags, see [MAPI Property Tags](mapi-property-tags.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="911fb-120">См. также</span><span class="sxs-lookup"><span data-stu-id="911fb-120">See also</span></span>

- [<span data-ttu-id="911fb-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="911fb-121">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="911fb-122">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="911fb-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

