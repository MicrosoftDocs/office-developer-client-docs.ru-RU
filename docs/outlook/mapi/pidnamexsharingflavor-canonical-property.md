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
ms.openlocfilehash: bcdca783778e1a310be638ce376d408acf0b247f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580042"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="56df1-103">Каноническое свойство PidNameXSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="56df1-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="56df1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56df1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56df1-105">Представляет значение свойства **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="56df1-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="56df1-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="56df1-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="56df1-107">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="56df1-107">None</span></span>  <br/> |
|<span data-ttu-id="56df1-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="56df1-108">Property set:</span></span>  <br/> |<span data-ttu-id="56df1-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="56df1-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="56df1-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="56df1-110">Property name:</span></span>  <br/> |<span data-ttu-id="56df1-111">Общий доступ к конфигурация X</span><span class="sxs-lookup"><span data-stu-id="56df1-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="56df1-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="56df1-112">Data type:</span></span>  <br/> |<span data-ttu-id="56df1-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="56df1-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="56df1-114">Область:</span><span class="sxs-lookup"><span data-stu-id="56df1-114">Area:</span></span>  <br/> |<span data-ttu-id="56df1-115">Sharing</span><span class="sxs-lookup"><span data-stu-id="56df1-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56df1-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="56df1-116">Remarks</span></span>

<span data-ttu-id="56df1-117">Свойство **dispidSharingFlavor** должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="56df1-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="56df1-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="56df1-118">**Value**</span></span>|<span data-ttu-id="56df1-119">**Тип общего доступа к сообщения**</span><span class="sxs-lookup"><span data-stu-id="56df1-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="56df1-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="56df1-120">0x00020310</span></span>  <br/> |<span data-ttu-id="56df1-121">Приглашения на общий доступ для отдельной папки.</span><span class="sxs-lookup"><span data-stu-id="56df1-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="56df1-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="56df1-122">0x00000310</span></span>  <br/> |<span data-ttu-id="56df1-123">Приглашения на общий доступ к папке, которая не является отдельной папки.</span><span class="sxs-lookup"><span data-stu-id="56df1-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="56df1-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="56df1-124">0x00020500</span></span>  <br/> |<span data-ttu-id="56df1-125">Запрос на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="56df1-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="56df1-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="56df1-126">0x00020710</span></span>  <br/> |<span data-ttu-id="56df1-127">Оба приглашения на общий доступ для отдельной папки и запрос на общий доступ для получателя соответствует специальную папку.</span><span class="sxs-lookup"><span data-stu-id="56df1-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="56df1-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="56df1-128">0x00025100</span></span>  <br/> |<span data-ttu-id="56df1-129">Ответ общего доступа, не дает запрос.</span><span class="sxs-lookup"><span data-stu-id="56df1-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="56df1-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="56df1-130">0x00023310</span></span>  <br/> |<span data-ttu-id="56df1-131">Ответ общего доступа, который принимает запрос (также тип приглашение для совместного использования).</span><span class="sxs-lookup"><span data-stu-id="56df1-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="56df1-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="56df1-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="56df1-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="56df1-133">Protocol specifications</span></span>

<span data-ttu-id="56df1-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56df1-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56df1-135">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="56df1-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="56df1-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56df1-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56df1-137">Открывает общий доступ папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="56df1-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="56df1-138">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="56df1-138">Header files</span></span>

<span data-ttu-id="56df1-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56df1-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="56df1-140">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="56df1-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56df1-141">См. также</span><span class="sxs-lookup"><span data-stu-id="56df1-141">See also</span></span>



[<span data-ttu-id="56df1-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="56df1-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56df1-143">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="56df1-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56df1-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="56df1-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56df1-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="56df1-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

