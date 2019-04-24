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
ms.openlocfilehash: bbf1ae0d7b38886fe08af2ad13f1a2be6b6e01cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342576"
---
# <a name="pidtagsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="e9809-103">Каноническое свойство PidTagSentRepresentingAddressType</span><span class="sxs-lookup"><span data-stu-id="e9809-103">PidTagSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="e9809-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9809-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9809-105">Содержит тип адреса пользователя обмена сообщениями, представленного отправителем.</span><span class="sxs-lookup"><span data-stu-id="e9809-105">Contains the address type for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9809-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e9809-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9809-107">ПР_СЕНТ_РЕПРЕСЕНТИНГ_АДДРТИПЕ, ПР_СЕНТ_РЕПРЕСЕНТИНГ_АДДРТИПЕ_А, ПР_СЕНТ_РЕПРЕСЕНТИНГ_АДДРТИПЕ_В</span><span class="sxs-lookup"><span data-stu-id="e9809-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="e9809-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e9809-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9809-109">0x0064</span><span class="sxs-lookup"><span data-stu-id="e9809-109">0x0064</span></span>  <br/> |
|<span data-ttu-id="e9809-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e9809-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9809-111">ПТ_УНИКОДЕ, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="e9809-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="e9809-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e9809-112">Area:</span></span>  <br/> |<span data-ttu-id="e9809-113">Address</span><span class="sxs-lookup"><span data-stu-id="e9809-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9809-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9809-114">Remarks</span></span>

<span data-ttu-id="e9809-115">Эти свойства являются примерами свойств адресов для пользователя обмена сообщениями, представленного отправителями.</span><span class="sxs-lookup"><span data-stu-id="e9809-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="e9809-116">Когда клиентское приложение отправляет сообщение от имени другого клиента, он должен задать всем представленным свойствам отправителя значения для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="e9809-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="e9809-117">Пользователь обмена сообщениями, который отправляется от собственного имени, обычно оставляет свойства предоставленных отправителей неопределенными.</span><span class="sxs-lookup"><span data-stu-id="e9809-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="e9809-118">Поставщик исходящей транспортировки всегда должен оставить это свойство без изменений, если оно было задано отправляющим клиентом.</span><span class="sxs-lookup"><span data-stu-id="e9809-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="e9809-119">Если это не так, поставщик транспорта должен задать для него свойство **пр_сендер_аддртипе** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) в исходящей копии сообщения и оставить его незаданным для локальной копии.</span><span class="sxs-lookup"><span data-stu-id="e9809-119">If it is unset, the transport provider should set it to the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e9809-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e9809-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9809-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e9809-121">Protocol specifications</span></span>

<span data-ttu-id="e9809-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9809-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9809-123">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e9809-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e9809-124">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9809-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9809-125">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="e9809-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e9809-126">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9809-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9809-127">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="e9809-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e9809-128">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9809-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9809-129">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="e9809-129">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="e9809-130">[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9809-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9809-131">Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="e9809-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="e9809-132">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9809-132">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9809-133">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e9809-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="e9809-134">[[MS — ОКСОПОСТ]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9809-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9809-135">Задает свойства и операции, допустимые для объектов POST.</span><span class="sxs-lookup"><span data-stu-id="e9809-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="e9809-136">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9809-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9809-137">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="e9809-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="e9809-138">[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9809-138">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9809-139">Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.</span><span class="sxs-lookup"><span data-stu-id="e9809-139">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9809-140">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="e9809-140">Header files</span></span>

<span data-ttu-id="e9809-141">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="e9809-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9809-142">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e9809-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9809-143">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="e9809-143">Mapitags.h</span></span>
  
> <span data-ttu-id="e9809-144">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="e9809-144">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9809-145">См. также</span><span class="sxs-lookup"><span data-stu-id="e9809-145">See also</span></span>



[<span data-ttu-id="e9809-146">Каноническое свойство PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="e9809-146">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)


[<span data-ttu-id="e9809-147">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e9809-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9809-148">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="e9809-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9809-149">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e9809-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9809-150">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e9809-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

