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
# <a name="pidtagbodycontentlocation-canonical-property"></a><span data-ttu-id="e1761-103">Каноническое свойство PidTagBodyContentLocation</span><span class="sxs-lookup"><span data-stu-id="e1761-103">PidTagBodyContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="e1761-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1761-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1761-105">Содержит значение поля загона содержимого MIME.</span><span class="sxs-lookup"><span data-stu-id="e1761-105">Contains the value of a MIME Content-Location header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1761-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e1761-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1761-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="e1761-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="e1761-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e1761-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1761-109">0x1014</span><span class="sxs-lookup"><span data-stu-id="e1761-109">0x1014</span></span>  <br/> |
|<span data-ttu-id="e1761-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e1761-110">Data type:</span></span>  <br/> |<span data-ttu-id="e1761-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e1761-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e1761-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e1761-112">Area:</span></span>  <br/> |<span data-ttu-id="e1761-113">MIME</span><span class="sxs-lookup"><span data-stu-id="e1761-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1761-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e1761-114">Remarks</span></span>

<span data-ttu-id="e1761-115">Чтобы установить значение этих свойств, клиенты MIME должны записать нужное значение в поле заголовщика content-Location в объекте MIME, соповедуемом с текстом сообщения.</span><span class="sxs-lookup"><span data-stu-id="e1761-115">To set the value of these properties, MIME clients should write the desired value to a Content-Location header field on a MIME entity that maps to a message body.</span></span>
  
<span data-ttu-id="e1761-116">Читатели MIME должны скопировать значение поля загоровка content-Location для такой сущности MIME в значение этих свойств.</span><span class="sxs-lookup"><span data-stu-id="e1761-116">MIME readers should copy the value of a Content-Location header field on such a MIME entity to the value of these properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e1761-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e1761-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1761-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e1761-118">Protocol specifications</span></span>

<span data-ttu-id="e1761-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1761-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1761-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="e1761-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1761-121">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1761-121">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1761-122">Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="e1761-122">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1761-123">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="e1761-123">Header files</span></span>

<span data-ttu-id="e1761-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1761-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1761-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e1761-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1761-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e1761-126">Mapitags.h</span></span>
  
> <span data-ttu-id="e1761-127">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e1761-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1761-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e1761-128">See also</span></span>



[<span data-ttu-id="e1761-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e1761-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1761-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e1761-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1761-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e1761-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1761-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e1761-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

