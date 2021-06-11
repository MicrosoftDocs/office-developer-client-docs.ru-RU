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
# <a name="pidtagreceivedrepresentingname-canonical-property"></a><span data-ttu-id="72876-103">Каноническое свойство PidTagReceivedRepresentingName</span><span class="sxs-lookup"><span data-stu-id="72876-103">PidTagReceivedRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="72876-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72876-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72876-105">Содержит имя отображения для пользователя обмена сообщениями, который представлен принимающим пользователем.</span><span class="sxs-lookup"><span data-stu-id="72876-105">Contains the display name for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72876-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="72876-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72876-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="72876-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="72876-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="72876-108">Identifier:</span></span>  <br/> |<span data-ttu-id="72876-109">0x0044</span><span class="sxs-lookup"><span data-stu-id="72876-109">0x0044</span></span>  <br/> |
|<span data-ttu-id="72876-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="72876-110">Data type:</span></span>  <br/> |<span data-ttu-id="72876-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="72876-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="72876-112">Область:</span><span class="sxs-lookup"><span data-stu-id="72876-112">Area:</span></span>  <br/> |<span data-ttu-id="72876-113">Адрес</span><span class="sxs-lookup"><span data-stu-id="72876-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72876-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="72876-114">Remarks</span></span>

<span data-ttu-id="72876-115">Эти свойства являются примерами свойств адресов для пользователя обмена сообщениями, которого представляет получаюющий пользователь.</span><span class="sxs-lookup"><span data-stu-id="72876-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="72876-116">Они должны быть установлены поставщиком входящих транспортных средств, который также отвечает за авторизацию или проверку делегата.</span><span class="sxs-lookup"><span data-stu-id="72876-116">They must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="72876-117">Если пользователь обмена сообщениями не представлен, эти свойства следует задать имени отображения, содержамуся в **свойстве PR_RECEIVED_BY_NAME** [(PidTagReceivedByName).](pidtagreceivedbyname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="72876-117">If no messaging user is being represented, these properties should be set to the display name contained in the **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="72876-118">Клиентская заявка, отвечая на сообщение, полученное от имени другого клиента, должно скопировать эти свойства из полученного сообщения в **свойство PR_SENT_REPRESENTING_NAME** [(PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)для ответа.</span><span class="sxs-lookup"><span data-stu-id="72876-118">A client application replying to a message received on behalf of another client should copy these properties from the received message into the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="72876-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="72876-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="72876-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="72876-120">Protocol specifications</span></span>

<span data-ttu-id="72876-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72876-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72876-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="72876-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="72876-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72876-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72876-124">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="72876-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="72876-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72876-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72876-126">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="72876-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="72876-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72876-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72876-128">Преобразования между объектами IETF RFC2445, RFC2446 и RFC2447, а также объектами назначения и собраний.</span><span class="sxs-lookup"><span data-stu-id="72876-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="72876-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72876-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72876-130">Указывает методы подключения к почтовым ящикам и настройки их в качестве делегатов, а также взаимодействия с объектами сообщений и календаря, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="72876-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="72876-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72876-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72876-132">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="72876-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="72876-133">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="72876-133">Header files</span></span>

<span data-ttu-id="72876-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72876-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="72876-135">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="72876-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="72876-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="72876-136">Mapitags.h</span></span>
  
> <span data-ttu-id="72876-137">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="72876-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72876-138">См. также</span><span class="sxs-lookup"><span data-stu-id="72876-138">See also</span></span>



[<span data-ttu-id="72876-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="72876-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72876-140">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="72876-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72876-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="72876-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72876-142">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="72876-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

