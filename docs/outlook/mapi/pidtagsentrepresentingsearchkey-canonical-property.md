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
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="9df64-103">Каноническое свойство PidTagSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="9df64-103">PidTagSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="9df64-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9df64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9df64-105">Содержит ключ поиска для пользователя обмена сообщениями, представленного отправищиком.</span><span class="sxs-lookup"><span data-stu-id="9df64-105">Contains the search key for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9df64-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9df64-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9df64-107">PR_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="9df64-107">PR_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="9df64-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9df64-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9df64-109">0x003B</span><span class="sxs-lookup"><span data-stu-id="9df64-109">0x003B</span></span>  <br/> |
|<span data-ttu-id="9df64-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9df64-110">Data type:</span></span>  <br/> |<span data-ttu-id="9df64-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9df64-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9df64-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9df64-112">Area:</span></span>  <br/> |<span data-ttu-id="9df64-113">Address</span><span class="sxs-lookup"><span data-stu-id="9df64-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9df64-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9df64-114">Remarks</span></span>

<span data-ttu-id="9df64-115">Это свойство является одним из свойств адреса для пользователя обмена сообщениями, представленного отправищиком.</span><span class="sxs-lookup"><span data-stu-id="9df64-115">This property is one of the address properties for the messaging user who is being represented by the sender.</span></span> <span data-ttu-id="9df64-116">Когда клиентская приложение отправляет сообщение от имени другого клиента, оно должно установить для всех представленных свойств отправитель значения для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="9df64-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="9df64-117">Пользователь обмена сообщениями, отправляющий сообщения от своего имени, обычно оставляет представленные свойства отправитель ненамеренными.</span><span class="sxs-lookup"><span data-stu-id="9df64-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="9df64-118">Отправляющий клиент всегда должен оставить это свойство без изменений.</span><span class="sxs-lookup"><span data-stu-id="9df64-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="9df64-119">Если он не затенен, поставщик транспорта должен установить для него PR_SENDER_SEARCH_KEY **(** [PidTagSenderSearchKey)](pidtagsendersearchkey-canonical-property.md)в исходящие копии сообщения и оставить его ненастроенным в локальной копии.</span><span class="sxs-lookup"><span data-stu-id="9df64-119">If it is unset, the transport provider should set it to **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9df64-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9df64-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9df64-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9df64-121">Protocol specifications</span></span>

<span data-ttu-id="9df64-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9df64-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9df64-123">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="9df64-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9df64-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9df64-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9df64-125">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9df64-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="9df64-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9df64-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9df64-127">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="9df64-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="9df64-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9df64-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9df64-129">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="9df64-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="9df64-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9df64-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9df64-131">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="9df64-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="9df64-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9df64-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9df64-133">Указывает свойства и операции, которые разрешены для объектов post.</span><span class="sxs-lookup"><span data-stu-id="9df64-133">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="9df64-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9df64-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9df64-135">Указывает свойства и операции, которые разрешены для списков контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="9df64-135">Specifies the properties and operations that are permissible for contact and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9df64-136">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="9df64-136">Header files</span></span>

<span data-ttu-id="9df64-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9df64-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="9df64-138">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9df64-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="9df64-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9df64-139">Mapitags.h</span></span>
  
> <span data-ttu-id="9df64-140">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="9df64-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9df64-141">См. также</span><span class="sxs-lookup"><span data-stu-id="9df64-141">See also</span></span>



[<span data-ttu-id="9df64-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9df64-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9df64-143">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9df64-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9df64-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9df64-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9df64-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9df64-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

