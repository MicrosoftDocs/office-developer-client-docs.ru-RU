---
title: Каноническое свойство PidTagOriginalAuthorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorNam
api_type:
- COM
ms.assetid: beb23742-d844-4d90-9b13-1ad376d4206c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bb62f3a44c9f17070db969683891fb2e2d62eb5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355778"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a><span data-ttu-id="d9d7a-103">Каноническое свойство PidTagOriginalAuthorName</span><span class="sxs-lookup"><span data-stu-id="d9d7a-103">PidTagOriginalAuthorName Canonical Property</span></span>

  
  
<span data-ttu-id="d9d7a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9d7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9d7a-105">Содержит отображаемое имя автора первой версии сообщения, то есть сообщение перед пересылкой или ответом.</span><span class="sxs-lookup"><span data-stu-id="d9d7a-105">Contains the display name of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9d7a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d9d7a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9d7a-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A PR_ORIGINAL_AUTHOR_NAME_W</span><span class="sxs-lookup"><span data-stu-id="d9d7a-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span></span>  <br/> |
|<span data-ttu-id="d9d7a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d9d7a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9d7a-109">0x004D</span><span class="sxs-lookup"><span data-stu-id="d9d7a-109">0x004D</span></span>  <br/> |
|<span data-ttu-id="d9d7a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d9d7a-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9d7a-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="d9d7a-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="d9d7a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d9d7a-112">Area:</span></span>  <br/> |<span data-ttu-id="d9d7a-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="d9d7a-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9d7a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d9d7a-114">Remarks</span></span>

<span data-ttu-id="d9d7a-115">Эти свойства являются примерами свойств адреса для автора сообщения.</span><span class="sxs-lookup"><span data-stu-id="d9d7a-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="d9d7a-116">При первой отправке сообщения клиентскому приложению следует задать для этих свойств значение **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d9d7a-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span></span> <span data-ttu-id="d9d7a-117">Он никогда не изменяется при пересылке сообщения или ответе на него.</span><span class="sxs-lookup"><span data-stu-id="d9d7a-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="d9d7a-118">Исходные свойства автора допускают сохранение данных извне локального домена обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d9d7a-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="d9d7a-119">Когда сообщение поступает из другого домена обмена сообщениями (например, из Интернета), эти свойства предоставляют способ гарантировать, что исходные данные не будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="d9d7a-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d9d7a-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d9d7a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9d7a-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d9d7a-121">Protocol specifications</span></span>

<span data-ttu-id="d9d7a-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9d7a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9d7a-123">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d9d7a-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d9d7a-124">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9d7a-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9d7a-125">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="d9d7a-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9d7a-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d9d7a-126">Header files</span></span>

<span data-ttu-id="d9d7a-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d9d7a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9d7a-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d9d7a-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9d7a-129">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="d9d7a-129">Mapitags.h</span></span>
  
> <span data-ttu-id="d9d7a-130">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="d9d7a-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9d7a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="d9d7a-131">See also</span></span>



[<span data-ttu-id="d9d7a-132">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="d9d7a-132">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="d9d7a-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d9d7a-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9d7a-134">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="d9d7a-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9d7a-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d9d7a-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9d7a-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d9d7a-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

