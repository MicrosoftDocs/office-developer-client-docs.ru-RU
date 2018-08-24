---
title: Каноническое свойство PidTagSentRepresentingEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingEmailAddress
api_type:
- COM
ms.assetid: 5fa4edde-475c-4568-946b-73eb08f97a61
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 689bdeb463d0e54d02be88463dabb75ef756bee9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573924"
---
# <a name="pidtagsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="10b6b-103">Каноническое свойство PidTagSentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="10b6b-103">PidTagSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="10b6b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10b6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10b6b-105">Содержит адрес электронной почты для обмена сообщениями пользователя, который представлен отправителем.</span><span class="sxs-lookup"><span data-stu-id="10b6b-105">Contains the email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10b6b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="10b6b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10b6b-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="10b6b-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="10b6b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="10b6b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="10b6b-109">0x0065</span><span class="sxs-lookup"><span data-stu-id="10b6b-109">0x0065</span></span>  <br/> |
|<span data-ttu-id="10b6b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="10b6b-110">Data type:</span></span>  <br/> |<span data-ttu-id="10b6b-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="10b6b-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="10b6b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="10b6b-112">Area:</span></span>  <br/> |<span data-ttu-id="10b6b-113">Address</span><span class="sxs-lookup"><span data-stu-id="10b6b-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10b6b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="10b6b-114">Remarks</span></span>

<span data-ttu-id="10b6b-115">Эти свойства являются примерами свойства адреса для обмена мгновенными сообщениями, представленному отправителя пользователя.</span><span class="sxs-lookup"><span data-stu-id="10b6b-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="10b6b-116">Когда клиентское приложение отправляет сообщения от имени другого клиента, его следует устанавливать все свойства представленного отправителя значения для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="10b6b-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="10b6b-117">Обмена сообщениями при отправке на собственный имени обычно оставляет свойства представленного отправителя удалить.</span><span class="sxs-lookup"><span data-stu-id="10b6b-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="10b6b-118">Исходящие поставщика транспорта всегда необходимо оставить эти свойства, без изменений, если он имеет значение с клиента.</span><span class="sxs-lookup"><span data-stu-id="10b6b-118">The outgoing transport provider must always leave these properties unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="10b6b-119">Если оно не установлено, поставщика транспорта должен установить значение свойства **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) в исходящих копии сообщения и оставить неопределенные на локальной копии.</span><span class="sxs-lookup"><span data-stu-id="10b6b-119">If it is unset, the transport provider should set it to the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="10b6b-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="10b6b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10b6b-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="10b6b-121">Protocol specifications</span></span>

<span data-ttu-id="10b6b-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10b6b-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10b6b-123">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="10b6b-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="10b6b-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10b6b-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10b6b-125">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="10b6b-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="10b6b-126">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10b6b-126">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10b6b-127">Задает свойства и операции, которые представляют элементам RSS-Каналов.</span><span class="sxs-lookup"><span data-stu-id="10b6b-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="10b6b-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10b6b-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10b6b-129">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="10b6b-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="10b6b-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10b6b-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10b6b-131">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="10b6b-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="10b6b-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10b6b-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10b6b-133">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="10b6b-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="10b6b-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10b6b-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10b6b-135">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="10b6b-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="10b6b-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10b6b-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10b6b-137">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="10b6b-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10b6b-138">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="10b6b-138">Header files</span></span>

<span data-ttu-id="10b6b-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10b6b-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="10b6b-140">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="10b6b-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="10b6b-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="10b6b-141">Mapitags.h</span></span>
  
> <span data-ttu-id="10b6b-142">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="10b6b-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10b6b-143">См. также</span><span class="sxs-lookup"><span data-stu-id="10b6b-143">See also</span></span>



[<span data-ttu-id="10b6b-144">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="10b6b-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10b6b-145">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="10b6b-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10b6b-146">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="10b6b-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10b6b-147">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="10b6b-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

