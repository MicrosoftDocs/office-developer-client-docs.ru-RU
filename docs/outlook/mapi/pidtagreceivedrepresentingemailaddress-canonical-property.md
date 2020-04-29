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
ms.openlocfilehash: 6916b1148caaf8283c6d7ae64ac2e05deb3ee0c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359103"
---
# <a name="pidtagreceivedrepresentingemailaddress-canonical-property"></a><span data-ttu-id="0fc47-103">Каноническое свойство PidTagReceivedRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="0fc47-103">PidTagReceivedRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="0fc47-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fc47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fc47-105">Содержит адрес электронной почты пользователя для обмена сообщениями, представленного пользователем-получателем.</span><span class="sxs-lookup"><span data-stu-id="0fc47-105">Contains the email address for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0fc47-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0fc47-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0fc47-107">PR_RCVD_REPRESENTING_EMAIL_ADDRESS, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_A PR_RCVD_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="0fc47-107">PR_RCVD_REPRESENTING_EMAIL_ADDRESS, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_A, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="0fc47-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0fc47-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0fc47-109">0x0078</span><span class="sxs-lookup"><span data-stu-id="0fc47-109">0x0078</span></span>  <br/> |
|<span data-ttu-id="0fc47-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0fc47-110">Data type:</span></span>  <br/> |<span data-ttu-id="0fc47-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="0fc47-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="0fc47-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0fc47-112">Area:</span></span>  <br/> |<span data-ttu-id="0fc47-113">Address</span><span class="sxs-lookup"><span data-stu-id="0fc47-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0fc47-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0fc47-114">Remarks</span></span>

<span data-ttu-id="0fc47-115">Эти свойства являются примерами свойств адресов для пользователя обмена сообщениями, представленного принимающим пользователем.</span><span class="sxs-lookup"><span data-stu-id="0fc47-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="0fc47-116">Они должны быть заданы входящим поставщиком транспорта, который также отвечает за авторизацию или проверку делегата.</span><span class="sxs-lookup"><span data-stu-id="0fc47-116">They must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="0fc47-117">Если пользователя обмена сообщениями нет, для этих свойств необходимо задать адрес электронной почты, который хранится в свойстве **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0fc47-117">If no messaging user is being represented, these properties should be set to the email address contained in the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="0fc47-118">Клиентское приложение, отвечающее на сообщение, полученное от имени другого клиента, должно копировать эти свойства из полученного сообщения в свойство **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) для ответа.</span><span class="sxs-lookup"><span data-stu-id="0fc47-118">A client application replying to a message received on behalf of another client should copy these properties from the received message into the **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0fc47-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0fc47-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0fc47-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0fc47-120">Protocol specifications</span></span>

<span data-ttu-id="0fc47-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fc47-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fc47-122">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0fc47-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0fc47-123">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fc47-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fc47-124">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0fc47-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="0fc47-125">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fc47-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fc47-126">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="0fc47-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="0fc47-127">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fc47-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fc47-128">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="0fc47-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="0fc47-129">[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fc47-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fc47-130">Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="0fc47-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="0fc47-131">[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fc47-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fc47-132">Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.</span><span class="sxs-lookup"><span data-stu-id="0fc47-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0fc47-133">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0fc47-133">Header files</span></span>

<span data-ttu-id="0fc47-134">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="0fc47-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="0fc47-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0fc47-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="0fc47-136">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="0fc47-136">Mapitags.h</span></span>
  
> <span data-ttu-id="0fc47-137">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="0fc47-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0fc47-138">См. также</span><span class="sxs-lookup"><span data-stu-id="0fc47-138">See also</span></span>



[<span data-ttu-id="0fc47-139">Каноническое свойство PidTagEmailAddress</span><span class="sxs-lookup"><span data-stu-id="0fc47-139">PidTagEmailAddress Canonical Property</span></span>](pidtagemailaddress-canonical-property.md)


[<span data-ttu-id="0fc47-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0fc47-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0fc47-141">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="0fc47-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0fc47-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0fc47-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0fc47-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0fc47-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

