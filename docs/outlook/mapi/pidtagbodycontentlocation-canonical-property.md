---
title: Каноническое свойство PidTagBodyContentLocation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyContentLocation
api_type:
- HeaderDef
ms.assetid: a66d1c64-5c5a-4980-9acd-72448108fd2c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 90a873174b5b990f165d0b2173efa38fc7df2d9d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350941"
---
# <a name="pidtagbodycontentlocation-canonical-property"></a><span data-ttu-id="c5163-103">Каноническое свойство PidTagBodyContentLocation</span><span class="sxs-lookup"><span data-stu-id="c5163-103">PidTagBodyContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="c5163-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5163-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5163-105">Содержит значение поля заголовка Content – Location (расположение MIME).</span><span class="sxs-lookup"><span data-stu-id="c5163-105">Contains the value of a MIME Content-Location header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5163-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c5163-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5163-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A PR_BODY_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="c5163-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="c5163-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c5163-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c5163-109">0x1014</span><span class="sxs-lookup"><span data-stu-id="c5163-109">0x1014</span></span>  <br/> |
|<span data-ttu-id="c5163-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c5163-110">Data type:</span></span>  <br/> |<span data-ttu-id="c5163-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c5163-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c5163-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c5163-112">Area:</span></span>  <br/> |<span data-ttu-id="c5163-113">MIME</span><span class="sxs-lookup"><span data-stu-id="c5163-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5163-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5163-114">Remarks</span></span>

<span data-ttu-id="c5163-115">Чтобы задать значение этих свойств, клиенты MIME должны записать нужное значение в поле заголовка Content – Location в объекте MIME, который сопоставляется с текстом сообщения.</span><span class="sxs-lookup"><span data-stu-id="c5163-115">To set the value of these properties, MIME clients should write the desired value to a Content-Location header field on a MIME entity that maps to a message body.</span></span>
  
<span data-ttu-id="c5163-116">Считыватели MIME должны скопировать значение поля заголовка Content – Location в такой сущности MIME в значение этих свойств.</span><span class="sxs-lookup"><span data-stu-id="c5163-116">MIME readers should copy the value of a Content-Location header field on such a MIME entity to the value of these properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c5163-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c5163-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c5163-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c5163-118">Protocol specifications</span></span>

<span data-ttu-id="c5163-119">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5163-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5163-120">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c5163-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c5163-121">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5163-121">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5163-122">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="c5163-122">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c5163-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c5163-123">Header files</span></span>

<span data-ttu-id="c5163-124">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c5163-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5163-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c5163-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="c5163-126">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="c5163-126">Mapitags.h</span></span>
  
> <span data-ttu-id="c5163-127">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="c5163-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5163-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c5163-128">See also</span></span>



[<span data-ttu-id="c5163-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c5163-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5163-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="c5163-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5163-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c5163-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5163-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c5163-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

