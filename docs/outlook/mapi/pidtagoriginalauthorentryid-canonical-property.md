---
title: Каноническое свойство PidTagOriginalAuthorEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEntryId
api_type:
- COM
ms.assetid: 34654660-b003-42f5-9fcd-24ebaccd735d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 866c28bc08f669d18487c99c9a13bc7347b605fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425591"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a><span data-ttu-id="50596-103">Каноническое свойство PidTagOriginalAuthorEntryId</span><span class="sxs-lookup"><span data-stu-id="50596-103">PidTagOriginalAuthorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="50596-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50596-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50596-105">Содержит идентификатор записи автора первой версии сообщения, то есть сообщения перед его переададрещением или ответом.</span><span class="sxs-lookup"><span data-stu-id="50596-105">Contains the entry identifier of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50596-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="50596-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50596-107">PR_ORIGINAL_AUTHOR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="50596-107">PR_ORIGINAL_AUTHOR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="50596-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="50596-108">Identifier:</span></span>  <br/> |<span data-ttu-id="50596-109">0x004C</span><span class="sxs-lookup"><span data-stu-id="50596-109">0x004C</span></span>  <br/> |
|<span data-ttu-id="50596-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="50596-110">Data type:</span></span>  <br/> |<span data-ttu-id="50596-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="50596-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="50596-112">Область:</span><span class="sxs-lookup"><span data-stu-id="50596-112">Area:</span></span>  <br/> |<span data-ttu-id="50596-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="50596-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50596-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="50596-114">Remarks</span></span>

<span data-ttu-id="50596-115">Это свойство является одним из свойств адресов для автора сообщения.</span><span class="sxs-lookup"><span data-stu-id="50596-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="50596-116">При первой отправке сообщения клиентская заявка должна установить это свойство к значению **PR_SENDER_ENTRYID** [(PidTagSenderEntryId).](pidtagsenderentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="50596-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span></span> <span data-ttu-id="50596-117">Он никогда не меняется, когда сообщение переададовыв или отвечает на него.</span><span class="sxs-lookup"><span data-stu-id="50596-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="50596-118">Исходное свойство автора позволяет сохранить сведения из локального домена обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="50596-118">The original author property allows for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="50596-119">Когда сообщение поступает из другого домена обмена сообщениями, например из Интернета, это свойство предоставляет способ убедиться, что исходные сведения не будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="50596-119">When a message arrives from another messaging domain, such as from the Internet, this property provides a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50596-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="50596-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="50596-121">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="50596-121">Header files</span></span>

<span data-ttu-id="50596-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50596-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="50596-123">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="50596-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="50596-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="50596-124">Mapitags.h</span></span>
  
> <span data-ttu-id="50596-125">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="50596-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50596-126">См. также</span><span class="sxs-lookup"><span data-stu-id="50596-126">See also</span></span>



[<span data-ttu-id="50596-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="50596-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50596-128">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="50596-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50596-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="50596-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50596-130">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="50596-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

