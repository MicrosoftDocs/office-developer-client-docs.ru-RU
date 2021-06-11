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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342856"
---
# <a name="pidtagsendersearchkey-canonical-property"></a><span data-ttu-id="6448c-103">Каноническое свойство PidTagSenderSearchKey</span><span class="sxs-lookup"><span data-stu-id="6448c-103">PidTagSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="6448c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6448c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6448c-105">Содержит ключ поиска отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="6448c-105">Contains the message sender's search key.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6448c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6448c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6448c-107">PR_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="6448c-107">PR_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="6448c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6448c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6448c-109">0x0C1D</span><span class="sxs-lookup"><span data-stu-id="6448c-109">0x0C1D</span></span>  <br/> |
|<span data-ttu-id="6448c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6448c-110">Data type:</span></span>  <br/> |<span data-ttu-id="6448c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6448c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6448c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6448c-112">Area:</span></span>  <br/> |<span data-ttu-id="6448c-113">Адрес</span><span class="sxs-lookup"><span data-stu-id="6448c-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6448c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6448c-114">Remarks</span></span>

<span data-ttu-id="6448c-115">Это свойство является одним из свойств адресов отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="6448c-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="6448c-116">Он должен быть задат исходячим поставщиком транспорта, который никогда не должен распространять какие-либо ранее существующие значения.</span><span class="sxs-lookup"><span data-stu-id="6448c-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="6448c-117">Если ни один поставщик транспорта не предоставил никаких свойств адресов отправитель, пуллер MAPI пытается заполнить их путем вызова метода [IMAPISession::QueryIdentity](imapisession-queryidentity.md) для идентификатора входа.</span><span class="sxs-lookup"><span data-stu-id="6448c-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="6448c-118">Если идентификаторы записей не предоставлены, в пульлере MAPI хранится ключ, соответствующий строке "Unknown" в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="6448c-118">If no entry identifiers have been provided, the MAPI spooler stores a key corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6448c-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6448c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6448c-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6448c-120">Protocol specifications</span></span>

<span data-ttu-id="6448c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6448c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6448c-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="6448c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6448c-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6448c-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6448c-124">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6448c-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="6448c-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6448c-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6448c-126">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6448c-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="6448c-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6448c-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6448c-128">Преобразования между объектами IETF RFC2445, RFC2446 и RFC2447, а также объектами назначения и собраний.</span><span class="sxs-lookup"><span data-stu-id="6448c-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="6448c-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6448c-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6448c-130">Указывает свойства и операции, допустимые для почтовых объектов.</span><span class="sxs-lookup"><span data-stu-id="6448c-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="6448c-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6448c-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6448c-132">Указывает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="6448c-132">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="6448c-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6448c-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6448c-134">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="6448c-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6448c-135">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="6448c-135">Header files</span></span>

<span data-ttu-id="6448c-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6448c-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="6448c-137">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6448c-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="6448c-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6448c-138">Mapitags.h</span></span>
  
> <span data-ttu-id="6448c-139">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="6448c-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6448c-140">См. также</span><span class="sxs-lookup"><span data-stu-id="6448c-140">See also</span></span>



[<span data-ttu-id="6448c-141">Каноническое свойство PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="6448c-141">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)
  
[<span data-ttu-id="6448c-142">Каноническое свойство PidTagSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="6448c-142">PidTagSentRepresentingSearchKey Canonical Property</span></span>](pidtagsentrepresentingsearchkey-canonical-property.md)


[<span data-ttu-id="6448c-143">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6448c-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6448c-144">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6448c-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6448c-145">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6448c-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6448c-146">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="6448c-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

