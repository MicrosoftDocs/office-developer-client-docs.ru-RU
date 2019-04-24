---
title: Каноническое свойство PidTagConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334722"
---
# <a name="pidtagconversationindex-canonical-property"></a><span data-ttu-id="d87eb-103">Каноническое свойство PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="d87eb-103">PidTagConversationIndex Canonical Property</span></span>

  
  
<span data-ttu-id="d87eb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d87eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d87eb-105">Содержит двоичное значение, которое указывает относительное положение этого сообщения в цепочке сообщений.</span><span class="sxs-lookup"><span data-stu-id="d87eb-105">Contains a binary value that indicates the relative position of this message within a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d87eb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d87eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d87eb-107">ПР_КОНВЕРСАТИОН_ИНДЕКС</span><span class="sxs-lookup"><span data-stu-id="d87eb-107">PR_CONVERSATION_INDEX</span></span>  <br/> |
|<span data-ttu-id="d87eb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d87eb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d87eb-109">0x0071</span><span class="sxs-lookup"><span data-stu-id="d87eb-109">0x0071</span></span>  <br/> |
|<span data-ttu-id="d87eb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d87eb-110">Data type:</span></span>  <br/> |<span data-ttu-id="d87eb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d87eb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d87eb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d87eb-112">Area:</span></span>  <br/> |<span data-ttu-id="d87eb-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="d87eb-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d87eb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d87eb-114">Remarks</span></span>

<span data-ttu-id="d87eb-115">Поток беседы представляет ряд сообщений и ответов.</span><span class="sxs-lookup"><span data-stu-id="d87eb-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="d87eb-116">Это свойство обычно реализуется с помощью сцепленных значений отметок времени.</span><span class="sxs-lookup"><span data-stu-id="d87eb-116">This property is usually implemented using concatenated time stamp values.</span></span> <span data-ttu-id="d87eb-117">Его использование является необязательным, даже если задано свойство **пр_конверсатион_топик** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d87eb-117">Its use is optional, even if **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) is set.</span></span> 
  
<span data-ttu-id="d87eb-118">MAPI предоставляет функцию [сккреатеконверсатиониндекс](sccreateconversationindex.md) для создания или обновления индекса беседы.</span><span class="sxs-lookup"><span data-stu-id="d87eb-118">MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index.</span></span> <span data-ttu-id="d87eb-119">Функция принимает текущее значение индекса в виде массива байтов и возвращает значение индекса с отметкой времени, сцепленной с конечной областью.</span><span class="sxs-lookup"><span data-stu-id="d87eb-119">The function takes the current index value as a counted byte array and returns the index value with a time stamp concatenated onto the end.</span></span> <span data-ttu-id="d87eb-120">Сообщение, представляющее ответ на другое сообщение, должно использовать **сккреатеконверсатиониндекс** для обновления этого свойства.</span><span class="sxs-lookup"><span data-stu-id="d87eb-120">A message representing a reply to another message should use **ScCreateConversationIndex** to update this property.</span></span> 
  
<span data-ttu-id="d87eb-121">У поставщика хранилища сообщений есть возможность гарантировать, что **пр_конверсатион_индекс** всегда устанавливается для входящих и исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="d87eb-121">A message store provider has the option of assuring that **PR_CONVERSATION_INDEX** is always set on incoming or outgoing messages.</span></span> <span data-ttu-id="d87eb-122">Это можно сделать, вызвав **сккреатеконверсатиониндекс**, либо с существующим значением, если это свойство задано, либо со значением NULL, если это не так.</span><span class="sxs-lookup"><span data-stu-id="d87eb-122">It can do this by calling **ScCreateConversationIndex**, either with the existing value if this property is set or with NULL if it is not.</span></span> <span data-ttu-id="d87eb-123">Это действие следует выполнить перед [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="d87eb-123">This action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
<span data-ttu-id="d87eb-124">Все сообщения с одинаковым значением для **пр_конверсатион_топик** можно сортировать по этому свойству, чтобы отобразить иерархические отношения между сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d87eb-124">All messages that have the same value for **PR_CONVERSATION_TOPIC** can be sorted on this property to reveal the hierarchical relationship of the messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d87eb-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d87eb-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d87eb-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d87eb-126">Protocol specifications</span></span>

<span data-ttu-id="d87eb-127">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d87eb-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d87eb-128">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d87eb-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d87eb-129">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d87eb-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d87eb-130">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d87eb-130">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d87eb-131">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="d87eb-131">Header files</span></span>

<span data-ttu-id="d87eb-132">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d87eb-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="d87eb-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d87eb-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="d87eb-134">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="d87eb-134">Mapitags.h</span></span>
  
> <span data-ttu-id="d87eb-135">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="d87eb-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d87eb-136">См. также</span><span class="sxs-lookup"><span data-stu-id="d87eb-136">See also</span></span>



[<span data-ttu-id="d87eb-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d87eb-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d87eb-138">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="d87eb-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d87eb-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d87eb-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d87eb-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d87eb-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

