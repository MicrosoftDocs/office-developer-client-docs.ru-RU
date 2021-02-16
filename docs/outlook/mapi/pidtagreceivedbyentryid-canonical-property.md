---
title: Каноническое свойство PidTagReceivedByEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEntryId
api_type:
- COM
ms.assetid: 737f8584-fc52-4324-ac40-2fc554a3095d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2f0203fc787ced9a0198be10c238f6245cb15144
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359222"
---
# <a name="pidtagreceivedbyentryid-canonical-property"></a><span data-ttu-id="0642a-103">Каноническое свойство PidTagReceivedByEntryId</span><span class="sxs-lookup"><span data-stu-id="0642a-103">PidTagReceivedByEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="0642a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0642a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0642a-105">Содержит идентификатор записи пользователя обмена сообщениями, который фактически получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="0642a-105">Contains the entry identifier of the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0642a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0642a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0642a-107">PR_RECEIVED_BY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0642a-107">PR_RECEIVED_BY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="0642a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0642a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0642a-109">0x003F</span><span class="sxs-lookup"><span data-stu-id="0642a-109">0x003F</span></span>  <br/> |
|<span data-ttu-id="0642a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0642a-110">Data type:</span></span>  <br/> |<span data-ttu-id="0642a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0642a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0642a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0642a-112">Area:</span></span>  <br/> |<span data-ttu-id="0642a-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="0642a-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0642a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0642a-114">Remarks</span></span>

<span data-ttu-id="0642a-115">Это свойство является одним из свойств адреса для пользователя сообщения, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="0642a-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="0642a-116">Его должен установить поставщик входящих транспортных услуг.</span><span class="sxs-lookup"><span data-stu-id="0642a-116">It must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="0642a-117">Это свойство соответствует атрибуту конверта доставки X.400 для каждого MH_T_ сообщения.</span><span class="sxs-lookup"><span data-stu-id="0642a-117">This property corresponds to an X.400 delivery envelope per-message MH_T_ attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0642a-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0642a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0642a-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0642a-119">Protocol specifications</span></span>

<span data-ttu-id="0642a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0642a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0642a-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="0642a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0642a-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0642a-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0642a-123">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0642a-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="0642a-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0642a-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0642a-125">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="0642a-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="0642a-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0642a-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0642a-127">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также элементами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="0642a-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
<span data-ttu-id="0642a-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0642a-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0642a-129">Указывает методы подключения и настройки почтовых ящиков в качестве делегатов, а также взаимодействия с объектами сообщений и календаря, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="0642a-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="0642a-130">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0642a-130">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0642a-131">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="0642a-131">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0642a-132">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="0642a-132">Header files</span></span>

<span data-ttu-id="0642a-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0642a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="0642a-134">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0642a-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="0642a-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0642a-135">Mapitags.h</span></span>
  
> <span data-ttu-id="0642a-136">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="0642a-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0642a-137">См. также</span><span class="sxs-lookup"><span data-stu-id="0642a-137">See also</span></span>



[<span data-ttu-id="0642a-138">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="0642a-138">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="0642a-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0642a-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0642a-140">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0642a-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0642a-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0642a-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0642a-142">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0642a-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

