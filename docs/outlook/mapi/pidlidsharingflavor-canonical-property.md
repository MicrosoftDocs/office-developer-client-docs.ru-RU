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
ms.openlocfilehash: ad98be2a457a1f7152f428f4aae834848a3b0536
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564558"
---
# <a name="pidlidsharingflavor-canonical-property"></a><span data-ttu-id="00455-103">Каноническое свойство PidLidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="00455-103">PidLidSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="00455-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00455-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00455-105">Определяет, как свойство общего доступа сообщения.</span><span class="sxs-lookup"><span data-stu-id="00455-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00455-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="00455-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00455-107">dispidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="00455-107">dispidSharingFlavor</span></span>  <br/> |
|<span data-ttu-id="00455-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="00455-108">Property set:</span></span>  <br/> |<span data-ttu-id="00455-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="00455-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="00455-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="00455-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="00455-111">0x00008A18</span><span class="sxs-lookup"><span data-stu-id="00455-111">0x00008A18</span></span>  <br/> |
|<span data-ttu-id="00455-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="00455-112">Data type:</span></span>  <br/> |<span data-ttu-id="00455-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="00455-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="00455-114">Область:</span><span class="sxs-lookup"><span data-stu-id="00455-114">Area:</span></span>  <br/> |<span data-ttu-id="00455-115">Sharing</span><span class="sxs-lookup"><span data-stu-id="00455-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00455-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="00455-116">Remarks</span></span>

<span data-ttu-id="00455-117">Значение этого свойства должно быть одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="00455-117">The value of this property must be one of the following:</span></span>
  
|<span data-ttu-id="00455-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="00455-118">**Value**</span></span>|<span data-ttu-id="00455-119">**Тип объекта, общий доступ к сообщения**</span><span class="sxs-lookup"><span data-stu-id="00455-119">**Type of Sharing Message object**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00455-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="00455-120">0x00020310</span></span>  <br/> |<span data-ttu-id="00455-121">Приглашения на общий доступ для отдельной папки.</span><span class="sxs-lookup"><span data-stu-id="00455-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="00455-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="00455-122">0x00000310</span></span>  <br/> |<span data-ttu-id="00455-123">Приглашения на общий доступ к папке, которая не является отдельной папки.</span><span class="sxs-lookup"><span data-stu-id="00455-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="00455-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="00455-124">0x00020500</span></span>  <br/> |<span data-ttu-id="00455-125">Запрос на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="00455-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="00455-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="00455-126">0x00020710</span></span>  <br/> |<span data-ttu-id="00455-127">Оба приглашения на общий доступ для отдельной папки и запрос на общий доступ для получателя соответствует специальную папку.</span><span class="sxs-lookup"><span data-stu-id="00455-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="00455-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="00455-128">0x00025100</span></span>  <br/> |<span data-ttu-id="00455-129">Общего доступа ответа, отклонения запроса.</span><span class="sxs-lookup"><span data-stu-id="00455-129">A sharing response denying a request.</span></span>  <br/> |
|<span data-ttu-id="00455-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="00455-130">0x00023310</span></span>  <br/> |<span data-ttu-id="00455-131">Ответ общего доступа, принимает запрос (также тип приглашение для совместного использования).</span><span class="sxs-lookup"><span data-stu-id="00455-131">A sharing response accepting a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="00455-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="00455-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00455-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="00455-133">Protocol specifications</span></span>

<span data-ttu-id="00455-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00455-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00455-135">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="00455-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00455-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00455-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00455-137">Открывает общий доступ папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="00455-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00455-138">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="00455-138">Header files</span></span>

<span data-ttu-id="00455-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00455-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="00455-140">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="00455-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00455-141">См. также</span><span class="sxs-lookup"><span data-stu-id="00455-141">See also</span></span>



[<span data-ttu-id="00455-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="00455-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00455-143">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="00455-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00455-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="00455-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00455-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="00455-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

