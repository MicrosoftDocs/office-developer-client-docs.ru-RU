---
title: Каноническое свойство PidTagSentRepresentingAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingAddressType
api_type:
- COM
ms.assetid: 6ecbf653-1faf-47bd-81a4-20157859fdfd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a58ae878ba13415823e61db3b1717e3cf07f29c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811895"
---
# <a name="pidtagsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="0e0e4-103">Каноническое свойство PidTagSentRepresentingAddressType</span><span class="sxs-lookup"><span data-stu-id="0e0e4-103">PidTagSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="0e0e4-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e0e4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e0e4-105">Содержит тип адреса для обмена мгновенными сообщениями пользователя, который представлен отправителем.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-105">Contains the address type for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e0e4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0e0e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e0e4-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="0e0e4-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="0e0e4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0e0e4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e0e4-109">0x0064</span><span class="sxs-lookup"><span data-stu-id="0e0e4-109">0x0064</span></span>  <br/> |
|<span data-ttu-id="0e0e4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0e0e4-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e0e4-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="0e0e4-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="0e0e4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0e0e4-112">Area:</span></span>  <br/> |<span data-ttu-id="0e0e4-113">Address</span><span class="sxs-lookup"><span data-stu-id="0e0e4-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e0e4-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="0e0e4-114">Remarks</span></span>

<span data-ttu-id="0e0e4-115">Эти свойства являются примерами свойства адреса для обмена мгновенными сообщениями, представленному отправителя пользователя.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="0e0e4-116">Когда клиентское приложение отправляет сообщения от имени другого клиента, его следует устанавливать все свойства представленного отправителя значения для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="0e0e4-117">Обмена сообщениями при отправке на собственный имени обычно оставляет свойства представленного отправителя удалить.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="0e0e4-118">Исходящие поставщика транспорта всегда необходимо оставить это свойство без изменений, если он имеет значение с клиента.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="0e0e4-119">Если оно не установлено, поставщика транспорта должен установить значение свойства **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) в исходящих копии сообщения и оставить неопределенные на локальной копии.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-119">If it is unset, the transport provider should set it to the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0e0e4-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0e0e4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e0e4-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0e0e4-121">Protocol specifications</span></span>

<span data-ttu-id="0e0e4-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e0e4-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e0e4-123">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e0e4-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e0e4-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e0e4-125">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="0e0e4-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e0e4-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e0e4-127">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="0e0e4-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e0e4-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e0e4-129">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-129">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="0e0e4-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e0e4-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e0e4-131">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="0e0e4-132">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e0e4-132">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e0e4-133">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="0e0e4-134">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e0e4-134">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e0e4-135">Указывает, что свойства и операции, допустимые для учета объекты.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="0e0e4-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e0e4-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e0e4-137">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="0e0e4-138">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e0e4-138">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e0e4-139">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-139">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e0e4-140">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0e0e4-140">Header files</span></span>

<span data-ttu-id="0e0e4-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e0e4-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e0e4-142">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e0e4-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0e0e4-143">Mapitags.h</span></span>
  
> <span data-ttu-id="0e0e4-144">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="0e0e4-144">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e0e4-145">См. также</span><span class="sxs-lookup"><span data-stu-id="0e0e4-145">See also</span></span>



[<span data-ttu-id="0e0e4-146">Каноническое свойство PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="0e0e4-146">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)


[<span data-ttu-id="0e0e4-147">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0e0e4-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e0e4-148">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0e0e4-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e0e4-149">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0e0e4-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e0e4-150">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0e0e4-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

