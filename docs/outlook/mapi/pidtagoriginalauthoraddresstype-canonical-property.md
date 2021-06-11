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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431416"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a><span data-ttu-id="932b3-103">Каноническое свойство PidTagOriginalAuthorAddressType</span><span class="sxs-lookup"><span data-stu-id="932b3-103">PidTagOriginalAuthorAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="932b3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="932b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="932b3-105">Содержит тип адреса автора первой версии сообщения, то есть сообщение перед его переададрением или ответом.</span><span class="sxs-lookup"><span data-stu-id="932b3-105">Contains the address type of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="932b3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="932b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="932b3-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="932b3-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="932b3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="932b3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="932b3-109">0x0079</span><span class="sxs-lookup"><span data-stu-id="932b3-109">0x0079</span></span>  <br/> |
|<span data-ttu-id="932b3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="932b3-110">Data type:</span></span>  <br/> |<span data-ttu-id="932b3-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="932b3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="932b3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="932b3-112">Area:</span></span>  <br/> |<span data-ttu-id="932b3-113">Server</span><span class="sxs-lookup"><span data-stu-id="932b3-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="932b3-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="932b3-114">Remarks</span></span>

<span data-ttu-id="932b3-115">Эти свойства являются примерами свойств адресов для автора сообщения.</span><span class="sxs-lookup"><span data-stu-id="932b3-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="932b3-116">При первой отправке сообщения клиентская заявка должна установить это свойство к значению **свойства PR_SENDER_ADDRTYPE** [(PidTagSenderAddressType).](pidtagsenderaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="932b3-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="932b3-117">Он никогда не меняется, когда сообщение переададовыв или отвечает на него.</span><span class="sxs-lookup"><span data-stu-id="932b3-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="932b3-118">Исходные свойства автора позволяют сохранить сведения из локального домена обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="932b3-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="932b3-119">Когда сообщение поступает из другого домена обмена сообщениями, например из Интернета, эти свойства предоставляют способ убедиться, что исходные сведения не будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="932b3-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="932b3-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="932b3-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="932b3-121">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="932b3-121">Header files</span></span>

<span data-ttu-id="932b3-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="932b3-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="932b3-123">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="932b3-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="932b3-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="932b3-124">Mapitags.h</span></span>
  
> <span data-ttu-id="932b3-125">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="932b3-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="932b3-126">См. также</span><span class="sxs-lookup"><span data-stu-id="932b3-126">See also</span></span>



[<span data-ttu-id="932b3-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="932b3-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="932b3-128">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="932b3-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="932b3-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="932b3-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="932b3-130">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="932b3-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

