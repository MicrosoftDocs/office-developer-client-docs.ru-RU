---
title: Каноническое свойство PidTagConversationTopic
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dfd437fac3a784212807c495f6e8f1adbe759cb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334687"
---
# <a name="pidtagconversationtopic-canonical-property"></a><span data-ttu-id="2cddd-103">Каноническое свойство PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="2cddd-103">PidTagConversationTopic Canonical Property</span></span>

  
  
<span data-ttu-id="2cddd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2cddd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2cddd-105">Содержит тему первого сообщения в цепочке бесед.</span><span class="sxs-lookup"><span data-stu-id="2cddd-105">Contains the topic of the first message in a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2cddd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2cddd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2cddd-107">ПР_КОНВЕРСАТИОН_ТОПИК, ПР_КОНВЕРСАТИОН_ТОПИК_А, ПР_КОНВЕРСАТИОН_ТОПИК_В</span><span class="sxs-lookup"><span data-stu-id="2cddd-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span></span>  <br/> |
|<span data-ttu-id="2cddd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2cddd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2cddd-109">0x0070</span><span class="sxs-lookup"><span data-stu-id="2cddd-109">0x0070</span></span>  <br/> |
|<span data-ttu-id="2cddd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2cddd-110">Data type:</span></span>  <br/> |<span data-ttu-id="2cddd-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="2cddd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2cddd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2cddd-112">Area:</span></span>  <br/> |<span data-ttu-id="2cddd-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="2cddd-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2cddd-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2cddd-114">Remarks</span></span>

<span data-ttu-id="2cddd-115">Поток беседы представляет ряд сообщений и ответов.</span><span class="sxs-lookup"><span data-stu-id="2cddd-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="2cddd-116">Эти свойства задаются для первого сообщения в потоке, обычно для свойства **пр_нормализед_субжект** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2cddd-116">These properties are set for the first message in a thread, usually to the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="2cddd-117">Последующие сообщения в потоке должны использовать одну и ту же тему без изменения.</span><span class="sxs-lookup"><span data-stu-id="2cddd-117">Subsequent messages in the thread should use the same topic without modification.</span></span> 
  
<span data-ttu-id="2cddd-118">Свойство **пр_конверсатион_индекс** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) указывает связь порядка между последовательными сообщениями и ответами.</span><span class="sxs-lookup"><span data-stu-id="2cddd-118">The **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property indicates the order relationship between subsequent messages and replies.</span></span> <span data-ttu-id="2cddd-119">Его использование необязательно, даже если заданы эти свойства.</span><span class="sxs-lookup"><span data-stu-id="2cddd-119">Its use is optional, even if these properties are set.</span></span> 
  
<span data-ttu-id="2cddd-120">У поставщика хранилища сообщений есть возможность гарантировать, что эти свойства всегда устанавливаются для входящих и исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="2cddd-120">A message store provider has the option of assuring that these properties are always set on incoming or outgoing messages.</span></span> <span data-ttu-id="2cddd-121">Если эти свойства уже заданы, их не следует изменять.</span><span class="sxs-lookup"><span data-stu-id="2cddd-121">If these properties are already set they should not be altered.</span></span> <span data-ttu-id="2cddd-122">В противном случае им можно присвоить значение **пр_нормализед_субжект**.</span><span class="sxs-lookup"><span data-stu-id="2cddd-122">If not, they can be set to **PR_NORMALIZED_SUBJECT**.</span></span> <span data-ttu-id="2cddd-123">Все действия должны выполняться перед [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="2cddd-123">Any action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2cddd-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2cddd-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2cddd-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2cddd-125">Protocol specifications</span></span>

<span data-ttu-id="2cddd-126">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2cddd-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2cddd-127">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2cddd-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2cddd-128">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2cddd-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2cddd-129">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2cddd-129">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2cddd-130">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="2cddd-130">Header files</span></span>

<span data-ttu-id="2cddd-131">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="2cddd-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="2cddd-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2cddd-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="2cddd-133">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="2cddd-133">Mapitags.h</span></span>
  
> <span data-ttu-id="2cddd-134">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="2cddd-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2cddd-135">См. также</span><span class="sxs-lookup"><span data-stu-id="2cddd-135">See also</span></span>



[<span data-ttu-id="2cddd-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2cddd-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2cddd-137">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="2cddd-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2cddd-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2cddd-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2cddd-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2cddd-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

