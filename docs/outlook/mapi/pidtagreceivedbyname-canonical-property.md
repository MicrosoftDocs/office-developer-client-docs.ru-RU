---
title: Каноническое свойство PidTagReceivedByName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByName
api_type:
- COM
ms.assetid: edd29217-74bb-4321-82fd-65f0fbfd05f8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 039a51c2bb4cf1fe2a83e2ba144a87462b5d6d0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359215"
---
# <a name="pidtagreceivedbyname-canonical-property"></a><span data-ttu-id="2f3f6-103">Каноническое свойство PidTagReceivedByName</span><span class="sxs-lookup"><span data-stu-id="2f3f6-103">PidTagReceivedByName Canonical Property</span></span>

  
  
<span data-ttu-id="2f3f6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f3f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f3f6-105">Содержит отображаемую фамилию пользователя сообщения, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-105">Contains the display name of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2f3f6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2f3f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2f3f6-107">PR_RECEIVED_BY_NAME, PR_RECEIVED_BY_NAME_A, PR_RECEIVED_BY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="2f3f6-107">PR_RECEIVED_BY_NAME, PR_RECEIVED_BY_NAME_A, PR_RECEIVED_BY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="2f3f6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2f3f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2f3f6-109">0x0040</span><span class="sxs-lookup"><span data-stu-id="2f3f6-109">0x0040</span></span>  <br/> |
|<span data-ttu-id="2f3f6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2f3f6-110">Data type:</span></span>  <br/> |<span data-ttu-id="2f3f6-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="2f3f6-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="2f3f6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2f3f6-112">Area:</span></span>  <br/> |<span data-ttu-id="2f3f6-113">Address</span><span class="sxs-lookup"><span data-stu-id="2f3f6-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f3f6-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f3f6-114">Remarks</span></span>

<span data-ttu-id="2f3f6-115">Эти свойства являются примером свойств адреса для пользователя сообщения, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-115">These properties are an example of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="2f3f6-116">Их должен установить поставщик входящих транспортных услуг.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-116">They must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2f3f6-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2f3f6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2f3f6-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2f3f6-118">Protocol specifications</span></span>

<span data-ttu-id="2f3f6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f3f6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f3f6-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2f3f6-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f3f6-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f3f6-122">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="2f3f6-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f3f6-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f3f6-124">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="2f3f6-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f3f6-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f3f6-126">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="2f3f6-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f3f6-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f3f6-128">Указывает методы подключения и настройки почтовых ящиков в качестве делегатов, а также взаимодействия с объектами сообщений и календаря, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="2f3f6-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f3f6-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f3f6-130">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2f3f6-131">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="2f3f6-131">Header files</span></span>

<span data-ttu-id="2f3f6-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2f3f6-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="2f3f6-133">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="2f3f6-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2f3f6-134">Mapitags.h</span></span>
  
> <span data-ttu-id="2f3f6-135">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="2f3f6-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f3f6-136">См. также</span><span class="sxs-lookup"><span data-stu-id="2f3f6-136">See also</span></span>



[<span data-ttu-id="2f3f6-137">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="2f3f6-137">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="2f3f6-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2f3f6-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2f3f6-139">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2f3f6-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2f3f6-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2f3f6-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2f3f6-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2f3f6-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

