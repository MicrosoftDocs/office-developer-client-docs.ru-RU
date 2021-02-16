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
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="12fee-103">Каноническое свойство PidNameXSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="12fee-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="12fee-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12fee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12fee-105">Представляет значение свойства **dispidSharingFlavor** ([PidLidSharingFlavor).](pidlidsharingflavor-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="12fee-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12fee-106">Дружелюбные имена:</span><span class="sxs-lookup"><span data-stu-id="12fee-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="12fee-107">Нет</span><span class="sxs-lookup"><span data-stu-id="12fee-107">None</span></span>  <br/> |
|<span data-ttu-id="12fee-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="12fee-108">Property set:</span></span>  <br/> |<span data-ttu-id="12fee-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="12fee-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="12fee-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="12fee-110">Property name:</span></span>  <br/> |<span data-ttu-id="12fee-111">X-Sharing-Flavor</span><span class="sxs-lookup"><span data-stu-id="12fee-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="12fee-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="12fee-112">Data type:</span></span>  <br/> |<span data-ttu-id="12fee-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="12fee-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="12fee-114">Область:</span><span class="sxs-lookup"><span data-stu-id="12fee-114">Area:</span></span>  <br/> |<span data-ttu-id="12fee-115">Общий доступ</span><span class="sxs-lookup"><span data-stu-id="12fee-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12fee-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="12fee-116">Remarks</span></span>

<span data-ttu-id="12fee-117">Свойство **dispidSharingFlavor** должно иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="12fee-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="12fee-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="12fee-118">**Value**</span></span>|<span data-ttu-id="12fee-119">**Тип сообщения общего доступа**</span><span class="sxs-lookup"><span data-stu-id="12fee-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12fee-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="12fee-120">0x00020310</span></span>  <br/> |<span data-ttu-id="12fee-121">Приглашение к совместному доступу для специальной папки.</span><span class="sxs-lookup"><span data-stu-id="12fee-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="12fee-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="12fee-122">0x00000310</span></span>  <br/> |<span data-ttu-id="12fee-123">Приглашение к совместному доступу для папки, которая не является специальной.</span><span class="sxs-lookup"><span data-stu-id="12fee-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="12fee-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="12fee-124">0x00020500</span></span>  <br/> |<span data-ttu-id="12fee-125">Запрос на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="12fee-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="12fee-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="12fee-126">0x00020710</span></span>  <br/> |<span data-ttu-id="12fee-127">Приглашение к совместному доступу для специальной папки и запрос на общий доступ для эквивалентной специальной папки получателя.</span><span class="sxs-lookup"><span data-stu-id="12fee-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="12fee-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="12fee-128">0x00025100</span></span>  <br/> |<span data-ttu-id="12fee-129">Ответ общего доступа, который отказано в запросе.</span><span class="sxs-lookup"><span data-stu-id="12fee-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="12fee-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="12fee-130">0x00023310</span></span>  <br/> |<span data-ttu-id="12fee-131">Ответ для общего доступа, который принимает запрос (также тип приглашения к совместному доступу).</span><span class="sxs-lookup"><span data-stu-id="12fee-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="12fee-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="12fee-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="12fee-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="12fee-133">Protocol specifications</span></span>

<span data-ttu-id="12fee-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12fee-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12fee-135">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="12fee-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="12fee-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12fee-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12fee-137">Папки почтовых ящиков разделяются между клиентами.</span><span class="sxs-lookup"><span data-stu-id="12fee-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="12fee-138">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="12fee-138">Header files</span></span>

<span data-ttu-id="12fee-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12fee-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="12fee-140">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="12fee-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12fee-141">См. также</span><span class="sxs-lookup"><span data-stu-id="12fee-141">See also</span></span>



[<span data-ttu-id="12fee-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="12fee-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12fee-143">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="12fee-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12fee-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="12fee-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12fee-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="12fee-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

