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
ms.openlocfilehash: 000132f052abb666ae844ec7d21b59c85ab43613
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355057"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a><span data-ttu-id="2e2b7-103">Каноническое свойство PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="2e2b7-103">PidTagReplyRecipientEntries Canonical Property</span></span>

  
  
<span data-ttu-id="2e2b7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e2b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e2b7-105">Содержит большой массив идентификаторов записей для получателей, которые должны получить ответ.</span><span class="sxs-lookup"><span data-stu-id="2e2b7-105">Contains a sized array of entry identifiers for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e2b7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2e2b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e2b7-107">PR_REPLY_RECIPIENT_ENTRIES</span><span class="sxs-lookup"><span data-stu-id="2e2b7-107">PR_REPLY_RECIPIENT_ENTRIES</span></span>  <br/> |
|<span data-ttu-id="2e2b7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2e2b7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2e2b7-109">0x004F</span><span class="sxs-lookup"><span data-stu-id="2e2b7-109">0x004F</span></span>  <br/> |
|<span data-ttu-id="2e2b7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2e2b7-110">Data type:</span></span>  <br/> |<span data-ttu-id="2e2b7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2e2b7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2e2b7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2e2b7-112">Area:</span></span>  <br/> |<span data-ttu-id="2e2b7-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="2e2b7-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e2b7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2e2b7-114">Remarks</span></span>

<span data-ttu-id="2e2b7-115">Это свойство содержит [структуру FLATENTRYLIST](flatentrylist.md) и не является многоценным свойством.</span><span class="sxs-lookup"><span data-stu-id="2e2b7-115">This property contains a [FLATENTRYLIST](flatentrylist.md) structure and is not a multivalued property.</span></span> 
  
<span data-ttu-id="2e2b7-116">Если этого свойства нет, ответ отправляется только пользователю, идентифицированным свойством **PR_SENDER_ENTRYID** [(PidTagSenderEntryId).](pidtagsenderentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="2e2b7-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="2e2b7-117">Когда определяются свойства **PR_REPLY_RECIPIENT_NAMES** [(PidTagReplyRecipientNames),](pidtagreplyrecipientnames-canonical-property.md)ответ отправляется всем получателям, указанным этими двумя свойствами.</span><span class="sxs-lookup"><span data-stu-id="2e2b7-117">When this and the **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="2e2b7-118">Поставщик транспорта использует эти свойства для переопределения обычной логики ответа.</span><span class="sxs-lookup"><span data-stu-id="2e2b7-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="2e2b7-119">Если заданной PR_REPLY_RECIPIENT_NAMES  или PR_REPLY_RECIPIENT_NAMES, необходимо также установить другое свойство.</span><span class="sxs-lookup"><span data-stu-id="2e2b7-119">If either this property or the **PR_REPLY_RECIPIENT_NAMES** property is set, the other property must be set also.</span></span> <span data-ttu-id="2e2b7-120">Эти свойства должны содержать одинаковое число получателей и содержать их в том же порядке.</span><span class="sxs-lookup"><span data-stu-id="2e2b7-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="2e2b7-121">Несоблюдение этих требований может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="2e2b7-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2e2b7-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2e2b7-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2e2b7-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2e2b7-123">Protocol specifications</span></span>

<span data-ttu-id="2e2b7-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e2b7-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e2b7-125">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="2e2b7-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2e2b7-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e2b7-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e2b7-127">Указывает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2e2b7-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="2e2b7-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e2b7-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e2b7-129">Преобразуется из стандартных конвенций электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="2e2b7-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2e2b7-130">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="2e2b7-130">Header files</span></span>

<span data-ttu-id="2e2b7-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e2b7-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e2b7-132">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2e2b7-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="2e2b7-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2e2b7-133">Mapitags.h</span></span>
  
> <span data-ttu-id="2e2b7-134">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2e2b7-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e2b7-135">См. также</span><span class="sxs-lookup"><span data-stu-id="2e2b7-135">See also</span></span>



[<span data-ttu-id="2e2b7-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2e2b7-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e2b7-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2e2b7-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e2b7-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2e2b7-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e2b7-139">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="2e2b7-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

