---
title: Каноническое свойство PidTagSentRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: bfee6c5e-d4c6-442e-af71-23156569fed5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8e2df13f4e9c5d1d636c4f71ea6805ac031899e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314933"
---
# <a name="pidtagsentrepresentingname-canonical-property"></a><span data-ttu-id="8be93-103">Каноническое свойство PidTagSentRepresentingName</span><span class="sxs-lookup"><span data-stu-id="8be93-103">PidTagSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="8be93-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8be93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8be93-105">Содержит отображаемое имя пользователя обмена сообщениями, представленного отправителем.</span><span class="sxs-lookup"><span data-stu-id="8be93-105">Contains the display name for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8be93-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8be93-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8be93-107">ПР_СЕНТ_РЕПРЕСЕНТИНГ_НАМЕ, ПР_СЕНТ_РЕПРЕСЕНТИНГ_НАМЕ_А, ПР_СЕНТ_РЕПРЕСЕНТИНГ_НАМЕ_В</span><span class="sxs-lookup"><span data-stu-id="8be93-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="8be93-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8be93-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8be93-109">0x0042</span><span class="sxs-lookup"><span data-stu-id="8be93-109">0x0042</span></span>  <br/> |
|<span data-ttu-id="8be93-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8be93-110">Data type:</span></span>  <br/> |<span data-ttu-id="8be93-111">ПТ_УНИКОДЕ, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="8be93-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="8be93-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8be93-112">Area:</span></span>  <br/> |<span data-ttu-id="8be93-113">Address</span><span class="sxs-lookup"><span data-stu-id="8be93-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8be93-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8be93-114">Remarks</span></span>

<span data-ttu-id="8be93-115">Эти свойства являются примерами свойств адресов для пользователя обмена сообщениями, представленного отправителями.</span><span class="sxs-lookup"><span data-stu-id="8be93-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="8be93-116">Когда клиентское приложение отправляет сообщение от имени другого клиента, он должен задать всем представленным свойствам отправителя значения для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="8be93-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="8be93-117">Пользователь обмена сообщениями, который отправляется от собственного имени, обычно оставляет свойства предоставленных отправителей неопределенными.</span><span class="sxs-lookup"><span data-stu-id="8be93-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="8be93-118">Поставщик исходящей транспортировки всегда должен оставить это свойство без изменений, если оно было задано отправляющим клиентом.</span><span class="sxs-lookup"><span data-stu-id="8be93-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="8be93-119">Если это не так, поставщик транспорта должен задать для него значение **пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md)) в исходящей копии сообщения и оставить его незаданным для локальной копии.</span><span class="sxs-lookup"><span data-stu-id="8be93-119">If it is unset, the transport provider should set it to **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8be93-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8be93-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8be93-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8be93-121">Protocol specifications</span></span>

<span data-ttu-id="8be93-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8be93-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8be93-123">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8be93-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8be93-124">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8be93-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="8be93-125">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8be93-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8be93-126">[[MS — ОКСОРСС]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8be93-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="8be93-127">Задает свойства и операции, представляющие элементы RSS.</span><span class="sxs-lookup"><span data-stu-id="8be93-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="8be93-128">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8be93-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8be93-129">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="8be93-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8be93-130">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8be93-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8be93-131">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="8be93-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8be93-132">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8be93-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8be93-133">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="8be93-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="8be93-134">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8be93-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8be93-135">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="8be93-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="8be93-136">[[MS — ОКСОКФГ]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8be93-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8be93-137">Задает расположение и свойства данных конфигурации клиента и сервера, например списки общих категорий и рабочие часы.</span><span class="sxs-lookup"><span data-stu-id="8be93-137">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="8be93-138">[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8be93-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8be93-139">Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="8be93-139">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="8be93-140">[[MS — ОКСОПОСТ]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8be93-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8be93-141">Задает свойства и операции, допустимые для объектов POST.</span><span class="sxs-lookup"><span data-stu-id="8be93-141">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="8be93-142">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8be93-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8be93-143">Задает свойства и операции, которые являются допустимыми для объектов контакта и личного списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="8be93-143">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="8be93-144">[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8be93-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8be93-145">Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.</span><span class="sxs-lookup"><span data-stu-id="8be93-145">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8be93-146">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="8be93-146">Header files</span></span>

<span data-ttu-id="8be93-147">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8be93-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="8be93-148">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8be93-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="8be93-149">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="8be93-149">Mapitags.h</span></span>
  
> <span data-ttu-id="8be93-150">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="8be93-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8be93-151">См. также</span><span class="sxs-lookup"><span data-stu-id="8be93-151">See also</span></span>



[<span data-ttu-id="8be93-152">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="8be93-152">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="8be93-153">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8be93-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8be93-154">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="8be93-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8be93-155">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8be93-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8be93-156">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8be93-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

