---
title: Каноническое свойство PidTagTnefCorrelationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5a0216616d9a35ef5ad4509bc377044c1d217d79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812010"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a><span data-ttu-id="ecf1f-103">Каноническое свойство PidTagTnefCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="ecf1f-103">PidTagTnefCorrelationKey Canonical Property</span></span>

  
  
<span data-ttu-id="ecf1f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecf1f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecf1f-105">Содержит значение, соответствующее подключение к транспорта Neutral Encapsulation формата TNEF с сообщением.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-105">Contains a value that correlates a Transport Neutral Encapsulation Format (TNEF) attachment with a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ecf1f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ecf1f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ecf1f-107">PR_TNEF_CORRELATION_KEY</span><span class="sxs-lookup"><span data-stu-id="ecf1f-107">PR_TNEF_CORRELATION_KEY</span></span>  <br/> |
|<span data-ttu-id="ecf1f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ecf1f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ecf1f-109">0x007F</span><span class="sxs-lookup"><span data-stu-id="ecf1f-109">0x007F</span></span>  <br/> |
|<span data-ttu-id="ecf1f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ecf1f-110">Data type:</span></span>  <br/> |<span data-ttu-id="ecf1f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ecf1f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ecf1f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ecf1f-112">Area:</span></span>  <br/> |<span data-ttu-id="ecf1f-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="ecf1f-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecf1f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ecf1f-114">Remarks</span></span>

<span data-ttu-id="ecf1f-115">Рекомендуется указывать, что дочерним объектам вложения TNEF данное свойство.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-115">It is recommended that TNEF attachment sub-objects expose this property.</span></span> <span data-ttu-id="ecf1f-116">Это свойство определяет, принадлежит ли файл входящих TNEF сообщение, которое он подключен к.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-116">This property determines whether or not an inbound TNEF file belongs to the message it is attached to.</span></span> <span data-ttu-id="ecf1f-117">Он используется в основном с поставщиками транспорта и шлюзов.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-117">It is used primarily by transport providers and gateways.</span></span>
  
<span data-ttu-id="ecf1f-118">На исходящее сообщение поставщика транспорта должен compute двоичное значение, уникальным для этого сообщения или использовать существующее значение, которая должна удовлетворять требования уникальности, такие как идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-118">On an outbound message, the transport provider should compute a binary value unique to that message, or use an existing value that satisfies the uniqueness requirement, such as a message identifier.</span></span> <span data-ttu-id="ecf1f-119">Поставщика транспорта следует хранить это значение в это свойство и затем вызвать метод [ITnef::AddProps](itnef-addprops.md) для его инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-119">The transport provider should store this value in this property and then call the [ITnef::AddProps](itnef-addprops.md) method to encapsulate it.</span></span> <span data-ttu-id="ecf1f-120">Такое же значение также должны храниться в конверте транспорта на месте, определенные поставщиком, такие как заголовок сообщения.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-120">The same value should also be stored in the transport envelope in a place defined by the provider, such as the message header.</span></span> 
  
<span data-ttu-id="ecf1f-121">На входящих сообщений поставщика транспорта необходимо вызвать метод [ITnef::ExtractProps](itnef-extractprops.md) для decapsulate вложения TNEF и сравните это свойство со значением, хранящиеся в конверте транспорта.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-121">On an inbound message, the transport provider should call the [ITnef::ExtractProps](itnef-extractprops.md) method to decapsulate the TNEF attachment and then compare this property with the value stored in the transport envelope.</span></span> <span data-ttu-id="ecf1f-122">Если значения совпадают, TNEF обрабатывается обычным способом, то есть, следует использовать все свойства, извлеченные из вложения TNEF.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-122">If the values match, TNEF should be processed normally, that is, all the properties extracted from the TNEF attachment should be used.</span></span> <span data-ttu-id="ecf1f-123">Если значения не совпадают, все свойства из вложения TNEF можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-123">If the values do not match, all the properties from the TNEF attachment should be ignored.</span></span> <span data-ttu-id="ecf1f-124">Если это свойство не задано, в файл формата TNEF должны считаться принадлежать на это сообщение и другие свойства, извлеченные из его следует использовать.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-124">If this property is not set, the TNEF file should be considered to belong to this message, and the other properties extracted from it should be used.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ecf1f-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ecf1f-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ecf1f-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ecf1f-126">Protocol specifications</span></span>

<span data-ttu-id="ecf1f-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecf1f-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecf1f-128">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ecf1f-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecf1f-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecf1f-130">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ecf1f-131">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecf1f-131">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecf1f-132">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-132">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="ecf1f-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecf1f-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecf1f-134">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ecf1f-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ecf1f-135">Header files</span></span>

<span data-ttu-id="ecf1f-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecf1f-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="ecf1f-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="ecf1f-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ecf1f-138">Mapitags.h</span></span>
  
> <span data-ttu-id="ecf1f-139">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ecf1f-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecf1f-140">См. также</span><span class="sxs-lookup"><span data-stu-id="ecf1f-140">See also</span></span>



[<span data-ttu-id="ecf1f-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ecf1f-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ecf1f-142">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ecf1f-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ecf1f-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ecf1f-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ecf1f-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ecf1f-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

