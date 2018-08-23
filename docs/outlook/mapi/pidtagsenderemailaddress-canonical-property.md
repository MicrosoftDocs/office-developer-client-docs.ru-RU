---
title: Каноническое свойство PidTagSenderEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEmailAddress
api_type:
- COM
ms.assetid: 6e1531ac-489b-4224-921a-8fd13ace9497
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8efceed4910d057d6dcca742dfe9b8f0010c968e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578677"
---
# <a name="pidtagsenderemailaddress-canonical-property"></a><span data-ttu-id="884fd-103">Каноническое свойство PidTagSenderEmailAddress</span><span class="sxs-lookup"><span data-stu-id="884fd-103">PidTagSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="884fd-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="884fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="884fd-105">Содержит адрес электронной почты отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="884fd-105">Contains the message sender's email address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="884fd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="884fd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="884fd-107">PR_SENDER_EMAIL_ADDRESS, PR_SENDER_EMAIL_ADDRESS_A, PR_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="884fd-107">PR_SENDER_EMAIL_ADDRESS, PR_SENDER_EMAIL_ADDRESS_A, PR_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="884fd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="884fd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="884fd-109">0x0C1F</span><span class="sxs-lookup"><span data-stu-id="884fd-109">0x0C1F</span></span>  <br/> |
|<span data-ttu-id="884fd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="884fd-110">Data type:</span></span>  <br/> |<span data-ttu-id="884fd-111">PT_UNICOIDE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="884fd-111">PT_UNICOIDE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="884fd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="884fd-112">Area:</span></span>  <br/> |<span data-ttu-id="884fd-113">Address</span><span class="sxs-lookup"><span data-stu-id="884fd-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="884fd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="884fd-114">Remarks</span></span>

<span data-ttu-id="884fd-115">Эти свойства являются примерами свойства адреса отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="884fd-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="884fd-116">Им должен иметь значение исходящей поставщика транспорта, никогда не следует передать все ранее существующие значения.</span><span class="sxs-lookup"><span data-stu-id="884fd-116">They must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="884fd-117">Если отсутствует транспорт не предоставил любые свойства адрес отправителя, диспетчер очереди MAPI пытается заполните их путем вызова метода [IMAPISession::QueryIdentity](imapisession-queryidentity.md) на идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="884fd-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="884fd-118">Если этот параметр указан без идентификаторы записей диспетчер очереди MAPI сохраняет «Неизвестно» в все свойства адреса отправителя типа PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="884fd-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="884fd-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="884fd-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="884fd-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="884fd-120">Protocol specifications</span></span>

<span data-ttu-id="884fd-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="884fd-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="884fd-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="884fd-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="884fd-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="884fd-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="884fd-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="884fd-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="884fd-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="884fd-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="884fd-126">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="884fd-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="884fd-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="884fd-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="884fd-128">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="884fd-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="884fd-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="884fd-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="884fd-130">Указывает, что свойства и операции, допустимые для учета объекты.</span><span class="sxs-lookup"><span data-stu-id="884fd-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="884fd-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="884fd-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="884fd-132">Задает свойства и операции, допустимые для объектов списка рассылки и контактов.</span><span class="sxs-lookup"><span data-stu-id="884fd-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="884fd-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="884fd-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="884fd-134">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="884fd-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="884fd-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="884fd-135">Header files</span></span>

<span data-ttu-id="884fd-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="884fd-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="884fd-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="884fd-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="884fd-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="884fd-138">Mapitags.h</span></span>
  
> <span data-ttu-id="884fd-139">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="884fd-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="884fd-140">См. также</span><span class="sxs-lookup"><span data-stu-id="884fd-140">See also</span></span>



[<span data-ttu-id="884fd-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="884fd-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="884fd-142">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="884fd-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="884fd-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="884fd-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="884fd-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="884fd-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

