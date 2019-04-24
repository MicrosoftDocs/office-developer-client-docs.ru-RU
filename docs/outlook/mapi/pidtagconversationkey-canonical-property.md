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
ms.openlocfilehash: 00c65dae9bc29fe9cdb310b819ba99d6d46ebfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334701"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="915e9-103">Каноническое свойство PidTagConversationKey</span><span class="sxs-lookup"><span data-stu-id="915e9-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="915e9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="915e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="915e9-105">Содержит ключ беседы, используемый в Microsoft Outlook только при размещении **IPM. Сообщения Мессажеманажер** , например сообщение, содержащее историю загрузки для учетной записи протокола POP3.</span><span class="sxs-lookup"><span data-stu-id="915e9-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="915e9-106">Это свойство является устаревшим в Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="915e9-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="915e9-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="915e9-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="915e9-108">ПР_КОНВЕРСАТИОН_КЭЙ</span><span class="sxs-lookup"><span data-stu-id="915e9-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="915e9-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="915e9-109">Identifier:</span></span>  <br/> |<span data-ttu-id="915e9-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="915e9-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="915e9-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="915e9-111">Data type:</span></span>  <br/> |<span data-ttu-id="915e9-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="915e9-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="915e9-113">Область:</span><span class="sxs-lookup"><span data-stu-id="915e9-113">Area:</span></span>  <br/> |<span data-ttu-id="915e9-114">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="915e9-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="915e9-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="915e9-115">Remarks</span></span>

<span data-ttu-id="915e9-116">При доступе к сообщениям электронной почты в виде бесед и преобразовании свойств сообщения в [Формат TNEF](transport-neutral-encapsulation-format-tnef.md)не используйте это свойство. Вместо этого используйте канонические свойства [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) и [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="915e9-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="915e9-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="915e9-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="915e9-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="915e9-118">Protocol specifications</span></span>

<span data-ttu-id="915e9-119">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="915e9-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="915e9-120">Содержит ссылки на соответствующие спецификации протоколов Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="915e9-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="915e9-121">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="915e9-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="915e9-122">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="915e9-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="915e9-123">[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="915e9-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="915e9-124">Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.</span><span class="sxs-lookup"><span data-stu-id="915e9-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="915e9-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="915e9-125">Header files</span></span>

<span data-ttu-id="915e9-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="915e9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="915e9-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="915e9-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="915e9-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="915e9-128">Mapitags.h</span></span>
  
> <span data-ttu-id="915e9-129">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="915e9-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="915e9-130">См. также</span><span class="sxs-lookup"><span data-stu-id="915e9-130">See also</span></span>



[<span data-ttu-id="915e9-131">Поддерево IPM</span><span class="sxs-lookup"><span data-stu-id="915e9-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="915e9-132">Специальные папки MAPI</span><span class="sxs-lookup"><span data-stu-id="915e9-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="915e9-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="915e9-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="915e9-134">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="915e9-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="915e9-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="915e9-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="915e9-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="915e9-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

