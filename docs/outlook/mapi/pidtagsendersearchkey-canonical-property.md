---
title: Каноническое свойство PidTagSenderSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderSearchKey
api_type:
- COM
ms.assetid: e15599c5-f40f-46a6-a726-7359efd09ff8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c36d9744bcf5b1126a0fcc90ae6330f2dc8ef0ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386091"
---
# <a name="pidtagsendersearchkey-canonical-property"></a><span data-ttu-id="70547-103">Каноническое свойство PidTagSenderSearchKey</span><span class="sxs-lookup"><span data-stu-id="70547-103">PidTagSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="70547-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70547-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70547-105">Содержит ключ поиска отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="70547-105">Contains the message sender's search key.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70547-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="70547-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70547-107">PR_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="70547-107">PR_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="70547-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="70547-108">Identifier:</span></span>  <br/> |<span data-ttu-id="70547-109">0x0C1D</span><span class="sxs-lookup"><span data-stu-id="70547-109">0x0C1D</span></span>  <br/> |
|<span data-ttu-id="70547-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="70547-110">Data type:</span></span>  <br/> |<span data-ttu-id="70547-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="70547-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="70547-112">Область:</span><span class="sxs-lookup"><span data-stu-id="70547-112">Area:</span></span>  <br/> |<span data-ttu-id="70547-113">Address</span><span class="sxs-lookup"><span data-stu-id="70547-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70547-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="70547-114">Remarks</span></span>

<span data-ttu-id="70547-115">Это свойство является одним из свойств адреса отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="70547-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="70547-116">Он должен иметь значение исходящей поставщика транспорта, никогда не следует передать все ранее существующие значения.</span><span class="sxs-lookup"><span data-stu-id="70547-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="70547-117">Если отсутствует транспорт не предоставил любые свойства адрес отправителя, диспетчер очереди MAPI пытается заполните их путем вызова метода [IMAPISession::QueryIdentity](imapisession-queryidentity.md) на идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="70547-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="70547-118">Если этот параметр указан без идентификаторы записей диспетчер очереди MAPI сохранение ключа, соответствующего строка «Неизвестно» в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="70547-118">If no entry identifiers have been provided, the MAPI spooler stores a key corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="70547-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="70547-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="70547-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="70547-120">Protocol specifications</span></span>

<span data-ttu-id="70547-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70547-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70547-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="70547-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="70547-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70547-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70547-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="70547-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="70547-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70547-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70547-126">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="70547-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="70547-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70547-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70547-128">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="70547-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="70547-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70547-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70547-130">Указывает, что свойства и операции, допустимые для учета объекты.</span><span class="sxs-lookup"><span data-stu-id="70547-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="70547-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70547-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70547-132">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="70547-132">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="70547-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70547-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70547-134">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="70547-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="70547-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="70547-135">Header files</span></span>

<span data-ttu-id="70547-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70547-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="70547-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="70547-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="70547-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="70547-138">Mapitags.h</span></span>
  
> <span data-ttu-id="70547-139">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="70547-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70547-140">См. также</span><span class="sxs-lookup"><span data-stu-id="70547-140">See also</span></span>



[<span data-ttu-id="70547-141">Каноническое свойство PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="70547-141">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)
  
[<span data-ttu-id="70547-142">Каноническое свойство PidTagSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="70547-142">PidTagSentRepresentingSearchKey Canonical Property</span></span>](pidtagsentrepresentingsearchkey-canonical-property.md)


[<span data-ttu-id="70547-143">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="70547-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70547-144">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="70547-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70547-145">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="70547-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70547-146">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="70547-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

