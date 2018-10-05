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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400392"
---
# <a name="pidtagconversationtopic-canonical-property"></a><span data-ttu-id="824d9-103">Каноническое свойство PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="824d9-103">PidTagConversationTopic Canonical Property</span></span>

  
  
<span data-ttu-id="824d9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="824d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="824d9-105">Содержит раздел первого сообщения в потоке беседы.</span><span class="sxs-lookup"><span data-stu-id="824d9-105">Contains the topic of the first message in a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="824d9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="824d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="824d9-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span><span class="sxs-lookup"><span data-stu-id="824d9-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span></span>  <br/> |
|<span data-ttu-id="824d9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="824d9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="824d9-109">0x0070</span><span class="sxs-lookup"><span data-stu-id="824d9-109">0x0070</span></span>  <br/> |
|<span data-ttu-id="824d9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="824d9-110">Data type:</span></span>  <br/> |<span data-ttu-id="824d9-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="824d9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="824d9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="824d9-112">Area:</span></span>  <br/> |<span data-ttu-id="824d9-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="824d9-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="824d9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="824d9-114">Remarks</span></span>

<span data-ttu-id="824d9-115">Поток беседы представляет ряд сообщения и ответы.</span><span class="sxs-lookup"><span data-stu-id="824d9-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="824d9-116">Эти свойства задаются для первого сообщения в потоке, обычно к свойству **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="824d9-116">These properties are set for the first message in a thread, usually to the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="824d9-117">Длина последующих сообщений в потоке следует использовать же раздел без изменений.</span><span class="sxs-lookup"><span data-stu-id="824d9-117">Subsequent messages in the thread should use the same topic without modification.</span></span> 
  
<span data-ttu-id="824d9-118">Свойство **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) указывает порядок отношение между последующие сообщения и ответы.</span><span class="sxs-lookup"><span data-stu-id="824d9-118">The **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property indicates the order relationship between subsequent messages and replies.</span></span> <span data-ttu-id="824d9-119">Ее использования является необязательным, даже в том случае, если заданы следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="824d9-119">Its use is optional, even if these properties are set.</span></span> 
  
<span data-ttu-id="824d9-120">Поставщик хранения сообщений имеет возможность подтверждения, которое всегда эти свойства задаются на входящих или исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="824d9-120">A message store provider has the option of assuring that these properties are always set on incoming or outgoing messages.</span></span> <span data-ttu-id="824d9-121">Если эти свойства уже установлены они не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="824d9-121">If these properties are already set they should not be altered.</span></span> <span data-ttu-id="824d9-122">В противном случае может иметь значение **PR_NORMALIZED_SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="824d9-122">If not, they can be set to **PR_NORMALIZED_SUBJECT**.</span></span> <span data-ttu-id="824d9-123">Должна быть переведена каких-либо действий в до вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="824d9-123">Any action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="824d9-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="824d9-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="824d9-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="824d9-125">Protocol specifications</span></span>

<span data-ttu-id="824d9-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="824d9-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="824d9-127">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="824d9-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="824d9-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="824d9-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="824d9-129">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="824d9-129">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="824d9-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="824d9-130">Header files</span></span>

<span data-ttu-id="824d9-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="824d9-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="824d9-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="824d9-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="824d9-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="824d9-133">Mapitags.h</span></span>
  
> <span data-ttu-id="824d9-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="824d9-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="824d9-135">См. также</span><span class="sxs-lookup"><span data-stu-id="824d9-135">See also</span></span>



[<span data-ttu-id="824d9-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="824d9-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="824d9-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="824d9-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="824d9-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="824d9-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="824d9-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="824d9-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

