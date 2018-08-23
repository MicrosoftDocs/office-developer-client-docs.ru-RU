---
title: Каноническое свойство PidTagReceivedRepresentingAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingAddressType
api_type:
- COM
ms.assetid: c342bb2a-157e-4748-bf21-0926f95e5312
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c57324972f02366822a64e9e6c642d0f22ce158b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563382"
---
# <a name="pidtagreceivedrepresentingaddresstype-canonical-property"></a><span data-ttu-id="5ef91-103">Каноническое свойство PidTagReceivedRepresentingAddressType</span><span class="sxs-lookup"><span data-stu-id="5ef91-103">PidTagReceivedRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="5ef91-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ef91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ef91-105">Содержит тип адреса для обмена мгновенными сообщениями пользователя, представленного пользователя, фактически сообщения.</span><span class="sxs-lookup"><span data-stu-id="5ef91-105">Contains the address type for the messaging user who is represented by the user actually receiving the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ef91-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5ef91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ef91-107">PR_RCVD_REPRESENTING_ADDRTYPE, PR_RCVD_REPRESENTING_ADDRTYPE_A, PR_RCVD_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="5ef91-107">PR_RCVD_REPRESENTING_ADDRTYPE, PR_RCVD_REPRESENTING_ADDRTYPE_A, PR_RCVD_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="5ef91-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5ef91-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5ef91-109">0x0077</span><span class="sxs-lookup"><span data-stu-id="5ef91-109">0x0077</span></span>  <br/> |
|<span data-ttu-id="5ef91-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5ef91-110">Data type:</span></span>  <br/> |<span data-ttu-id="5ef91-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="5ef91-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="5ef91-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5ef91-112">Area:</span></span>  <br/> |<span data-ttu-id="5ef91-113">Address</span><span class="sxs-lookup"><span data-stu-id="5ef91-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ef91-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5ef91-114">Remarks</span></span>

<span data-ttu-id="5ef91-115">Эти свойства являются примерами свойства адреса для обмена мгновенными сообщениями пользователя, который представляется получателя.</span><span class="sxs-lookup"><span data-stu-id="5ef91-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="5ef91-116">Он должен иметь значение входящих поставщика транспорта, также несет ответственность за авторизации или проверки делегата.</span><span class="sxs-lookup"><span data-stu-id="5ef91-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="5ef91-117">Если пользователь не обмена сообщениями представлен, это свойство должно быть присвоено тип адреса, содержащихся в свойстве **PR_RECEIVED_BY_ADDRTYPE** ([PidTagReceivedByAddressType](pidtagreceivedbyaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5ef91-117">If no messaging user is being represented, this property should be set to the address type contained in the **PR_RECEIVED_BY_ADDRTYPE** ([PidTagReceivedByAddressType](pidtagreceivedbyaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="5ef91-118">Клиентского приложения ответ на сообщение получено от имени другого клиента должны скопируйте это свойство из полученного сообщения в свойство **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) для ответа.</span><span class="sxs-lookup"><span data-stu-id="5ef91-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5ef91-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5ef91-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5ef91-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5ef91-120">Protocol specifications</span></span>

<span data-ttu-id="5ef91-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ef91-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ef91-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5ef91-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5ef91-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ef91-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ef91-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5ef91-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="5ef91-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ef91-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ef91-126">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="5ef91-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="5ef91-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ef91-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ef91-128">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="5ef91-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="5ef91-129">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ef91-129">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ef91-130">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ef91-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="5ef91-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ef91-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ef91-132">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="5ef91-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5ef91-133">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5ef91-133">Header files</span></span>

<span data-ttu-id="5ef91-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ef91-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ef91-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5ef91-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="5ef91-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5ef91-136">Mapitags.h</span></span>
  
> <span data-ttu-id="5ef91-137">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="5ef91-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ef91-138">См. также</span><span class="sxs-lookup"><span data-stu-id="5ef91-138">See also</span></span>



[<span data-ttu-id="5ef91-139">Каноническое свойство PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="5ef91-139">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)


[<span data-ttu-id="5ef91-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5ef91-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ef91-141">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5ef91-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ef91-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5ef91-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ef91-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5ef91-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

