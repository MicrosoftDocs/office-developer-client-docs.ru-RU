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
ms.openlocfilehash: 854b9c69a4a3ca74ee18a30e54ebded4976c18e2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563753"
---
# <a name="pidtagreceivedrepresentingname-canonical-property"></a><span data-ttu-id="e2125-103">Каноническое свойство PidTagReceivedRepresentingName</span><span class="sxs-lookup"><span data-stu-id="e2125-103">PidTagReceivedRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="e2125-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2125-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2125-105">Содержит отображаемое имя для обмена сообщениями пользователя, представленного получателя.</span><span class="sxs-lookup"><span data-stu-id="e2125-105">Contains the display name for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2125-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e2125-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2125-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e2125-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e2125-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e2125-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2125-109">0x0044</span><span class="sxs-lookup"><span data-stu-id="e2125-109">0x0044</span></span>  <br/> |
|<span data-ttu-id="e2125-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e2125-110">Data type:</span></span>  <br/> |<span data-ttu-id="e2125-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="e2125-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="e2125-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e2125-112">Area:</span></span>  <br/> |<span data-ttu-id="e2125-113">Address</span><span class="sxs-lookup"><span data-stu-id="e2125-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2125-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e2125-114">Remarks</span></span>

<span data-ttu-id="e2125-115">Эти свойства являются примерами свойства адреса для обмена мгновенными сообщениями пользователя, который представляется получателя.</span><span class="sxs-lookup"><span data-stu-id="e2125-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="e2125-116">Им должен иметь значение входящих поставщика транспорта, также несет ответственность за авторизации или проверки делегата.</span><span class="sxs-lookup"><span data-stu-id="e2125-116">They must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="e2125-117">Если пользователь не обмена сообщениями представлен, эти свойства должны быть установлены для отображаемое имя, содержащихся в свойстве **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e2125-117">If no messaging user is being represented, these properties should be set to the display name contained in the **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="e2125-118">Клиентского приложения ответ на сообщение получено от имени другого клиента должен скопировать эти свойства из полученного сообщения в свойство **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) для ответа на.</span><span class="sxs-lookup"><span data-stu-id="e2125-118">A client application replying to a message received on behalf of another client should copy these properties from the received message into the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e2125-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e2125-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2125-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e2125-120">Protocol specifications</span></span>

<span data-ttu-id="e2125-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2125-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2125-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e2125-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2125-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2125-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2125-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e2125-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="e2125-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2125-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2125-126">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="e2125-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e2125-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2125-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2125-128">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="e2125-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e2125-129">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2125-129">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2125-130">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="e2125-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="e2125-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2125-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2125-132">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="e2125-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2125-133">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e2125-133">Header files</span></span>

<span data-ttu-id="e2125-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2125-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2125-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e2125-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="e2125-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e2125-136">Mapitags.h</span></span>
  
> <span data-ttu-id="e2125-137">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="e2125-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2125-138">См. также</span><span class="sxs-lookup"><span data-stu-id="e2125-138">See also</span></span>



[<span data-ttu-id="e2125-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e2125-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2125-140">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e2125-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2125-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e2125-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2125-142">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e2125-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

