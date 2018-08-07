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
ms.openlocfilehash: ad4b9d3f7c2ca1766ecca4fe9467fc49098f2212
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812072"
---
# <a name="propid"></a><span data-ttu-id="2377d-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="2377d-103">PROP_ID</span></span>

  
  
<span data-ttu-id="2377d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2377d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2377d-105">Возвращает идентификатор свойства tag указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="2377d-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2377d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2377d-106">Header file:</span></span>  <br/> |<span data-ttu-id="2377d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2377d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2377d-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="2377d-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="2377d-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2377d-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="2377d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2377d-110">Parameters</span></span>

 <span data-ttu-id="2377d-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="2377d-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="2377d-112">Тег свойства, содержащее идентификатор которого требуется получить.</span><span class="sxs-lookup"><span data-stu-id="2377d-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2377d-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="2377d-113">Remarks</span></span>

<span data-ttu-id="2377d-114">Каждого свойства тега содержит тип свойства в word низкого приоритета (бит 0 до 15) и идентификатор свойства в word высокого приоритета (bits 16 до 31).</span><span class="sxs-lookup"><span data-stu-id="2377d-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="2377d-115">Макрос **PROP_ID** извлекает идентификатор свойства и помещает его в бит 0 до 15 целое число должно быть возвращено.</span><span class="sxs-lookup"><span data-stu-id="2377d-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="2377d-116">Оставшиеся биты возвращаемое значение устанавливаются нули.</span><span class="sxs-lookup"><span data-stu-id="2377d-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="2377d-117">Например, макрос **PROP_ID** можно использовать для получения идентификатора для передачи [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="2377d-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="2377d-118">**GetNamesFromIDs** возвращает имя свойства, связанного с идентификатором для именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="2377d-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2377d-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2377d-119">See also</span></span>



[<span data-ttu-id="2377d-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2377d-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="2377d-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="2377d-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

