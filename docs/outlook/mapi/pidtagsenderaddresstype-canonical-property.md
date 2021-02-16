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
# <a name="pidtagsenderaddresstype-canonical-property"></a><span data-ttu-id="92812-103">Каноническое свойство PidTagSenderAddressType</span><span class="sxs-lookup"><span data-stu-id="92812-103">PidTagSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="92812-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92812-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92812-105">Содержит тип адреса электронной почты отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="92812-105">Contains the message sender's email address type.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92812-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="92812-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92812-107">PR_SENDER_ADDRTYPE, PR_SENDER_ADDRTYPE_A, PR_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="92812-107">PR_SENDER_ADDRTYPE, PR_SENDER_ADDRTYPE_A, PR_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="92812-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="92812-108">Identifier:</span></span>  <br/> |<span data-ttu-id="92812-109">0x0C1E</span><span class="sxs-lookup"><span data-stu-id="92812-109">0x0C1E</span></span>  <br/> |
|<span data-ttu-id="92812-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="92812-110">Data type:</span></span>  <br/> |<span data-ttu-id="92812-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="92812-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="92812-112">Область:</span><span class="sxs-lookup"><span data-stu-id="92812-112">Area:</span></span>  <br/> |<span data-ttu-id="92812-113">Address</span><span class="sxs-lookup"><span data-stu-id="92812-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92812-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="92812-114">Remarks</span></span>

<span data-ttu-id="92812-115">Эти свойства являются примерами свойств адреса для отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="92812-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="92812-116">Он должен быть установлен поставщиком исходячих транспортных данных, который никогда не должен распространять ранее существовавших значений.</span><span class="sxs-lookup"><span data-stu-id="92812-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="92812-117">Если ни один поставщик транспорта не предоставил никаких свойств адресов отправитель, то пулер MAPI пытается заполнить их, вызывая метод [IMAPISession::QueryIdentity](imapisession-queryidentity.md) для идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="92812-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="92812-118">Если идентификаторы записей не указаны, то пульщик MAPI сохраняет "Unknown" во всех свойствах адреса отправитель типа PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="92812-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="92812-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="92812-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="92812-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="92812-120">Protocol specifications</span></span>

<span data-ttu-id="92812-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92812-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92812-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="92812-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="92812-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92812-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92812-124">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="92812-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="92812-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92812-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92812-126">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="92812-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="92812-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92812-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92812-128">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="92812-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="92812-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92812-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92812-130">Указывает свойства и операции, которые разрешены для объектов post.</span><span class="sxs-lookup"><span data-stu-id="92812-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="92812-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92812-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92812-132">Указывает свойства и операции, которые разрешены для объектов контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="92812-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="92812-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92812-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92812-134">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="92812-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="92812-135">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="92812-135">Header files</span></span>

<span data-ttu-id="92812-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92812-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="92812-137">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="92812-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="92812-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="92812-138">Mapitags.h</span></span>
  
> <span data-ttu-id="92812-139">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="92812-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92812-140">См. также</span><span class="sxs-lookup"><span data-stu-id="92812-140">See also</span></span>



[<span data-ttu-id="92812-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="92812-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92812-142">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="92812-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92812-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="92812-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92812-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="92812-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

