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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328576"
---
# <a name="propid"></a><span data-ttu-id="998b3-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="998b3-103">PROP_ID</span></span>

  
  
<span data-ttu-id="998b3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="998b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="998b3-105">Возвращает идентификатор свойства указанного тега свойства.</span><span class="sxs-lookup"><span data-stu-id="998b3-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="998b3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="998b3-106">Header file:</span></span>  <br/> |<span data-ttu-id="998b3-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="998b3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="998b3-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="998b3-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="998b3-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="998b3-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="998b3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="998b3-110">Parameters</span></span>

 <span data-ttu-id="998b3-111">_Улпроптаг_</span><span class="sxs-lookup"><span data-stu-id="998b3-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="998b3-112">Тег свойства, который содержит возвращаемый идентификатор.</span><span class="sxs-lookup"><span data-stu-id="998b3-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="998b3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="998b3-113">Remarks</span></span>

<span data-ttu-id="998b3-114">Каждый тег Property содержит тип свойства в младших словах (в битах от 0 до 15) и идентификатор свойства в высоком уровне (биты от 16 до 31).</span><span class="sxs-lookup"><span data-stu-id="998b3-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="998b3-115">Макрос **проп_ид** извлекает идентификатор свойства и преобразует его в двоичные значения, возвращаемые в битах от 0 до 15.</span><span class="sxs-lookup"><span data-stu-id="998b3-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="998b3-116">Остальные биты возвращаемого значения задаются нулевыми.</span><span class="sxs-lookup"><span data-stu-id="998b3-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="998b3-117">Макрос **проп_ид** можно использовать, например, для извлечения идентификатора, который передается в [IMAPIProp:: жетнамесфромидс](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="998b3-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="998b3-118">**Жетнамесфромидс** получает имя свойства, связанного с идентификатором именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="998b3-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="998b3-119">См. также</span><span class="sxs-lookup"><span data-stu-id="998b3-119">See also</span></span>



[<span data-ttu-id="998b3-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="998b3-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="998b3-121">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="998b3-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

