---
title: Каноническое свойство PidNameXSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameXSharingFlavor
api_type:
- COM
ms.assetid: 7757fde1-564b-4f3a-9b9e-f80a143690ea
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d2afa598bf9b7949f2e9142611570ebbd048f7e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360888"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="403f5-103">Каноническое свойство PidNameXSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="403f5-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="403f5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="403f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="403f5-105">Представляет значение свойства **диспидшарингфлавор** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="403f5-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="403f5-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="403f5-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="403f5-107">Нет</span><span class="sxs-lookup"><span data-stu-id="403f5-107">None</span></span>  <br/> |
|<span data-ttu-id="403f5-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="403f5-108">Property set:</span></span>  <br/> |<span data-ttu-id="403f5-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="403f5-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="403f5-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="403f5-110">Property name:</span></span>  <br/> |<span data-ttu-id="403f5-111">X – флаг</span><span class="sxs-lookup"><span data-stu-id="403f5-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="403f5-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="403f5-112">Data type:</span></span>  <br/> |<span data-ttu-id="403f5-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="403f5-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="403f5-114">Область:</span><span class="sxs-lookup"><span data-stu-id="403f5-114">Area:</span></span>  <br/> |<span data-ttu-id="403f5-115">Общий доступ</span><span class="sxs-lookup"><span data-stu-id="403f5-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="403f5-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="403f5-116">Remarks</span></span>

<span data-ttu-id="403f5-117">Свойство **диспидшарингфлавор** должно иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="403f5-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="403f5-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="403f5-118">**Value**</span></span>|<span data-ttu-id="403f5-119">**Тип сообщения о совместном доступе**</span><span class="sxs-lookup"><span data-stu-id="403f5-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="403f5-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="403f5-120">0x00020310</span></span>  <br/> |<span data-ttu-id="403f5-121">Приглашение к совместному использованию для специальной папки.</span><span class="sxs-lookup"><span data-stu-id="403f5-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="403f5-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="403f5-122">0x00000310</span></span>  <br/> |<span data-ttu-id="403f5-123">Приглашение к совместному использованию для папки, которая не является специальной папкой.</span><span class="sxs-lookup"><span data-stu-id="403f5-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="403f5-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="403f5-124">0x00020500</span></span>  <br/> |<span data-ttu-id="403f5-125">Запрос на предоставление общего доступа.</span><span class="sxs-lookup"><span data-stu-id="403f5-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="403f5-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="403f5-126">0x00020710</span></span>  <br/> |<span data-ttu-id="403f5-127">Приглашение к совместному использованию для специальной папки и запрос общего доступа для эквивалентной особой папки получателя.</span><span class="sxs-lookup"><span data-stu-id="403f5-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="403f5-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="403f5-128">0x00025100</span></span>  <br/> |<span data-ttu-id="403f5-129">Ответ общего доступа, который запрещает запрос.</span><span class="sxs-lookup"><span data-stu-id="403f5-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="403f5-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="403f5-130">0x00023310</span></span>  <br/> |<span data-ttu-id="403f5-131">Ответ общего доступа, принимающий запрос (а также тип приглашения для совместного доступа).</span><span class="sxs-lookup"><span data-stu-id="403f5-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="403f5-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="403f5-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="403f5-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="403f5-133">Protocol specifications</span></span>

<span data-ttu-id="403f5-134">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="403f5-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="403f5-135">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="403f5-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="403f5-136">[[MS — ОКСШАРЕ]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="403f5-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="403f5-137">Предоставляет общий доступ к папкам почтового ящика между клиентами.</span><span class="sxs-lookup"><span data-stu-id="403f5-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="403f5-138">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="403f5-138">Header files</span></span>

<span data-ttu-id="403f5-139">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="403f5-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="403f5-140">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="403f5-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="403f5-141">См. также</span><span class="sxs-lookup"><span data-stu-id="403f5-141">See also</span></span>



[<span data-ttu-id="403f5-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="403f5-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="403f5-143">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="403f5-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="403f5-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="403f5-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="403f5-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="403f5-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

