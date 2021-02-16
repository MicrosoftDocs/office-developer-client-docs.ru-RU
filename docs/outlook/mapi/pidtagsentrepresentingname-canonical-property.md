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
# <a name="pidtagsentrepresentingname-canonical-property"></a><span data-ttu-id="318a6-103">Каноническое свойство PidTagSentRepresentingName</span><span class="sxs-lookup"><span data-stu-id="318a6-103">PidTagSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="318a6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="318a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="318a6-105">Содержит отображаемую имя пользователя обмена сообщениями, представленного отправищиком.</span><span class="sxs-lookup"><span data-stu-id="318a6-105">Contains the display name for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="318a6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="318a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="318a6-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="318a6-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="318a6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="318a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="318a6-109">0x0042</span><span class="sxs-lookup"><span data-stu-id="318a6-109">0x0042</span></span>  <br/> |
|<span data-ttu-id="318a6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="318a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="318a6-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="318a6-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="318a6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="318a6-112">Area:</span></span>  <br/> |<span data-ttu-id="318a6-113">Address</span><span class="sxs-lookup"><span data-stu-id="318a6-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="318a6-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="318a6-114">Remarks</span></span>

<span data-ttu-id="318a6-115">Эти свойства являются примерами свойств адреса для пользователя обмена сообщениями, представленного отправищиком.</span><span class="sxs-lookup"><span data-stu-id="318a6-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="318a6-116">Когда клиентская приложение отправляет сообщение от имени другого клиента, оно должно установить для всех представленных свойств отправитель значения для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="318a6-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="318a6-117">Пользователь обмена сообщениями, отправляющий сообщения от своего имени, обычно оставляет представленные свойства отправитель ненамеренными.</span><span class="sxs-lookup"><span data-stu-id="318a6-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="318a6-118">Отправляющий клиент всегда должен оставить это свойство без изменений.</span><span class="sxs-lookup"><span data-stu-id="318a6-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="318a6-119">Если он не затенен, поставщик  транспорта должен установить для него PR_SENDER_NAME[(PidTagSenderName)](pidtagsendername-canonical-property.md)в исходящие копии сообщения и оставить его ненастроенным в локальной копии.</span><span class="sxs-lookup"><span data-stu-id="318a6-119">If it is unset, the transport provider should set it to **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="318a6-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="318a6-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="318a6-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="318a6-121">Protocol specifications</span></span>

<span data-ttu-id="318a6-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="318a6-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="318a6-123">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="318a6-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="318a6-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="318a6-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="318a6-125">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="318a6-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="318a6-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="318a6-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="318a6-127">Указывает свойства и операции, которые представляют элементы RSS.</span><span class="sxs-lookup"><span data-stu-id="318a6-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="318a6-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="318a6-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="318a6-129">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="318a6-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="318a6-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="318a6-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="318a6-131">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="318a6-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="318a6-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="318a6-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="318a6-133">Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="318a6-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="318a6-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="318a6-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="318a6-135">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="318a6-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="318a6-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="318a6-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="318a6-137">Указывает расположение и свойства данных конфигурации клиента и сервера, например списки общих категорий и рабочие часы.</span><span class="sxs-lookup"><span data-stu-id="318a6-137">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="318a6-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="318a6-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="318a6-139">Указывает методы подключения и настройки почтовых ящиков в качестве делегатов, а также взаимодействия с объектами сообщений и календаря, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="318a6-139">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="318a6-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="318a6-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="318a6-141">Указывает свойства и операции, которые разрешены для объектов post.</span><span class="sxs-lookup"><span data-stu-id="318a6-141">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="318a6-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="318a6-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="318a6-143">Указывает свойства и операции, которые разрешены для объектов контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="318a6-143">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="318a6-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="318a6-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="318a6-145">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="318a6-145">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="318a6-146">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="318a6-146">Header files</span></span>

<span data-ttu-id="318a6-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="318a6-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="318a6-148">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="318a6-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="318a6-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="318a6-149">Mapitags.h</span></span>
  
> <span data-ttu-id="318a6-150">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="318a6-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="318a6-151">См. также</span><span class="sxs-lookup"><span data-stu-id="318a6-151">See also</span></span>



[<span data-ttu-id="318a6-152">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="318a6-152">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="318a6-153">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="318a6-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="318a6-154">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="318a6-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="318a6-155">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="318a6-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="318a6-156">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="318a6-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

