---
title: Каноническое свойство PidTagSenderAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderAddressType
api_type:
- COM
ms.assetid: ad7f49ac-6fe8-4037-90f3-8dabd5648bed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1389c1189293955145f14e65f4c0f3e58bec909f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359145"
---
# <a name="pidtagsenderaddresstype-canonical-property"></a><span data-ttu-id="8efe7-103">Каноническое свойство PidTagSenderAddressType</span><span class="sxs-lookup"><span data-stu-id="8efe7-103">PidTagSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="8efe7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8efe7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8efe7-105">Содержит тип адреса электронной почты отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="8efe7-105">Contains the message sender's email address type.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8efe7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8efe7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8efe7-107">PR_SENDER_ADDRTYPE, PR_SENDER_ADDRTYPE_A, PR_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="8efe7-107">PR_SENDER_ADDRTYPE, PR_SENDER_ADDRTYPE_A, PR_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="8efe7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8efe7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8efe7-109">0x0C1E</span><span class="sxs-lookup"><span data-stu-id="8efe7-109">0x0C1E</span></span>  <br/> |
|<span data-ttu-id="8efe7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8efe7-110">Data type:</span></span>  <br/> |<span data-ttu-id="8efe7-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="8efe7-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="8efe7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8efe7-112">Area:</span></span>  <br/> |<span data-ttu-id="8efe7-113">Адрес</span><span class="sxs-lookup"><span data-stu-id="8efe7-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8efe7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8efe7-114">Remarks</span></span>

<span data-ttu-id="8efe7-115">Эти свойства являются примерами свойств адресов отправщика сообщений.</span><span class="sxs-lookup"><span data-stu-id="8efe7-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="8efe7-116">Он должен быть задат исходячим поставщиком транспорта, который никогда не должен распространять какие-либо ранее существующие значения.</span><span class="sxs-lookup"><span data-stu-id="8efe7-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="8efe7-117">Если ни один поставщик транспорта не предоставил никаких свойств адресов отправитель, пуллер MAPI пытается заполнить их путем вызова метода [IMAPISession::QueryIdentity](imapisession-queryidentity.md) для идентификатора входа.</span><span class="sxs-lookup"><span data-stu-id="8efe7-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="8efe7-118">Если идентификаторы записей не предоставлены, пульпер MAPI сохраняет "Unknown" во всех свойствах адресов отправителей типа PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="8efe7-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8efe7-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8efe7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8efe7-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8efe7-120">Protocol specifications</span></span>

<span data-ttu-id="8efe7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8efe7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8efe7-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="8efe7-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8efe7-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8efe7-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8efe7-124">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8efe7-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8efe7-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8efe7-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8efe7-126">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="8efe7-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8efe7-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8efe7-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8efe7-128">Преобразования между объектами IETF RFC2445, RFC2446 и RFC2447, а также объектами назначения и собраний.</span><span class="sxs-lookup"><span data-stu-id="8efe7-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8efe7-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8efe7-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8efe7-130">Указывает свойства и операции, допустимые для почтовых объектов.</span><span class="sxs-lookup"><span data-stu-id="8efe7-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="8efe7-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8efe7-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8efe7-132">Указывает свойства и операции, допустимые для объектов списка контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="8efe7-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="8efe7-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8efe7-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8efe7-134">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="8efe7-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8efe7-135">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="8efe7-135">Header files</span></span>

<span data-ttu-id="8efe7-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8efe7-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="8efe7-137">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8efe7-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="8efe7-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8efe7-138">Mapitags.h</span></span>
  
> <span data-ttu-id="8efe7-139">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="8efe7-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8efe7-140">См. также</span><span class="sxs-lookup"><span data-stu-id="8efe7-140">See also</span></span>



[<span data-ttu-id="8efe7-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8efe7-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8efe7-142">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8efe7-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8efe7-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8efe7-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8efe7-144">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="8efe7-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

