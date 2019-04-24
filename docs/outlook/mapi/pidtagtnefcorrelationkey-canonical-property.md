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
ms.openlocfilehash: e38cf93523c14d2d58c48e24a79249674298b4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341953"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a><span data-ttu-id="ad258-103">Каноническое свойство PidTagTnefCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="ad258-103">PidTagTnefCorrelationKey Canonical Property</span></span>

  
  
<span data-ttu-id="ad258-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad258-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad258-105">Содержит значение, которое сопоставляет вложение формата TNEF с сообщением.</span><span class="sxs-lookup"><span data-stu-id="ad258-105">Contains a value that correlates a Transport Neutral Encapsulation Format (TNEF) attachment with a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad258-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ad258-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad258-107">ПР_ТНЕФ_КОРРЕЛАТИОН_КЭЙ</span><span class="sxs-lookup"><span data-stu-id="ad258-107">PR_TNEF_CORRELATION_KEY</span></span>  <br/> |
|<span data-ttu-id="ad258-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ad258-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad258-109">0x007F</span><span class="sxs-lookup"><span data-stu-id="ad258-109">0x007F</span></span>  <br/> |
|<span data-ttu-id="ad258-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ad258-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad258-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ad258-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ad258-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ad258-112">Area:</span></span>  <br/> |<span data-ttu-id="ad258-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="ad258-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad258-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad258-114">Remarks</span></span>

<span data-ttu-id="ad258-115">Рекомендуется, чтобы вложенные объекты вложения TNEF предоставляли это свойство.</span><span class="sxs-lookup"><span data-stu-id="ad258-115">It is recommended that TNEF attachment sub-objects expose this property.</span></span> <span data-ttu-id="ad258-116">Это свойство определяет, принадлежит ли входящий файл TNEF к сообщению, к которому оно присоединено.</span><span class="sxs-lookup"><span data-stu-id="ad258-116">This property determines whether or not an inbound TNEF file belongs to the message it is attached to.</span></span> <span data-ttu-id="ad258-117">В основном он используется поставщиками транспорта и шлюзами.</span><span class="sxs-lookup"><span data-stu-id="ad258-117">It is used primarily by transport providers and gateways.</span></span>
  
<span data-ttu-id="ad258-118">Для исходящих сообщений поставщик транспорта должен вычислить двоичное значение, которое соответствует этому сообщению, или использовать существующее значение, которое соответствует требованию уникальности, например идентификатору сообщения.</span><span class="sxs-lookup"><span data-stu-id="ad258-118">On an outbound message, the transport provider should compute a binary value unique to that message, or use an existing value that satisfies the uniqueness requirement, such as a message identifier.</span></span> <span data-ttu-id="ad258-119">Поставщик транспорта должен хранить это значение в этом свойстве, а затем вызвать метод [итнеф:: аддпропс](itnef-addprops.md) для его инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="ad258-119">The transport provider should store this value in this property and then call the [ITnef::AddProps](itnef-addprops.md) method to encapsulate it.</span></span> <span data-ttu-id="ad258-120">Одно и то же значение должно также храниться на транспортном конверте в месте, определенном поставщиком, например, в заголовке сообщения.</span><span class="sxs-lookup"><span data-stu-id="ad258-120">The same value should also be stored in the transport envelope in a place defined by the provider, such as the message header.</span></span> 
  
<span data-ttu-id="ad258-121">Для входящего сообщения поставщик транспорта должен вызвать метод [итнеф:: екстрактпропс](itnef-extractprops.md) , чтобы декапсулате вложение в формат TNEF, а затем сравнить это свойство со значением, хранящимся в конверте транспорта.</span><span class="sxs-lookup"><span data-stu-id="ad258-121">On an inbound message, the transport provider should call the [ITnef::ExtractProps](itnef-extractprops.md) method to decapsulate the TNEF attachment and then compare this property with the value stored in the transport envelope.</span></span> <span data-ttu-id="ad258-122">Если значения совпадают, формат TNEF должен обрабатываться обычным образом, то есть все свойства, извлеченные из вложения TNEF, следует использовать.</span><span class="sxs-lookup"><span data-stu-id="ad258-122">If the values match, TNEF should be processed normally, that is, all the properties extracted from the TNEF attachment should be used.</span></span> <span data-ttu-id="ad258-123">Если значения не совпадают, все свойства из вложения TNEF следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="ad258-123">If the values do not match, all the properties from the TNEF attachment should be ignored.</span></span> <span data-ttu-id="ad258-124">Если это свойство не задано, файл TNEF должен считаться принадлежащим этому сообщению, и остальные свойства, извлеченные из него, следует использовать.</span><span class="sxs-lookup"><span data-stu-id="ad258-124">If this property is not set, the TNEF file should be considered to belong to this message, and the other properties extracted from it should be used.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ad258-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ad258-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ad258-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ad258-126">Protocol specifications</span></span>

<span data-ttu-id="ad258-127">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad258-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad258-128">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ad258-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ad258-129">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad258-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad258-130">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="ad258-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ad258-131">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad258-131">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad258-132">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="ad258-132">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="ad258-133">[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad258-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad258-134">Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.</span><span class="sxs-lookup"><span data-stu-id="ad258-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ad258-135">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="ad258-135">Header files</span></span>

<span data-ttu-id="ad258-136">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ad258-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad258-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ad258-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad258-138">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="ad258-138">Mapitags.h</span></span>
  
> <span data-ttu-id="ad258-139">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="ad258-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad258-140">См. также</span><span class="sxs-lookup"><span data-stu-id="ad258-140">See also</span></span>



[<span data-ttu-id="ad258-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ad258-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad258-142">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="ad258-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad258-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ad258-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad258-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ad258-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

