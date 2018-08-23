---
title: Каноническое свойство PidTagConversationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b4c8c6cf3bee0575a42bc42a1ebf5e185ef78ab4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591634"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="fcec1-103">Каноническое свойство PidTagConversationKey</span><span class="sxs-lookup"><span data-stu-id="fcec1-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="fcec1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcec1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcec1-105">Содержит беседы ключ, используемый в Microsoft Outlook только в том случае, если поиск **IPM. MessageManager** сообщения, такие как сообщение, содержащее истории загрузки для учетной записи Post Office Protocol (POP3).</span><span class="sxs-lookup"><span data-stu-id="fcec1-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="fcec1-106">Это свойство является устаревшим в Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fcec1-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcec1-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fcec1-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="fcec1-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="fcec1-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="fcec1-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="fcec1-109">Identifier:</span></span>  <br/> |<span data-ttu-id="fcec1-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="fcec1-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="fcec1-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="fcec1-111">Data type:</span></span>  <br/> |<span data-ttu-id="fcec1-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fcec1-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fcec1-113">Область:</span><span class="sxs-lookup"><span data-stu-id="fcec1-113">Area:</span></span>  <br/> |<span data-ttu-id="fcec1-114">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="fcec1-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fcec1-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="fcec1-115">Remarks</span></span>

<span data-ttu-id="fcec1-116">При доступе к сообщениям электронной почты как бесед и преобразование свойства сообщения в [Transport-Neutral Encapsulation формата TNEF ()](transport-neutral-encapsulation-format-tnef.md), не используйте это свойство; Используйте свойства каноническое [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) и [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="fcec1-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fcec1-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fcec1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fcec1-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="fcec1-118">Protocol specifications</span></span>

<span data-ttu-id="fcec1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcec1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcec1-120">Содержит ссылки на связанные спецификаций протокола Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fcec1-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fcec1-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcec1-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcec1-122">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="fcec1-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="fcec1-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcec1-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcec1-124">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="fcec1-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fcec1-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="fcec1-125">Header files</span></span>

<span data-ttu-id="fcec1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fcec1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fcec1-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fcec1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="fcec1-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fcec1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="fcec1-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="fcec1-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fcec1-130">См. также</span><span class="sxs-lookup"><span data-stu-id="fcec1-130">See also</span></span>



[<span data-ttu-id="fcec1-131">Поддерево IPM</span><span class="sxs-lookup"><span data-stu-id="fcec1-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="fcec1-132">����������� ����� MAPI</span><span class="sxs-lookup"><span data-stu-id="fcec1-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="fcec1-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fcec1-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fcec1-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fcec1-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fcec1-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fcec1-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fcec1-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="fcec1-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

