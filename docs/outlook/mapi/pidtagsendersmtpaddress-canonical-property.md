---
title: Каноническое свойство PidTagSenderSmtpAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 321cde5a-05db-498b-a9b8-cb54c8a14e34
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c39fce40fb508370e62cb8b38123fa6ccc0e7d7b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387029"
---
# <a name="pidtagsendersmtpaddress-canonical-property"></a><span data-ttu-id="a7ab2-103">Каноническое свойство PidTagSenderSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="a7ab2-103">PidTagSenderSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="a7ab2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7ab2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7ab2-105">Содержит формат транспортный протокол SMTP (Simple Mail) адрес электронной почты отправителя владельца почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="a7ab2-105">Contains the format of the Simple Mail Transport Protocol (SMTP) email address of the sending mailbox owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7ab2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a7ab2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7ab2-107">PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="a7ab2-107">PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="a7ab2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a7ab2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7ab2-109">0x5D01</span><span class="sxs-lookup"><span data-stu-id="a7ab2-109">0x5D01</span></span>  <br/> |
|<span data-ttu-id="a7ab2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a7ab2-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7ab2-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a7ab2-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a7ab2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a7ab2-112">Area:</span></span>  <br/> |<span data-ttu-id="a7ab2-113">Address</span><span class="sxs-lookup"><span data-stu-id="a7ab2-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7ab2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a7ab2-114">Remarks</span></span>

<span data-ttu-id="a7ab2-115">Это свойство является примером свойства адреса отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="a7ab2-115">This property is an example of the address properties for the message sender.</span></span> <span data-ttu-id="a7ab2-116">Он должен иметь значение исходящей поставщика транспорта, никогда не следует передать все ранее существующие значения.</span><span class="sxs-lookup"><span data-stu-id="a7ab2-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="a7ab2-117">Если отсутствует транспорт не предоставил любые свойства адрес отправителя, диспетчер очереди MAPI пытается заполните их путем вызова метода [IMAPISession::QueryIdentity](imapisession-queryidentity.md) на идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="a7ab2-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="a7ab2-118">Если этот параметр указан без идентификаторы записей диспетчер очереди MAPI сохраняет «Неизвестно» в все свойства адреса отправителя типа PT_UNICODE или PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="a7ab2-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_UNICODE or PT_STRING8.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a7ab2-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a7ab2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7ab2-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a7ab2-120">Protocol specifications</span></span>

<span data-ttu-id="a7ab2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7ab2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7ab2-122">Содержит ссылки на связанные спецификаций протокола Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a7ab2-122">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a7ab2-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7ab2-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7ab2-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a7ab2-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="a7ab2-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7ab2-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7ab2-126">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="a7ab2-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="a7ab2-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7ab2-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7ab2-128">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="a7ab2-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="a7ab2-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7ab2-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7ab2-130">Указывает, что свойства и операции, допустимые для учета объекты.</span><span class="sxs-lookup"><span data-stu-id="a7ab2-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="a7ab2-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7ab2-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7ab2-132">Задает свойства и операции, допустимые для объектов списка рассылки и контактов.</span><span class="sxs-lookup"><span data-stu-id="a7ab2-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="a7ab2-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7ab2-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7ab2-134">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="a7ab2-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7ab2-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a7ab2-135">Header files</span></span>

<span data-ttu-id="a7ab2-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7ab2-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7ab2-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a7ab2-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7ab2-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a7ab2-138">Mapitags.h</span></span>
  
> <span data-ttu-id="a7ab2-139">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="a7ab2-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7ab2-140">См. также</span><span class="sxs-lookup"><span data-stu-id="a7ab2-140">See also</span></span>



[<span data-ttu-id="a7ab2-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a7ab2-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7ab2-142">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a7ab2-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7ab2-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a7ab2-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7ab2-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a7ab2-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

