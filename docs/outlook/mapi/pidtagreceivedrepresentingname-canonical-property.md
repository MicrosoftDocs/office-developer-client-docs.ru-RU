---
title: Каноническое свойство PidTagReceivedRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingName
api_type:
- COM
ms.assetid: 8f699782-8a82-4834-bc55-a0b3cf18a117
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5fce7e6d2163bdb8d1682dbef10d627b34ddd889
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356737"
---
# <a name="pidtagreceivedrepresentingname-canonical-property"></a><span data-ttu-id="db6df-103">Каноническое свойство PidTagReceivedRepresentingName</span><span class="sxs-lookup"><span data-stu-id="db6df-103">PidTagReceivedRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="db6df-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db6df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db6df-105">Содержит отображаемую фамилию пользователя обмена сообщениями, представленного принимающим пользователем.</span><span class="sxs-lookup"><span data-stu-id="db6df-105">Contains the display name for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db6df-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="db6df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="db6df-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="db6df-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="db6df-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="db6df-108">Identifier:</span></span>  <br/> |<span data-ttu-id="db6df-109">0x0044</span><span class="sxs-lookup"><span data-stu-id="db6df-109">0x0044</span></span>  <br/> |
|<span data-ttu-id="db6df-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="db6df-110">Data type:</span></span>  <br/> |<span data-ttu-id="db6df-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="db6df-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="db6df-112">Область:</span><span class="sxs-lookup"><span data-stu-id="db6df-112">Area:</span></span>  <br/> |<span data-ttu-id="db6df-113">Address</span><span class="sxs-lookup"><span data-stu-id="db6df-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db6df-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="db6df-114">Remarks</span></span>

<span data-ttu-id="db6df-115">Эти свойства являются примерами свойств адреса для пользователя обмена сообщениями, представленного принимающим пользователем.</span><span class="sxs-lookup"><span data-stu-id="db6df-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="db6df-116">Их должен установить поставщик входящих транспортных услуг, который также отвечает за авторизацию или проверку делегата.</span><span class="sxs-lookup"><span data-stu-id="db6df-116">They must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="db6df-117">Если пользователь обмена сообщениями не представлен, для этих свойств следует установить отображаемую имя, **содержаноеся** в свойстве PR_RECEIVED_BY_NAME ([PidTagReceivedByName).](pidtagreceivedbyname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db6df-117">If no messaging user is being represented, these properties should be set to the display name contained in the **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="db6df-118">Клиентская приложение, отвечая на сообщение, полученное от имени другого клиента, должно скопировать эти свойства из полученного сообщения в свойство **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)для ответа.</span><span class="sxs-lookup"><span data-stu-id="db6df-118">A client application replying to a message received on behalf of another client should copy these properties from the received message into the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="db6df-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="db6df-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="db6df-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="db6df-120">Protocol specifications</span></span>

<span data-ttu-id="db6df-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db6df-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db6df-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="db6df-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="db6df-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db6df-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db6df-124">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="db6df-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="db6df-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db6df-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db6df-126">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="db6df-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="db6df-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db6df-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db6df-128">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="db6df-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="db6df-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db6df-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db6df-130">Указывает методы подключения и настройки почтовых ящиков в качестве делегатов, а также взаимодействия с объектами сообщений и календаря, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="db6df-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="db6df-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db6df-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db6df-132">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="db6df-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="db6df-133">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="db6df-133">Header files</span></span>

<span data-ttu-id="db6df-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="db6df-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="db6df-135">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="db6df-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="db6df-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="db6df-136">Mapitags.h</span></span>
  
> <span data-ttu-id="db6df-137">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="db6df-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db6df-138">См. также</span><span class="sxs-lookup"><span data-stu-id="db6df-138">See also</span></span>



[<span data-ttu-id="db6df-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="db6df-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="db6df-140">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="db6df-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="db6df-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="db6df-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="db6df-142">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="db6df-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

