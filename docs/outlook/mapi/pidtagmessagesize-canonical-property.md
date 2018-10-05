---
title: Каноническое свойство PidTagMessageSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3a49c6d70cc47ff726a7a99860b5e81a400be0bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387309"
---
# <a name="pidtagmessagesize-canonical-property"></a><span data-ttu-id="9feb9-103">Каноническое свойство PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="9feb9-103">PidTagMessageSize Canonical Property</span></span>

  
  
<span data-ttu-id="9feb9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9feb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9feb9-105">Содержит суммы размеров всех свойств для объекта сообщения, в байтах.</span><span class="sxs-lookup"><span data-stu-id="9feb9-105">Contains the sum, in bytes, of the sizes of all properties on a message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9feb9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9feb9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9feb9-107">PR_MESSAGE_SIZE</span><span class="sxs-lookup"><span data-stu-id="9feb9-107">PR_MESSAGE_SIZE</span></span>  <br/> |
|<span data-ttu-id="9feb9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9feb9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9feb9-109">0x0E08</span><span class="sxs-lookup"><span data-stu-id="9feb9-109">0x0E08</span></span>  <br/> |
|<span data-ttu-id="9feb9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9feb9-110">Data type:</span></span>  <br/> |<span data-ttu-id="9feb9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9feb9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9feb9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9feb9-112">Area:</span></span>  <br/> |<span data-ttu-id="9feb9-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="9feb9-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9feb9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9feb9-114">Remarks</span></span>

<span data-ttu-id="9feb9-115">Рекомендуется, что сообщение объекты предоставляют это свойство.</span><span class="sxs-lookup"><span data-stu-id="9feb9-115">It is recommended that message objects expose this property.</span></span> <span data-ttu-id="9feb9-116">Размер сообщения Указывает приблизительное число байтов, которые переносятся при перемещении сообщения из одного хранилища в другое.</span><span class="sxs-lookup"><span data-stu-id="9feb9-116">The message size indicates the approximate number of bytes that are transferred when the message is moved from one message store to another.</span></span> <span data-ttu-id="9feb9-117">Что совокупного размера всех свойств объекта сообщения, это обычно значительно больше, чем сам по себе он текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="9feb9-117">Being the sum of the sizes of all properties on the message object, it is usually considerably greater than the message text alone.</span></span> 
  
<span data-ttu-id="9feb9-118">Большинство сообщений хранилища compute поставщиков этого свойства для сообщений, которые они работают.</span><span class="sxs-lookup"><span data-stu-id="9feb9-118">Most message store providers compute this property for messages that they handle.</span></span> <span data-ttu-id="9feb9-119">Тем не менее некоторые поставщики хранения сообщения не поддерживают это свойство.</span><span class="sxs-lookup"><span data-stu-id="9feb9-119">However, some message store providers do not support this property.</span></span> <span data-ttu-id="9feb9-120">В любом случае это свойство недоступно до вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) или [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="9feb9-120">In any case, this property is not available until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMessage::SubmitMessage](imessage-submitmessage.md) method has been called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9feb9-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9feb9-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9feb9-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9feb9-122">Protocol specifications</span></span>

<span data-ttu-id="9feb9-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9feb9-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9feb9-124">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9feb9-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9feb9-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9feb9-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9feb9-126">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="9feb9-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9feb9-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9feb9-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9feb9-128">Обрабатывает операции папки.</span><span class="sxs-lookup"><span data-stu-id="9feb9-128">Handles folder operations.</span></span>
    
<span data-ttu-id="9feb9-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9feb9-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9feb9-130">Указывает допустимые операции для базовых объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="9feb9-130">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9feb9-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9feb9-131">Header files</span></span>

<span data-ttu-id="9feb9-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9feb9-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="9feb9-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9feb9-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="9feb9-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9feb9-134">Mapitags.h</span></span>
  
> <span data-ttu-id="9feb9-135">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="9feb9-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9feb9-136">См. также</span><span class="sxs-lookup"><span data-stu-id="9feb9-136">See also</span></span>



[<span data-ttu-id="9feb9-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9feb9-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9feb9-138">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9feb9-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9feb9-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9feb9-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9feb9-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9feb9-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

