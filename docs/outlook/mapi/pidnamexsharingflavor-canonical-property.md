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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392125"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="af38f-103">Каноническое свойство PidNameXSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="af38f-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="af38f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af38f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af38f-105">Представляет значение свойства **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="af38f-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af38f-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="af38f-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="af38f-107">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="af38f-107">None</span></span>  <br/> |
|<span data-ttu-id="af38f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="af38f-108">Property set:</span></span>  <br/> |<span data-ttu-id="af38f-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="af38f-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="af38f-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="af38f-110">Property name:</span></span>  <br/> |<span data-ttu-id="af38f-111">Общий доступ к конфигурация X</span><span class="sxs-lookup"><span data-stu-id="af38f-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="af38f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="af38f-112">Data type:</span></span>  <br/> |<span data-ttu-id="af38f-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="af38f-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="af38f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="af38f-114">Area:</span></span>  <br/> |<span data-ttu-id="af38f-115">Sharing</span><span class="sxs-lookup"><span data-stu-id="af38f-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af38f-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="af38f-116">Remarks</span></span>

<span data-ttu-id="af38f-117">Свойство **dispidSharingFlavor** должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="af38f-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="af38f-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="af38f-118">**Value**</span></span>|<span data-ttu-id="af38f-119">**Тип общего доступа к сообщения**</span><span class="sxs-lookup"><span data-stu-id="af38f-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af38f-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="af38f-120">0x00020310</span></span>  <br/> |<span data-ttu-id="af38f-121">Приглашения на общий доступ для отдельной папки.</span><span class="sxs-lookup"><span data-stu-id="af38f-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="af38f-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="af38f-122">0x00000310</span></span>  <br/> |<span data-ttu-id="af38f-123">Приглашения на общий доступ к папке, которая не является отдельной папки.</span><span class="sxs-lookup"><span data-stu-id="af38f-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="af38f-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="af38f-124">0x00020500</span></span>  <br/> |<span data-ttu-id="af38f-125">Запрос на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="af38f-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="af38f-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="af38f-126">0x00020710</span></span>  <br/> |<span data-ttu-id="af38f-127">Оба приглашения на общий доступ для отдельной папки и запрос на общий доступ для получателя соответствует специальную папку.</span><span class="sxs-lookup"><span data-stu-id="af38f-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="af38f-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="af38f-128">0x00025100</span></span>  <br/> |<span data-ttu-id="af38f-129">Ответ общего доступа, не дает запрос.</span><span class="sxs-lookup"><span data-stu-id="af38f-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="af38f-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="af38f-130">0x00023310</span></span>  <br/> |<span data-ttu-id="af38f-131">Ответ общего доступа, который принимает запрос (также тип приглашение для совместного использования).</span><span class="sxs-lookup"><span data-stu-id="af38f-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="af38f-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="af38f-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af38f-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="af38f-133">Protocol specifications</span></span>

<span data-ttu-id="af38f-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af38f-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af38f-135">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="af38f-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af38f-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af38f-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af38f-137">Открывает общий доступ папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="af38f-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af38f-138">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="af38f-138">Header files</span></span>

<span data-ttu-id="af38f-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af38f-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="af38f-140">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="af38f-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af38f-141">См. также</span><span class="sxs-lookup"><span data-stu-id="af38f-141">See also</span></span>



[<span data-ttu-id="af38f-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="af38f-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af38f-143">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="af38f-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af38f-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="af38f-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af38f-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="af38f-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

