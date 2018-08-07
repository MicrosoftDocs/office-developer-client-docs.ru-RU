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
ms.openlocfilehash: 5417b73fe13937a74bc01520a2dd9db359e894ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811911"
---
# <a name="pidtagsentrepresentingname-canonical-property"></a><span data-ttu-id="796e9-103">Каноническое свойство PidTagSentRepresentingName</span><span class="sxs-lookup"><span data-stu-id="796e9-103">PidTagSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="796e9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="796e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="796e9-105">Содержит отображаемое имя для обмена сообщениями пользователя, представленного отправителя.</span><span class="sxs-lookup"><span data-stu-id="796e9-105">Contains the display name for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="796e9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="796e9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="796e9-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="796e9-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="796e9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="796e9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="796e9-109">0x0042</span><span class="sxs-lookup"><span data-stu-id="796e9-109">0x0042</span></span>  <br/> |
|<span data-ttu-id="796e9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="796e9-110">Data type:</span></span>  <br/> |<span data-ttu-id="796e9-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="796e9-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="796e9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="796e9-112">Area:</span></span>  <br/> |<span data-ttu-id="796e9-113">Address</span><span class="sxs-lookup"><span data-stu-id="796e9-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="796e9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="796e9-114">Remarks</span></span>

<span data-ttu-id="796e9-115">Эти свойства являются примерами свойства адреса для обмена мгновенными сообщениями, представленному отправителя пользователя.</span><span class="sxs-lookup"><span data-stu-id="796e9-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="796e9-116">Когда клиентское приложение отправляет сообщения от имени другого клиента, его следует устанавливать все свойства представленного отправителя значения для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="796e9-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="796e9-117">Обмена сообщениями при отправке на собственный имени обычно оставляет свойства представленного отправителя удалить.</span><span class="sxs-lookup"><span data-stu-id="796e9-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="796e9-118">Исходящие поставщика транспорта всегда необходимо оставить это свойство без изменений, если он имеет значение с клиента.</span><span class="sxs-lookup"><span data-stu-id="796e9-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="796e9-119">Если оно не установлено, поставщика транспорта должен установить значение **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) в исходящих копии сообщения и оставить неопределенные на локальной копии.</span><span class="sxs-lookup"><span data-stu-id="796e9-119">If it is unset, the transport provider should set it to **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="796e9-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="796e9-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="796e9-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="796e9-121">Protocol specifications</span></span>

<span data-ttu-id="796e9-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="796e9-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="796e9-123">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="796e9-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="796e9-124">[[MS-OXOMSG]](http://msdn.microsoft.com/en-us/library/cc433482%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="796e9-124">[[MS-OXOMSG]](http://msdn.microsoft.com/en-us/library/cc433482%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="796e9-125">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="796e9-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="796e9-126">[[MS-OXORSS]](http://msdn.microsoft.com/en-us/library/cc463884%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="796e9-126">[[MS-OXORSS]](http://msdn.microsoft.com/en-us/library/cc463884%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="796e9-127">Задает свойства и операции, которые представляют элементам RSS-Каналов.</span><span class="sxs-lookup"><span data-stu-id="796e9-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="796e9-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="796e9-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="796e9-129">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="796e9-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="796e9-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="796e9-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="796e9-131">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="796e9-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="796e9-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="796e9-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="796e9-133">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="796e9-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="796e9-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="796e9-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="796e9-135">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="796e9-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="796e9-136">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="796e9-136">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="796e9-137">Указывает расположение и свойства клиентских и серверных данных конфигурации, такие как списки общие категории и рабочее время.</span><span class="sxs-lookup"><span data-stu-id="796e9-137">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="796e9-138">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="796e9-138">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="796e9-139">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="796e9-139">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="796e9-140">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="796e9-140">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="796e9-141">Указывает, что свойства и операции, допустимые для учета объекты.</span><span class="sxs-lookup"><span data-stu-id="796e9-141">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="796e9-142">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="796e9-142">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="796e9-143">Задает свойства и операции, допустимые для объектов списка рассылки и контактов.</span><span class="sxs-lookup"><span data-stu-id="796e9-143">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="796e9-144">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="796e9-144">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="796e9-145">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="796e9-145">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="796e9-146">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="796e9-146">Header files</span></span>

<span data-ttu-id="796e9-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="796e9-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="796e9-148">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="796e9-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="796e9-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="796e9-149">Mapitags.h</span></span>
  
> <span data-ttu-id="796e9-150">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="796e9-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="796e9-151">См. также</span><span class="sxs-lookup"><span data-stu-id="796e9-151">See also</span></span>



[<span data-ttu-id="796e9-152">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="796e9-152">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="796e9-153">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="796e9-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="796e9-154">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="796e9-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="796e9-155">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="796e9-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="796e9-156">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="796e9-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

