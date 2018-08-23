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
ms.openlocfilehash: 4b10daf3bdc11d406b6f7248fd6aaa9e3c6c2a68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584718"
---
# <a name="pidtagbodycontentlocation-canonical-property"></a><span data-ttu-id="38a79-103">Каноническое свойство PidTagBodyContentLocation</span><span class="sxs-lookup"><span data-stu-id="38a79-103">PidTagBodyContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="38a79-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38a79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38a79-105">Содержит значение поля заголовка MIME Content-Location.</span><span class="sxs-lookup"><span data-stu-id="38a79-105">Contains the value of a MIME Content-Location header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38a79-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="38a79-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38a79-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="38a79-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="38a79-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="38a79-108">Identifier:</span></span>  <br/> |<span data-ttu-id="38a79-109">0x1014</span><span class="sxs-lookup"><span data-stu-id="38a79-109">0x1014</span></span>  <br/> |
|<span data-ttu-id="38a79-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="38a79-110">Data type:</span></span>  <br/> |<span data-ttu-id="38a79-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="38a79-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="38a79-112">Область:</span><span class="sxs-lookup"><span data-stu-id="38a79-112">Area:</span></span>  <br/> |<span data-ttu-id="38a79-113">MIME</span><span class="sxs-lookup"><span data-stu-id="38a79-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38a79-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="38a79-114">Remarks</span></span>

<span data-ttu-id="38a79-115">Чтобы задать значения этих свойств, MIME клиентов указывайте нужное значение в поле Заголовок Content-Location в сущности MIME, которая сопоставлена с текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="38a79-115">To set the value of these properties, MIME clients should write the desired value to a Content-Location header field on a MIME entity that maps to a message body.</span></span>
  
<span data-ttu-id="38a79-116">Читатели MIME следует скопировать значение в поле Заголовок Content-Location в сущности MIME значения этих свойств.</span><span class="sxs-lookup"><span data-stu-id="38a79-116">MIME readers should copy the value of a Content-Location header field on such a MIME entity to the value of these properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="38a79-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="38a79-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38a79-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="38a79-118">Protocol specifications</span></span>

<span data-ttu-id="38a79-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38a79-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38a79-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="38a79-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="38a79-121">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38a79-121">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38a79-122">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="38a79-122">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38a79-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="38a79-123">Header files</span></span>

<span data-ttu-id="38a79-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38a79-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="38a79-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="38a79-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="38a79-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="38a79-126">Mapitags.h</span></span>
  
> <span data-ttu-id="38a79-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="38a79-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38a79-128">См. также</span><span class="sxs-lookup"><span data-stu-id="38a79-128">See also</span></span>



[<span data-ttu-id="38a79-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="38a79-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38a79-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="38a79-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38a79-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="38a79-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38a79-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="38a79-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

