---
title: Каноническое свойство PidTagReplyRecipientEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1ab8828dd2fc28a2fba1620fc251ba0a87c3e2bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811707"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a><span data-ttu-id="33ad8-103">Каноническое свойство PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="33ad8-103">PidTagReplyRecipientEntries Canonical Property</span></span>

  
  
<span data-ttu-id="33ad8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="33ad8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="33ad8-105">Содержит массив размера запись идентификаторов для получателей, которые требуется получить ответ.</span><span class="sxs-lookup"><span data-stu-id="33ad8-105">Contains a sized array of entry identifiers for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33ad8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="33ad8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33ad8-107">PR_REPLY_RECIPIENT_ENTRIES</span><span class="sxs-lookup"><span data-stu-id="33ad8-107">PR_REPLY_RECIPIENT_ENTRIES</span></span>  <br/> |
|<span data-ttu-id="33ad8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="33ad8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="33ad8-109">0x004F</span><span class="sxs-lookup"><span data-stu-id="33ad8-109">0x004F</span></span>  <br/> |
|<span data-ttu-id="33ad8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="33ad8-110">Data type:</span></span>  <br/> |<span data-ttu-id="33ad8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="33ad8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="33ad8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="33ad8-112">Area:</span></span>  <br/> |<span data-ttu-id="33ad8-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="33ad8-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33ad8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="33ad8-114">Remarks</span></span>

<span data-ttu-id="33ad8-115">Это свойство содержит структуру [FLATENTRYLIST](flatentrylist.md) и не является многозначным свойством.</span><span class="sxs-lookup"><span data-stu-id="33ad8-115">This property contains a [FLATENTRYLIST](flatentrylist.md) structure and is not a multivalued property.</span></span> 
  
<span data-ttu-id="33ad8-116">Если это свойство не указан, ответ отправляется только для пользователя, заданной свойством **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="33ad8-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="33ad8-117">При определении свойства **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) и это ответ отправляется всех получателей, определяемую средством эти два свойства.</span><span class="sxs-lookup"><span data-stu-id="33ad8-117">When this and the **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="33ad8-118">Поставщика транспорта использует эти свойства переопределение логики обычной информации.</span><span class="sxs-lookup"><span data-stu-id="33ad8-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="33ad8-119">Если задано это свойство или свойство **PR_REPLY_RECIPIENT_NAMES** , необходимо также установлен другие свойства.</span><span class="sxs-lookup"><span data-stu-id="33ad8-119">If either this property or the **PR_REPLY_RECIPIENT_NAMES** property is set, the other property must be set also.</span></span> <span data-ttu-id="33ad8-120">Эти свойства должно содержать такое же число получателей, и они должны содержать их в том же порядке.</span><span class="sxs-lookup"><span data-stu-id="33ad8-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="33ad8-121">Сбой выполняли этих требований может привести к непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="33ad8-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="33ad8-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="33ad8-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33ad8-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="33ad8-123">Protocol specifications</span></span>

<span data-ttu-id="33ad8-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33ad8-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33ad8-125">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="33ad8-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="33ad8-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33ad8-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33ad8-127">Задает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="33ad8-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="33ad8-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33ad8-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33ad8-129">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="33ad8-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33ad8-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="33ad8-130">Header files</span></span>

<span data-ttu-id="33ad8-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33ad8-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="33ad8-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="33ad8-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="33ad8-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="33ad8-133">Mapitags.h</span></span>
  
> <span data-ttu-id="33ad8-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="33ad8-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33ad8-135">См. также</span><span class="sxs-lookup"><span data-stu-id="33ad8-135">See also</span></span>



[<span data-ttu-id="33ad8-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="33ad8-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33ad8-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="33ad8-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33ad8-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="33ad8-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33ad8-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="33ad8-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

