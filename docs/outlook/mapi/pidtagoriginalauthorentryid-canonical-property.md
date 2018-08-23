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
ms.openlocfilehash: 03dcc9a1f929bc6f99ca9e1dd9f75f3fb9c3dcb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562969"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a><span data-ttu-id="fe8ab-103">Каноническое свойство PidTagOriginalAuthorEntryId</span><span class="sxs-lookup"><span data-stu-id="fe8ab-103">PidTagOriginalAuthorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="fe8ab-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe8ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe8ab-105">Содержит запись идентификатор автора первая версия сообщения, то есть, сообщение перед пересылку и ответ.</span><span class="sxs-lookup"><span data-stu-id="fe8ab-105">Contains the entry identifier of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe8ab-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fe8ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe8ab-107">PR_ORIGINAL_AUTHOR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fe8ab-107">PR_ORIGINAL_AUTHOR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="fe8ab-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="fe8ab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fe8ab-109">0x004C</span><span class="sxs-lookup"><span data-stu-id="fe8ab-109">0x004C</span></span>  <br/> |
|<span data-ttu-id="fe8ab-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="fe8ab-110">Data type:</span></span>  <br/> |<span data-ttu-id="fe8ab-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fe8ab-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fe8ab-112">Область:</span><span class="sxs-lookup"><span data-stu-id="fe8ab-112">Area:</span></span>  <br/> |<span data-ttu-id="fe8ab-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="fe8ab-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe8ab-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="fe8ab-114">Remarks</span></span>

<span data-ttu-id="fe8ab-115">Это свойство является одним из свойств адреса для автора сообщения.</span><span class="sxs-lookup"><span data-stu-id="fe8ab-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="fe8ab-116">В первой отправки сообщения клиентское приложение следует этому свойству присвоено значение значение **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fe8ab-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span></span> <span data-ttu-id="fe8ab-117">Никогда не изменяется при сообщение будет переслано или ответ.</span><span class="sxs-lookup"><span data-stu-id="fe8ab-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="fe8ab-118">Свойство author исходного обеспечивает сохранение информации из других доменов обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="fe8ab-118">The original author property allows for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="fe8ab-119">При получении сообщения из другой домен обмена мгновенными сообщениями, например, из Интернета, это свойство позволяет убедиться, что исходное сведения не будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="fe8ab-119">When a message arrives from another messaging domain, such as from the Internet, this property provides a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fe8ab-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fe8ab-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fe8ab-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="fe8ab-121">Header files</span></span>

<span data-ttu-id="fe8ab-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe8ab-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe8ab-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fe8ab-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="fe8ab-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fe8ab-124">Mapitags.h</span></span>
  
> <span data-ttu-id="fe8ab-125">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="fe8ab-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe8ab-126">См. также</span><span class="sxs-lookup"><span data-stu-id="fe8ab-126">See also</span></span>



[<span data-ttu-id="fe8ab-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fe8ab-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe8ab-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fe8ab-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe8ab-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fe8ab-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe8ab-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="fe8ab-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

