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
ms.openlocfilehash: 03244fb240231a105b0a25a0797c13b9bf7f7a80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811420"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a><span data-ttu-id="ddaa0-103">Каноническое свойство PidTagOriginalAuthorEntryId</span><span class="sxs-lookup"><span data-stu-id="ddaa0-103">PidTagOriginalAuthorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="ddaa0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ddaa0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ddaa0-105">Содержит запись идентификатор автора первая версия сообщения, то есть, сообщение перед пересылку и ответ.</span><span class="sxs-lookup"><span data-stu-id="ddaa0-105">Contains the entry identifier of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ddaa0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ddaa0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ddaa0-107">PR_ORIGINAL_AUTHOR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ddaa0-107">PR_ORIGINAL_AUTHOR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="ddaa0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ddaa0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ddaa0-109">0x004C</span><span class="sxs-lookup"><span data-stu-id="ddaa0-109">0x004C</span></span>  <br/> |
|<span data-ttu-id="ddaa0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ddaa0-110">Data type:</span></span>  <br/> |<span data-ttu-id="ddaa0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ddaa0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ddaa0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ddaa0-112">Area:</span></span>  <br/> |<span data-ttu-id="ddaa0-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="ddaa0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddaa0-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ddaa0-114">Remarks</span></span>

<span data-ttu-id="ddaa0-115">Это свойство является одним из свойств адреса для автора сообщения.</span><span class="sxs-lookup"><span data-stu-id="ddaa0-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="ddaa0-116">В первой отправки сообщения клиентское приложение следует этому свойству присвоено значение значение **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ddaa0-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span></span> <span data-ttu-id="ddaa0-117">Никогда не изменяется при сообщение будет переслано или ответ.</span><span class="sxs-lookup"><span data-stu-id="ddaa0-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="ddaa0-118">Свойство author исходного обеспечивает сохранение информации из других доменов обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ddaa0-118">The original author property allows for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="ddaa0-119">При получении сообщения из другой домен обмена мгновенными сообщениями, например, из Интернета, это свойство позволяет убедиться, что исходное сведения не будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="ddaa0-119">When a message arrives from another messaging domain, such as from the Internet, this property provides a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ddaa0-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ddaa0-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ddaa0-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ddaa0-121">Header files</span></span>

<span data-ttu-id="ddaa0-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ddaa0-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="ddaa0-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ddaa0-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="ddaa0-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ddaa0-124">Mapitags.h</span></span>
  
> <span data-ttu-id="ddaa0-125">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ddaa0-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ddaa0-126">См. также</span><span class="sxs-lookup"><span data-stu-id="ddaa0-126">See also</span></span>



[<span data-ttu-id="ddaa0-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ddaa0-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ddaa0-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ddaa0-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ddaa0-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ddaa0-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ddaa0-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ddaa0-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

