---
title: Каноническое свойство PidTagOriginalAuthorSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 09331e1201b6f6e45bb9e26e618ee59e67efbf8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409582"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a><span data-ttu-id="8a721-103">Каноническое свойство PidTagOriginalAuthorSearchKey</span><span class="sxs-lookup"><span data-stu-id="8a721-103">PidTagOriginalAuthorSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="8a721-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a721-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a721-105">Содержит ключ поиска автора первой версии сообщения, то есть сообщения перед его переададрением или ответом.</span><span class="sxs-lookup"><span data-stu-id="8a721-105">Contains the search key of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a721-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8a721-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a721-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="8a721-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="8a721-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8a721-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a721-109">0x0056</span><span class="sxs-lookup"><span data-stu-id="8a721-109">0x0056</span></span>  <br/> |
|<span data-ttu-id="8a721-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8a721-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a721-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8a721-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8a721-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8a721-112">Area:</span></span>  <br/> |<span data-ttu-id="8a721-113">Server</span><span class="sxs-lookup"><span data-stu-id="8a721-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a721-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8a721-114">Remarks</span></span>

<span data-ttu-id="8a721-115">Это свойство является одним из свойств адресов для автора сообщения.</span><span class="sxs-lookup"><span data-stu-id="8a721-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="8a721-116">При первой отправке сообщения клиентская заявка должна установить это свойство к значению свойства[PR_SENDER_SEARCH_KEY PidTagSenderSearchKey.](pidtagsendersearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8a721-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) property.</span></span> <span data-ttu-id="8a721-117">Он никогда не меняется, когда сообщение переададовыв или отвечает на него.</span><span class="sxs-lookup"><span data-stu-id="8a721-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="8a721-118">Исходные свойства автора позволяют сохранить сведения из локального домена обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="8a721-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="8a721-119">Когда сообщение поступает из другого домена обмена сообщениями, например из Интернета, эти свойства предоставляют способ убедиться, что исходные сведения не будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="8a721-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8a721-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8a721-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8a721-121">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="8a721-121">Header files</span></span>

<span data-ttu-id="8a721-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a721-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a721-123">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8a721-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a721-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8a721-124">Mapitags.h</span></span>
  
> <span data-ttu-id="8a721-125">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="8a721-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a721-126">См. также</span><span class="sxs-lookup"><span data-stu-id="8a721-126">See also</span></span>



[<span data-ttu-id="8a721-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8a721-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a721-128">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8a721-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a721-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8a721-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a721-130">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="8a721-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

