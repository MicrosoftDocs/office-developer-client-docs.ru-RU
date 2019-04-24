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
ms.openlocfilehash: 9592057757b7bad0c2400f8b1c720ef0146bb9a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359201"
---
# <a name="pidtagreceivedrepresentingaddresstype-canonical-property"></a><span data-ttu-id="a6002-103">Каноническое свойство PidTagReceivedRepresentingAddressType</span><span class="sxs-lookup"><span data-stu-id="a6002-103">PidTagReceivedRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="a6002-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6002-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6002-105">Содержит тип адреса пользователя обмена сообщениями, представленного пользователем, который действительно получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="a6002-105">Contains the address type for the messaging user who is represented by the user actually receiving the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a6002-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a6002-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a6002-107">ПР_РКВД_РЕПРЕСЕНТИНГ_АДДРТИПЕ, ПР_РКВД_РЕПРЕСЕНТИНГ_АДДРТИПЕ_А, ПР_РКВД_РЕПРЕСЕНТИНГ_АДДРТИПЕ_В</span><span class="sxs-lookup"><span data-stu-id="a6002-107">PR_RCVD_REPRESENTING_ADDRTYPE, PR_RCVD_REPRESENTING_ADDRTYPE_A, PR_RCVD_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="a6002-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a6002-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a6002-109">0x0077</span><span class="sxs-lookup"><span data-stu-id="a6002-109">0x0077</span></span>  <br/> |
|<span data-ttu-id="a6002-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a6002-110">Data type:</span></span>  <br/> |<span data-ttu-id="a6002-111">ПТ_УНИКОДЕ, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a6002-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a6002-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a6002-112">Area:</span></span>  <br/> |<span data-ttu-id="a6002-113">Address</span><span class="sxs-lookup"><span data-stu-id="a6002-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6002-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a6002-114">Remarks</span></span>

<span data-ttu-id="a6002-115">Эти свойства являются примерами свойств адресов для пользователя обмена сообщениями, представленного принимающим пользователем.</span><span class="sxs-lookup"><span data-stu-id="a6002-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="a6002-116">Он должен быть задан входящим поставщиком транспорта, который также отвечает за авторизацию или проверку делегата.</span><span class="sxs-lookup"><span data-stu-id="a6002-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="a6002-117">Если не представлен пользователь обмена сообщениями, для этого свойства необходимо задать тип адреса, содержащийся в свойстве **пр_рецеивед_би_аддртипе** ([PidTagReceivedByAddressType](pidtagreceivedbyaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a6002-117">If no messaging user is being represented, this property should be set to the address type contained in the **PR_RECEIVED_BY_ADDRTYPE** ([PidTagReceivedByAddressType](pidtagreceivedbyaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="a6002-118">Клиентское приложение, отвечающее на сообщение, полученное от имени другого клиента, должно копировать это свойство из полученного сообщения в свойство **пр_сент_репресентинг_аддртипе** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) для ответа.</span><span class="sxs-lookup"><span data-stu-id="a6002-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a6002-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a6002-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a6002-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a6002-120">Protocol specifications</span></span>

<span data-ttu-id="a6002-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6002-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6002-122">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a6002-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a6002-123">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6002-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6002-124">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a6002-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="a6002-125">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6002-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6002-126">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="a6002-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="a6002-127">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6002-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6002-128">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="a6002-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="a6002-129">[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6002-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6002-130">Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="a6002-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="a6002-131">[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6002-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6002-132">Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.</span><span class="sxs-lookup"><span data-stu-id="a6002-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a6002-133">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="a6002-133">Header files</span></span>

<span data-ttu-id="a6002-134">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="a6002-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="a6002-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a6002-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="a6002-136">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="a6002-136">Mapitags.h</span></span>
  
> <span data-ttu-id="a6002-137">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="a6002-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6002-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a6002-138">See also</span></span>



[<span data-ttu-id="a6002-139">Каноническое свойство PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="a6002-139">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)


[<span data-ttu-id="a6002-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a6002-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a6002-141">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="a6002-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a6002-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a6002-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a6002-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a6002-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

