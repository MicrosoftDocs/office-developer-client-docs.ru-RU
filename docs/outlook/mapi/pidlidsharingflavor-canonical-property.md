---
title: Каноническое свойство PidLidSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 21144af15e7a36f54af3032f735c391b3038305b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327484"
---
# <a name="pidlidsharingflavor-canonical-property"></a><span data-ttu-id="49105-103">Каноническое свойство PidLidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="49105-103">PidLidSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="49105-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49105-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49105-105">Обозначается как свойство общего сообщения.</span><span class="sxs-lookup"><span data-stu-id="49105-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="49105-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="49105-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="49105-107">dispidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="49105-107">dispidSharingFlavor</span></span>  <br/> |
|<span data-ttu-id="49105-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="49105-108">Property set:</span></span>  <br/> |<span data-ttu-id="49105-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="49105-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="49105-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="49105-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="49105-111">0x00008A18</span><span class="sxs-lookup"><span data-stu-id="49105-111">0x00008A18</span></span>  <br/> |
|<span data-ttu-id="49105-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="49105-112">Data type:</span></span>  <br/> |<span data-ttu-id="49105-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="49105-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="49105-114">Область:</span><span class="sxs-lookup"><span data-stu-id="49105-114">Area:</span></span>  <br/> |<span data-ttu-id="49105-115">Доступ</span><span class="sxs-lookup"><span data-stu-id="49105-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49105-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="49105-116">Remarks</span></span>

<span data-ttu-id="49105-117">Значение этого свойства должно быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="49105-117">The value of this property must be one of the following:</span></span>
  
|<span data-ttu-id="49105-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="49105-118">**Value**</span></span>|<span data-ttu-id="49105-119">**Тип объекта Общего доступа к сообщению**</span><span class="sxs-lookup"><span data-stu-id="49105-119">**Type of Sharing Message object**</span></span>|
|:-----|:-----|
|<span data-ttu-id="49105-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="49105-120">0x00020310</span></span>  <br/> |<span data-ttu-id="49105-121">Приглашение к совместному доступу для специальной папки.</span><span class="sxs-lookup"><span data-stu-id="49105-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="49105-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="49105-122">0x00000310</span></span>  <br/> |<span data-ttu-id="49105-123">Приглашение к совместному доступу для папки, которая не является специальной папкой.</span><span class="sxs-lookup"><span data-stu-id="49105-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="49105-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="49105-124">0x00020500</span></span>  <br/> |<span data-ttu-id="49105-125">Запрос на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="49105-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="49105-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="49105-126">0x00020710</span></span>  <br/> |<span data-ttu-id="49105-127">Приглашение к совместному доступу для специальной папки и запрос на общий доступ для эквивалентной специальной папки получателя.</span><span class="sxs-lookup"><span data-stu-id="49105-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="49105-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="49105-128">0x00025100</span></span>  <br/> |<span data-ttu-id="49105-129">Ответ общего доступа, отказывающий запросу.</span><span class="sxs-lookup"><span data-stu-id="49105-129">A sharing response denying a request.</span></span>  <br/> |
|<span data-ttu-id="49105-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="49105-130">0x00023310</span></span>  <br/> |<span data-ttu-id="49105-131">Ответ общего доступа, принимающий запрос (также тип приглашения общего доступа).</span><span class="sxs-lookup"><span data-stu-id="49105-131">A sharing response accepting a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="49105-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="49105-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="49105-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="49105-133">Protocol specifications</span></span>

<span data-ttu-id="49105-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49105-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49105-135">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="49105-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="49105-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49105-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49105-137">Делит папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="49105-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="49105-138">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="49105-138">Header files</span></span>

<span data-ttu-id="49105-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49105-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="49105-140">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="49105-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49105-141">См. также</span><span class="sxs-lookup"><span data-stu-id="49105-141">See also</span></span>



[<span data-ttu-id="49105-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="49105-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49105-143">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="49105-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49105-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="49105-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49105-145">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="49105-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

