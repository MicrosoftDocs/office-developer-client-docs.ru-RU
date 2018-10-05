---
title: Каноническое свойство PidTagReceivedByEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEmailAddress
api_type:
- COM
ms.assetid: 5f9ebe20-b037-422b-9991-69f85122a706
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cea63037f926cdd178b6036c82e87cbba48d7347
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401526"
---
# <a name="pidtagreceivedbyemailaddress-canonical-property"></a><span data-ttu-id="a13a6-103">Каноническое свойство PidTagReceivedByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="a13a6-103">PidTagReceivedByEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="a13a6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a13a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a13a6-105">Содержит адрес электронной почты для обмена сообщениями пользователя, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="a13a6-105">Contains the email address for the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a13a6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a13a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a13a6-107">PR_RECEIVED_BY_EMAIL_ADDRESS, PR_RECEIVED_BY_EMAIL_ADDRESS_A, PR_RECEIVED_BY_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="a13a6-107">PR_RECEIVED_BY_EMAIL_ADDRESS, PR_RECEIVED_BY_EMAIL_ADDRESS_A, PR_RECEIVED_BY_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="a13a6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a13a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a13a6-109">0x0076</span><span class="sxs-lookup"><span data-stu-id="a13a6-109">0x0076</span></span>  <br/> |
|<span data-ttu-id="a13a6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a13a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="a13a6-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a13a6-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a13a6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a13a6-112">Area:</span></span>  <br/> |<span data-ttu-id="a13a6-113">Address</span><span class="sxs-lookup"><span data-stu-id="a13a6-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a13a6-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a13a6-114">Remarks</span></span>

<span data-ttu-id="a13a6-115">Эти свойства являются примерами свойства адреса для обмена мгновенными сообщениями пользователя, который получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="a13a6-115">These properties are examples of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="a13a6-116">Им должен иметь значение входящих поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="a13a6-116">They must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a13a6-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a13a6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a13a6-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a13a6-118">Protocol specifications</span></span>

<span data-ttu-id="a13a6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a13a6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a13a6-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a13a6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a13a6-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a13a6-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a13a6-122">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a13a6-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="a13a6-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a13a6-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a13a6-124">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="a13a6-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="a13a6-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a13a6-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a13a6-126">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="a13a6-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="a13a6-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a13a6-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a13a6-128">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="a13a6-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="a13a6-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a13a6-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a13a6-130">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a13a6-130">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="a13a6-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a13a6-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a13a6-132">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="a13a6-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a13a6-133">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a13a6-133">Header files</span></span>

<span data-ttu-id="a13a6-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a13a6-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="a13a6-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a13a6-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="a13a6-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a13a6-136">Mapitags.h</span></span>
  
> <span data-ttu-id="a13a6-137">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="a13a6-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a13a6-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a13a6-138">See also</span></span>



[<span data-ttu-id="a13a6-139">Каноническое свойство PidTagEmailAddress</span><span class="sxs-lookup"><span data-stu-id="a13a6-139">PidTagEmailAddress Canonical Property</span></span>](pidtagemailaddress-canonical-property.md)


[<span data-ttu-id="a13a6-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a13a6-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a13a6-141">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a13a6-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a13a6-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a13a6-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a13a6-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a13a6-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

