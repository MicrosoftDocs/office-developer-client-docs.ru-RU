---
title: Каноническое свойство PidTagOriginalAuthorAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorAddressType
api_type:
- COM
ms.assetid: 7cdedb1a-e441-469b-be50-2f18203eb30d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 596e416624fb6f2bf1fdaef64c2179feb7787815
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356219"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a><span data-ttu-id="98298-103">Каноническое свойство PidTagOriginalAuthorAddressType</span><span class="sxs-lookup"><span data-stu-id="98298-103">PidTagOriginalAuthorAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="98298-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98298-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98298-105">Содержит тип адреса автора первой версии сообщения, то есть сообщение перед пересылкой или ответом.</span><span class="sxs-lookup"><span data-stu-id="98298-105">Contains the address type of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98298-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="98298-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98298-107">ПР_ОРИГИНАЛ_АУСОР_АДДРТИПЕ, ПР_ОРИГИНАЛ_АУСОР_АДДРТИПЕ_А, ПР_ОРИГИНАЛ_АУСОР_АДДРТИПЕ_В</span><span class="sxs-lookup"><span data-stu-id="98298-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="98298-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="98298-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98298-109">0x0079</span><span class="sxs-lookup"><span data-stu-id="98298-109">0x0079</span></span>  <br/> |
|<span data-ttu-id="98298-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="98298-110">Data type:</span></span>  <br/> |<span data-ttu-id="98298-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="98298-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="98298-112">Область:</span><span class="sxs-lookup"><span data-stu-id="98298-112">Area:</span></span>  <br/> |<span data-ttu-id="98298-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="98298-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98298-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="98298-114">Remarks</span></span>

<span data-ttu-id="98298-115">Эти свойства являются примерами свойств адреса для автора сообщения.</span><span class="sxs-lookup"><span data-stu-id="98298-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="98298-116">При первой отправке сообщения клиентскому приложению следует задать для этого свойства значение свойства **пр_сендер_аддртипе** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="98298-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="98298-117">Он никогда не изменяется при пересылке сообщения или ответе на него.</span><span class="sxs-lookup"><span data-stu-id="98298-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="98298-118">Исходные свойства автора допускают сохранение данных извне локального домена обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="98298-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="98298-119">Когда сообщение поступает из другого домена обмена сообщениями (например, из Интернета), эти свойства предоставляют способ гарантировать, что исходные данные не будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="98298-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="98298-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="98298-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="98298-121">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="98298-121">Header files</span></span>

<span data-ttu-id="98298-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="98298-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="98298-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="98298-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="98298-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="98298-124">Mapitags.h</span></span>
  
> <span data-ttu-id="98298-125">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="98298-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98298-126">См. также</span><span class="sxs-lookup"><span data-stu-id="98298-126">See also</span></span>



[<span data-ttu-id="98298-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="98298-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98298-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="98298-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98298-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="98298-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98298-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="98298-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

