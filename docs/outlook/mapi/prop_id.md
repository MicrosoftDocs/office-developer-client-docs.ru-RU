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
ms.openlocfilehash: 228ea91969b35a1608dd6b3378b751312aa9c665
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409134"
---
# <a name="prop_id"></a><span data-ttu-id="7ef33-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="7ef33-103">PROP_ID</span></span>

  
  
<span data-ttu-id="7ef33-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ef33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ef33-105">Возвращает идентификатор указанного тега свойства.</span><span class="sxs-lookup"><span data-stu-id="7ef33-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7ef33-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7ef33-106">Header file:</span></span>  <br/> |<span data-ttu-id="7ef33-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7ef33-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7ef33-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="7ef33-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="7ef33-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7ef33-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="7ef33-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ef33-110">Parameters</span></span>

 <span data-ttu-id="7ef33-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="7ef33-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="7ef33-112">Тег свойства, содержащий возвращаемую идентификатор.</span><span class="sxs-lookup"><span data-stu-id="7ef33-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ef33-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ef33-113">Remarks</span></span>

<span data-ttu-id="7ef33-114">Каждый тег свойства содержит тип свойства в слове низкого порядка (биты от 0 до 15) и идентификатор свойства в слове высокого порядка (биты от 16 до 31).</span><span class="sxs-lookup"><span data-stu-id="7ef33-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="7ef33-115">Макрос **PROP_ID** извлекает идентификатор свойства и помещает его в биты от 0 до 15 возвращаемого integer.</span><span class="sxs-lookup"><span data-stu-id="7ef33-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="7ef33-116">Оставшиеся биты возвращаемого значения имеют нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7ef33-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="7ef33-117">Макрос **PROP_ID** можно использовать, например, для получения идентификатора, передав его в [IMAPIProp::GetNamesFromIDs.](imapiprop-getnamesfromids.md)</span><span class="sxs-lookup"><span data-stu-id="7ef33-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="7ef33-118">**GetNamesFromIDs** извлекает имя свойства, связанное с идентификатором именоваемой свойства.</span><span class="sxs-lookup"><span data-stu-id="7ef33-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7ef33-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7ef33-119">See also</span></span>



[<span data-ttu-id="7ef33-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7ef33-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7ef33-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="7ef33-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

