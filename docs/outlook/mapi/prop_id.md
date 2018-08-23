---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e1846b4be93bf6300ea89a9ae3133fbba82b344e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573126"
---
# <a name="propid"></a><span data-ttu-id="6e5a5-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="6e5a5-103">PROP_ID</span></span>

  
  
<span data-ttu-id="6e5a5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e5a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e5a5-105">Возвращает идентификатор свойства tag указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e5a5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6e5a5-106">Header file:</span></span>  <br/> |<span data-ttu-id="6e5a5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e5a5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6e5a5-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="6e5a5-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="6e5a5-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="6e5a5-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="6e5a5-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e5a5-110">Parameters</span></span>

 <span data-ttu-id="6e5a5-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="6e5a5-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="6e5a5-112">Тег свойства, содержащее идентификатор которого требуется получить.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e5a5-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="6e5a5-113">Remarks</span></span>

<span data-ttu-id="6e5a5-114">Каждого свойства тега содержит тип свойства в word низкого приоритета (бит 0 до 15) и идентификатор свойства в word высокого приоритета (bits 16 до 31).</span><span class="sxs-lookup"><span data-stu-id="6e5a5-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="6e5a5-115">Макрос **PROP_ID** извлекает идентификатор свойства и помещает его в бит 0 до 15 целое число должно быть возвращено.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="6e5a5-116">Оставшиеся биты возвращаемое значение устанавливаются нули.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="6e5a5-117">Например, макрос **PROP_ID** можно использовать для получения идентификатора для передачи [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="6e5a5-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="6e5a5-118">**GetNamesFromIDs** возвращает имя свойства, связанного с идентификатором для именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="6e5a5-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6e5a5-119">См. также</span><span class="sxs-lookup"><span data-stu-id="6e5a5-119">See also</span></span>



[<span data-ttu-id="6e5a5-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="6e5a5-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="6e5a5-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="6e5a5-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

