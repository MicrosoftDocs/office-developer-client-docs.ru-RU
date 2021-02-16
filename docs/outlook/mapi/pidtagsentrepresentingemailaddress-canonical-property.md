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
ms.openlocfilehash: 1b82e1e96a5ffbb5c17dd919e78a9f07342194c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341092"
---
# <a name="pidtagsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="3c0ec-103">Каноническое свойство PidTagSentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3c0ec-103">PidTagSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="3c0ec-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c0ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c0ec-105">Содержит адрес электронной почты пользователя обмена сообщениями, представленного отправищиком.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-105">Contains the email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c0ec-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3c0ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c0ec-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="3c0ec-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="3c0ec-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3c0ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3c0ec-109">0x0065</span><span class="sxs-lookup"><span data-stu-id="3c0ec-109">0x0065</span></span>  <br/> |
|<span data-ttu-id="3c0ec-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3c0ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="3c0ec-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="3c0ec-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="3c0ec-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3c0ec-112">Area:</span></span>  <br/> |<span data-ttu-id="3c0ec-113">Address</span><span class="sxs-lookup"><span data-stu-id="3c0ec-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c0ec-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3c0ec-114">Remarks</span></span>

<span data-ttu-id="3c0ec-115">Эти свойства являются примерами свойств адреса для пользователя обмена сообщениями, представленного отправищиком.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="3c0ec-116">Когда клиентская приложение отправляет сообщение от имени другого клиента, оно должно установить для всех представленных свойств отправитель значения для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="3c0ec-117">Пользователь обмена сообщениями, отправляющий сообщения от своего имени, обычно оставляет представленные свойства отправитель ненамеренными.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="3c0ec-118">Если отправляющий клиент установил эти свойства, эти свойства всегда должны оставаться без изменений.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-118">The outgoing transport provider must always leave these properties unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="3c0ec-119">Если он не затенен, поставщик транспорта должен установить для него свойство **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress)](pidtagsenderemailaddress-canonical-property.md)в исходящие копии сообщения и оставить его ненастроенным для локальной копии.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-119">If it is unset, the transport provider should set it to the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3c0ec-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3c0ec-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c0ec-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3c0ec-121">Protocol specifications</span></span>

<span data-ttu-id="3c0ec-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c0ec-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c0ec-123">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3c0ec-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c0ec-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c0ec-125">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="3c0ec-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c0ec-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c0ec-127">Указывает свойства и операции, которые представляют элементы RSS.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="3c0ec-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c0ec-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c0ec-129">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="3c0ec-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c0ec-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c0ec-131">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="3c0ec-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c0ec-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c0ec-133">Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="3c0ec-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c0ec-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c0ec-135">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="3c0ec-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c0ec-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c0ec-137">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c0ec-138">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="3c0ec-138">Header files</span></span>

<span data-ttu-id="3c0ec-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c0ec-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c0ec-140">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="3c0ec-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3c0ec-141">Mapitags.h</span></span>
  
> <span data-ttu-id="3c0ec-142">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c0ec-143">См. также</span><span class="sxs-lookup"><span data-stu-id="3c0ec-143">See also</span></span>



[<span data-ttu-id="3c0ec-144">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3c0ec-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c0ec-145">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3c0ec-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c0ec-146">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3c0ec-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c0ec-147">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3c0ec-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

