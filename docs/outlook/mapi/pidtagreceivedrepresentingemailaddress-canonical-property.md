---
title: Каноническое свойство PidTagReceivedRepresentingEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingEmailAddress
api_type:
- COM
ms.assetid: f85ce31c-f621-47ed-badf-4f59a45ec0a1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 47c2fdf3a48a7c672e7bf1b69d8315675a537e42
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811644"
---
# <a name="pidtagreceivedrepresentingemailaddress-canonical-property"></a><span data-ttu-id="44110-103">Каноническое свойство PidTagReceivedRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="44110-103">PidTagReceivedRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="44110-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44110-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44110-105">Содержит адрес электронной почты для обмена сообщениями пользователя, представленного получателя.</span><span class="sxs-lookup"><span data-stu-id="44110-105">Contains the email address for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44110-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="44110-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44110-107">PR_RCVD_REPRESENTING_EMAIL_ADDRESS, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_A, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="44110-107">PR_RCVD_REPRESENTING_EMAIL_ADDRESS, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_A, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="44110-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="44110-108">Identifier:</span></span>  <br/> |<span data-ttu-id="44110-109">0x0078</span><span class="sxs-lookup"><span data-stu-id="44110-109">0x0078</span></span>  <br/> |
|<span data-ttu-id="44110-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="44110-110">Data type:</span></span>  <br/> |<span data-ttu-id="44110-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="44110-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="44110-112">Область:</span><span class="sxs-lookup"><span data-stu-id="44110-112">Area:</span></span>  <br/> |<span data-ttu-id="44110-113">Address</span><span class="sxs-lookup"><span data-stu-id="44110-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44110-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="44110-114">Remarks</span></span>

<span data-ttu-id="44110-115">Эти свойства являются примерами свойства адреса для обмена мгновенными сообщениями пользователя, который представляется получателя.</span><span class="sxs-lookup"><span data-stu-id="44110-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="44110-116">Им должен иметь значение входящих поставщика транспорта, также несет ответственность за авторизации или проверки делегата.</span><span class="sxs-lookup"><span data-stu-id="44110-116">They must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="44110-117">Если пользователь не обмена сообщениями представлен, эти свойства должны быть установлены на адрес электронной почты, содержащихся в свойстве **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="44110-117">If no messaging user is being represented, these properties should be set to the email address contained in the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="44110-118">Клиентского приложения ответ на сообщение получено от имени другого клиента должен скопировать эти свойства из полученного сообщения в свойство **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) ответ.</span><span class="sxs-lookup"><span data-stu-id="44110-118">A client application replying to a message received on behalf of another client should copy these properties from the received message into the **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="44110-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="44110-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="44110-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="44110-120">Protocol specifications</span></span>

<span data-ttu-id="44110-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44110-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44110-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="44110-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="44110-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44110-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44110-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="44110-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="44110-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44110-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44110-126">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="44110-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="44110-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44110-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44110-128">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="44110-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="44110-129">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44110-129">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44110-130">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="44110-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="44110-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44110-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44110-132">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="44110-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="44110-133">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="44110-133">Header files</span></span>

<span data-ttu-id="44110-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44110-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="44110-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="44110-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="44110-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="44110-136">Mapitags.h</span></span>
  
> <span data-ttu-id="44110-137">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="44110-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44110-138">См. также</span><span class="sxs-lookup"><span data-stu-id="44110-138">See also</span></span>



[<span data-ttu-id="44110-139">Каноническое свойство PidTagEmailAddress</span><span class="sxs-lookup"><span data-stu-id="44110-139">PidTagEmailAddress Canonical Property</span></span>](pidtagemailaddress-canonical-property.md)


[<span data-ttu-id="44110-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="44110-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44110-141">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="44110-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44110-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="44110-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44110-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="44110-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

