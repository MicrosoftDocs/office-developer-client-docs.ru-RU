---
title: Каноническое свойство PidTagSentRepresentingSmtpAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ed122a2-0967-4de3-a2ee-69f81ae77b16
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a9114b1c9c3f5b09c5636f7d55d7111dd86afc06
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383585"
---
# <a name="pidtagsentrepresentingsmtpaddress-canonical-property"></a><span data-ttu-id="337f1-103">Каноническое свойство PidTagSentRepresentingSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="337f1-103">PidTagSentRepresentingSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="337f1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="337f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="337f1-105">Содержит адрес электронной почты транспортный протокол SMTP (Simple Mail) для обмена сообщениями пользователя, который представлен отправителем.</span><span class="sxs-lookup"><span data-stu-id="337f1-105">Contains the Simple Mail Transport Protocol (SMTP) email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="337f1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="337f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="337f1-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="337f1-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="337f1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="337f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="337f1-109">0x5D02</span><span class="sxs-lookup"><span data-stu-id="337f1-109">0x5D02</span></span>  <br/> |
|<span data-ttu-id="337f1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="337f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="337f1-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="337f1-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="337f1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="337f1-112">Area:</span></span>  <br/> |<span data-ttu-id="337f1-113">Address</span><span class="sxs-lookup"><span data-stu-id="337f1-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="337f1-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="337f1-114">Remarks</span></span>

<span data-ttu-id="337f1-115">Это свойство является примером свойства адреса для обмена мгновенными сообщениями, представленному отправителя пользователя.</span><span class="sxs-lookup"><span data-stu-id="337f1-115">This property is an example of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="337f1-116">Когда клиентское приложение отправляет сообщения от имени другого клиента, его следует устанавливать все свойства представленного отправителя значения для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="337f1-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="337f1-117">Обмена сообщениями при отправке на собственный имени обычно оставляет свойства представленного отправителя удалить.</span><span class="sxs-lookup"><span data-stu-id="337f1-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="337f1-118">Исходящие поставщика транспорта всегда необходимо оставить это свойство без изменений, если он имеет значение с клиента.</span><span class="sxs-lookup"><span data-stu-id="337f1-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="337f1-119">Если оно не установлено, поставщика транспорта должен установить значение свойства **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) в исходящих копии сообщения и оставить неопределенные на локальной копии.</span><span class="sxs-lookup"><span data-stu-id="337f1-119">If it is unset, the transport provider should set it to the **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="337f1-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="337f1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="337f1-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="337f1-121">Protocol specifications</span></span>

<span data-ttu-id="337f1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="337f1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="337f1-123">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="337f1-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="337f1-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="337f1-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="337f1-125">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="337f1-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="337f1-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="337f1-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="337f1-127">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="337f1-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="337f1-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="337f1-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="337f1-129">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="337f1-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="337f1-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="337f1-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="337f1-131">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="337f1-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="337f1-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="337f1-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="337f1-133">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="337f1-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="337f1-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="337f1-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="337f1-135">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="337f1-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="337f1-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="337f1-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="337f1-137">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="337f1-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="337f1-138">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="337f1-138">Header files</span></span>

<span data-ttu-id="337f1-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="337f1-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="337f1-140">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="337f1-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="337f1-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="337f1-141">Mapitags.h</span></span>
  
> <span data-ttu-id="337f1-142">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="337f1-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="337f1-143">См. также</span><span class="sxs-lookup"><span data-stu-id="337f1-143">See also</span></span>



[<span data-ttu-id="337f1-144">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="337f1-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="337f1-145">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="337f1-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="337f1-146">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="337f1-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="337f1-147">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="337f1-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

