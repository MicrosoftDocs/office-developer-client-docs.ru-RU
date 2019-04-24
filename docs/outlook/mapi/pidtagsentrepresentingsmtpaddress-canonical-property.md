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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341939"
---
# <a name="pidtagsentrepresentingsmtpaddress-canonical-property"></a><span data-ttu-id="7b812-103">Каноническое свойство PidTagSentRepresentingSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="7b812-103">PidTagSentRepresentingSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="7b812-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b812-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b812-105">Содержит адрес электронной почты по протоколу SMTP для пользователя обмена сообщениями, представленного отправителями.</span><span class="sxs-lookup"><span data-stu-id="7b812-105">Contains the Simple Mail Transport Protocol (SMTP) email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b812-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7b812-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b812-107">ПР_СЕНТ_РЕПРЕСЕНТИНГ_СМТП_АДДРЕСС, ПР_СЕНТ_РЕПРЕСЕНТИНГ_СМТП_АДДРЕСС_А, ПР_СЕНТ_РЕПРЕСЕНТИНГ_СМТП_АДДРЕСС_В</span><span class="sxs-lookup"><span data-stu-id="7b812-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="7b812-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7b812-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7b812-109">0x5D02</span><span class="sxs-lookup"><span data-stu-id="7b812-109">0x5D02</span></span>  <br/> |
|<span data-ttu-id="7b812-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7b812-110">Data type:</span></span>  <br/> |<span data-ttu-id="7b812-111">ПТ_УНИКОДЕ, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="7b812-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="7b812-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7b812-112">Area:</span></span>  <br/> |<span data-ttu-id="7b812-113">Address</span><span class="sxs-lookup"><span data-stu-id="7b812-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b812-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b812-114">Remarks</span></span>

<span data-ttu-id="7b812-115">Это свойство представляет собой пример свойств адреса для пользователя обмена сообщениями, представленного отправителями.</span><span class="sxs-lookup"><span data-stu-id="7b812-115">This property is an example of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="7b812-116">Когда клиентское приложение отправляет сообщение от имени другого клиента, он должен задать всем представленным свойствам отправителя значения для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="7b812-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="7b812-117">Пользователь обмена сообщениями, который отправляется от собственного имени, обычно оставляет свойства предоставленных отправителей неопределенными.</span><span class="sxs-lookup"><span data-stu-id="7b812-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="7b812-118">Поставщик исходящей транспортировки всегда должен оставить это свойство без изменений, если оно было задано отправляющим клиентом.</span><span class="sxs-lookup"><span data-stu-id="7b812-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="7b812-119">Если это не так, поставщик транспорта должен задать для него свойство **пр_сендер_смтп_аддресс** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) в исходящей копии сообщения и оставить его незаданным для локальной копии.</span><span class="sxs-lookup"><span data-stu-id="7b812-119">If it is unset, the transport provider should set it to the **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7b812-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7b812-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b812-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7b812-121">Protocol specifications</span></span>

<span data-ttu-id="7b812-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b812-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b812-123">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7b812-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7b812-124">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b812-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b812-125">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7b812-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="7b812-126">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b812-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b812-127">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="7b812-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="7b812-128">[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b812-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b812-129">Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="7b812-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="7b812-130">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b812-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b812-131">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="7b812-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="7b812-132">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b812-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b812-133">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="7b812-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="7b812-134">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b812-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b812-135">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="7b812-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="7b812-136">[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b812-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b812-137">Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.</span><span class="sxs-lookup"><span data-stu-id="7b812-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b812-138">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="7b812-138">Header files</span></span>

<span data-ttu-id="7b812-139">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="7b812-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b812-140">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7b812-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="7b812-141">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="7b812-141">Mapitags.h</span></span>
  
> <span data-ttu-id="7b812-142">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="7b812-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b812-143">См. также</span><span class="sxs-lookup"><span data-stu-id="7b812-143">See also</span></span>



[<span data-ttu-id="7b812-144">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7b812-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b812-145">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="7b812-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b812-146">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7b812-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b812-147">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7b812-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

