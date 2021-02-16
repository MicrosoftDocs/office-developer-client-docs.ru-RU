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
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="336b0-103">Каноническое свойство PidTagConversationKey</span><span class="sxs-lookup"><span data-stu-id="336b0-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="336b0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="336b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="336b0-105">Содержит ключ беседы, используемый в Microsoft Outlook только при поиске **IPM. Сообщения MessageManager,** например сообщения, которые содержат историю загрузки для учетной записи pop3.</span><span class="sxs-lookup"><span data-stu-id="336b0-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="336b0-106">Это свойство было неподготовлено в Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="336b0-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="336b0-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="336b0-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="336b0-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="336b0-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="336b0-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="336b0-109">Identifier:</span></span>  <br/> |<span data-ttu-id="336b0-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="336b0-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="336b0-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="336b0-111">Data type:</span></span>  <br/> |<span data-ttu-id="336b0-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="336b0-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="336b0-113">Область:</span><span class="sxs-lookup"><span data-stu-id="336b0-113">Area:</span></span>  <br/> |<span data-ttu-id="336b0-114">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="336b0-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="336b0-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="336b0-115">Remarks</span></span>

<span data-ttu-id="336b0-116">При доступе к электронным письмам в виде бесед и преобразовании свойств сообщений в формат [TNEF](transport-neutral-encapsulation-format-tnef.md)не используйте это свойство; вместо этого используйте канонические свойства [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) и [PidTagConversationTopic.](pidtagconversationtopic-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="336b0-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="336b0-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="336b0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="336b0-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="336b0-118">Protocol specifications</span></span>

<span data-ttu-id="336b0-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="336b0-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="336b0-120">Содержит ссылки на связанные Microsoft Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="336b0-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="336b0-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="336b0-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="336b0-122">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="336b0-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="336b0-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="336b0-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="336b0-124">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="336b0-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="336b0-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="336b0-125">Header files</span></span>

<span data-ttu-id="336b0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="336b0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="336b0-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="336b0-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="336b0-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="336b0-128">Mapitags.h</span></span>
  
> <span data-ttu-id="336b0-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="336b0-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="336b0-130">См. также</span><span class="sxs-lookup"><span data-stu-id="336b0-130">See also</span></span>



[<span data-ttu-id="336b0-131">Подtree IPM</span><span class="sxs-lookup"><span data-stu-id="336b0-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="336b0-132">Специальные папки MAPI</span><span class="sxs-lookup"><span data-stu-id="336b0-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="336b0-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="336b0-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="336b0-134">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="336b0-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="336b0-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="336b0-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="336b0-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="336b0-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

