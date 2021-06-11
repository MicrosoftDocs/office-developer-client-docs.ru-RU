---
title: Каноническое свойство PidTagSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 7a49b944-cef1-4642-9208-b137fd61171a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a9361f3027453742acbe50c3de01d860289cd0ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356688"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="9e5b8-103">Каноническое свойство PidTagSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="9e5b8-103">PidTagSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="9e5b8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e5b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e5b8-105">Содержит ключ поиска для пользователя обмена сообщениями, представленного отправивщиком.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-105">Contains the search key for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9e5b8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9e5b8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9e5b8-107">PR_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="9e5b8-107">PR_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="9e5b8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9e5b8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9e5b8-109">0x003B</span><span class="sxs-lookup"><span data-stu-id="9e5b8-109">0x003B</span></span>  <br/> |
|<span data-ttu-id="9e5b8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9e5b8-110">Data type:</span></span>  <br/> |<span data-ttu-id="9e5b8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9e5b8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9e5b8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9e5b8-112">Area:</span></span>  <br/> |<span data-ttu-id="9e5b8-113">Адрес</span><span class="sxs-lookup"><span data-stu-id="9e5b8-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e5b8-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e5b8-114">Remarks</span></span>

<span data-ttu-id="9e5b8-115">Это свойство является одним из свойств адресов для пользователя обмена сообщениями, который представляет отправитель.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-115">This property is one of the address properties for the messaging user who is being represented by the sender.</span></span> <span data-ttu-id="9e5b8-116">Когда клиентская заявка отправляет сообщение от имени другого клиента, оно должно установить все представленные свойства отправитель к значениям для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="9e5b8-117">Пользователь обмена сообщениями, отправляющий сообщения от своего имени, обычно оставляет представленные свойства отправитель неустановленными.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="9e5b8-118">Исходяющий поставщик транспорта всегда должен оставить это свойство без изменений, если оно было заданной клиентом отправки.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="9e5b8-119">Если оно не установлено, поставщик транспорта  должен установить его PR_SENDER_SEARCH_KEY[(PidTagSenderSearchKey)](pidtagsendersearchkey-canonical-property.md)в исходящие копии сообщения и оставить его неустановленным в локальной копии.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-119">If it is unset, the transport provider should set it to **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9e5b8-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9e5b8-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9e5b8-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9e5b8-121">Protocol specifications</span></span>

<span data-ttu-id="9e5b8-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e5b8-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e5b8-123">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9e5b8-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e5b8-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e5b8-125">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="9e5b8-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e5b8-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e5b8-127">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="9e5b8-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e5b8-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e5b8-129">Преобразования между объектами IETF RFC2445, RFC2446 и RFC2447, а также объектами назначения и собраний.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="9e5b8-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e5b8-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e5b8-131">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="9e5b8-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e5b8-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e5b8-133">Указывает свойства и операции, допустимые для почтовых объектов.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-133">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="9e5b8-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e5b8-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e5b8-135">Указывает свойства и операции, допустимые для списков контактов и личных рассылк.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-135">Specifies the properties and operations that are permissible for contact and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9e5b8-136">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="9e5b8-136">Header files</span></span>

<span data-ttu-id="9e5b8-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e5b8-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="9e5b8-138">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="9e5b8-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9e5b8-139">Mapitags.h</span></span>
  
> <span data-ttu-id="9e5b8-140">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e5b8-141">См. также</span><span class="sxs-lookup"><span data-stu-id="9e5b8-141">See also</span></span>



[<span data-ttu-id="9e5b8-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9e5b8-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9e5b8-143">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9e5b8-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9e5b8-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9e5b8-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9e5b8-145">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="9e5b8-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

