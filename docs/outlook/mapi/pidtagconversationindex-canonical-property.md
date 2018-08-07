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
ms.openlocfilehash: bddb667cba99e240a6ce182c9c1c8ed47f467e15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811007"
---
# <a name="pidtagconversationindex-canonical-property"></a><span data-ttu-id="835f0-103">Каноническое свойство PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="835f0-103">PidTagConversationIndex Canonical Property</span></span>

  
  
<span data-ttu-id="835f0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="835f0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="835f0-105">Содержит двоичные значение, указывающее, относительное положение этого сообщения в рамках потока беседы.</span><span class="sxs-lookup"><span data-stu-id="835f0-105">Contains a binary value that indicates the relative position of this message within a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="835f0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="835f0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="835f0-107">PR_CONVERSATION_INDEX</span><span class="sxs-lookup"><span data-stu-id="835f0-107">PR_CONVERSATION_INDEX</span></span>  <br/> |
|<span data-ttu-id="835f0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="835f0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="835f0-109">0x0071</span><span class="sxs-lookup"><span data-stu-id="835f0-109">0x0071</span></span>  <br/> |
|<span data-ttu-id="835f0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="835f0-110">Data type:</span></span>  <br/> |<span data-ttu-id="835f0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="835f0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="835f0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="835f0-112">Area:</span></span>  <br/> |<span data-ttu-id="835f0-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="835f0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="835f0-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="835f0-114">Remarks</span></span>

<span data-ttu-id="835f0-115">Поток беседы представляет ряд сообщения и ответы.</span><span class="sxs-lookup"><span data-stu-id="835f0-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="835f0-116">Обычно это свойство реализуется с помощью значений составное временной метки.</span><span class="sxs-lookup"><span data-stu-id="835f0-116">This property is usually implemented using concatenated time stamp values.</span></span> <span data-ttu-id="835f0-117">Ее использования является необязательным, даже в том случае, если установлено **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="835f0-117">Its use is optional, even if **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) is set.</span></span> 
  
<span data-ttu-id="835f0-118">MAPI предоставляет функцию [ScCreateConversationIndex](sccreateconversationindex.md) для создания или обновления индекса беседы.</span><span class="sxs-lookup"><span data-stu-id="835f0-118">MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index.</span></span> <span data-ttu-id="835f0-119">Функция принимает текущее значение индекса в виде массива байтов инвентаризации и возвращает значение индекса с отметкой времени, присоединенным в конце.</span><span class="sxs-lookup"><span data-stu-id="835f0-119">The function takes the current index value as a counted byte array and returns the index value with a time stamp concatenated onto the end.</span></span> <span data-ttu-id="835f0-120">Сообщение, представляющий ответ на другое сообщение необходимо использовать **ScCreateConversationIndex** для обновления этого свойства.</span><span class="sxs-lookup"><span data-stu-id="835f0-120">A message representing a reply to another message should use **ScCreateConversationIndex** to update this property.</span></span> 
  
<span data-ttu-id="835f0-121">Поставщик хранения сообщений имеет возможность подтверждения, **PR_CONVERSATION_INDEX** всегда установлено для входящих или исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="835f0-121">A message store provider has the option of assuring that **PR_CONVERSATION_INDEX** is always set on incoming or outgoing messages.</span></span> <span data-ttu-id="835f0-122">Его можно сделать, вызвав **ScCreateConversationIndex**, существующее значение, если значение этого свойства или значение NULL, если он не установлен.</span><span class="sxs-lookup"><span data-stu-id="835f0-122">It can do this by calling **ScCreateConversationIndex**, either with the existing value if this property is set or with NULL if it is not.</span></span> <span data-ttu-id="835f0-123">Это действие следует применять до вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="835f0-123">This action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
<span data-ttu-id="835f0-124">Все сообщения, которые имеют одинаковые значения для **PR_CONVERSATION_TOPIC** можно сортировать на это свойство, чтобы показать иерархическую связь сообщений.</span><span class="sxs-lookup"><span data-stu-id="835f0-124">All messages that have the same value for **PR_CONVERSATION_TOPIC** can be sorted on this property to reveal the hierarchical relationship of the messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="835f0-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="835f0-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="835f0-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="835f0-126">Protocol specifications</span></span>

<span data-ttu-id="835f0-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="835f0-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="835f0-128">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="835f0-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="835f0-129">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="835f0-129">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="835f0-130">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="835f0-130">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="835f0-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="835f0-131">Header files</span></span>

<span data-ttu-id="835f0-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="835f0-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="835f0-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="835f0-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="835f0-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="835f0-134">Mapitags.h</span></span>
  
> <span data-ttu-id="835f0-135">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="835f0-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="835f0-136">См. также</span><span class="sxs-lookup"><span data-stu-id="835f0-136">See also</span></span>



[<span data-ttu-id="835f0-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="835f0-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="835f0-138">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="835f0-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="835f0-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="835f0-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="835f0-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="835f0-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

