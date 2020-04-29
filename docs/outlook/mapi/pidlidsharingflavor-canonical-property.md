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
# <a name="pidlidsharingflavor-canonical-property"></a><span data-ttu-id="d268f-103">Каноническое свойство PidLidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="d268f-103">PidLidSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="d268f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d268f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d268f-105">Указывает как свойство сообщения о совместном доступе.</span><span class="sxs-lookup"><span data-stu-id="d268f-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d268f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d268f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d268f-107">диспидшарингфлавор</span><span class="sxs-lookup"><span data-stu-id="d268f-107">dispidSharingFlavor</span></span>  <br/> |
|<span data-ttu-id="d268f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d268f-108">Property set:</span></span>  <br/> |<span data-ttu-id="d268f-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="d268f-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="d268f-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="d268f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d268f-111">0x00008A18</span><span class="sxs-lookup"><span data-stu-id="d268f-111">0x00008A18</span></span>  <br/> |
|<span data-ttu-id="d268f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d268f-112">Data type:</span></span>  <br/> |<span data-ttu-id="d268f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d268f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d268f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d268f-114">Area:</span></span>  <br/> |<span data-ttu-id="d268f-115">Общий доступ</span><span class="sxs-lookup"><span data-stu-id="d268f-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d268f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="d268f-116">Remarks</span></span>

<span data-ttu-id="d268f-117">Значение этого свойства должно быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="d268f-117">The value of this property must be one of the following:</span></span>
  
|<span data-ttu-id="d268f-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d268f-118">**Value**</span></span>|<span data-ttu-id="d268f-119">**Тип объекта сообщения общего доступа**</span><span class="sxs-lookup"><span data-stu-id="d268f-119">**Type of Sharing Message object**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d268f-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="d268f-120">0x00020310</span></span>  <br/> |<span data-ttu-id="d268f-121">Приглашение к совместному использованию для специальной папки.</span><span class="sxs-lookup"><span data-stu-id="d268f-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="d268f-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="d268f-122">0x00000310</span></span>  <br/> |<span data-ttu-id="d268f-123">Приглашение к совместному использованию для папки, которая не является специальной папкой.</span><span class="sxs-lookup"><span data-stu-id="d268f-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="d268f-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="d268f-124">0x00020500</span></span>  <br/> |<span data-ttu-id="d268f-125">Запрос на предоставление общего доступа.</span><span class="sxs-lookup"><span data-stu-id="d268f-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="d268f-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="d268f-126">0x00020710</span></span>  <br/> |<span data-ttu-id="d268f-127">Приглашение к совместному использованию для специальной папки и запрос общего доступа для эквивалентной особой папки получателя.</span><span class="sxs-lookup"><span data-stu-id="d268f-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="d268f-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="d268f-128">0x00025100</span></span>  <br/> |<span data-ttu-id="d268f-129">Ответ общего доступа, запрещающий запрос.</span><span class="sxs-lookup"><span data-stu-id="d268f-129">A sharing response denying a request.</span></span>  <br/> |
|<span data-ttu-id="d268f-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="d268f-130">0x00023310</span></span>  <br/> |<span data-ttu-id="d268f-131">Ответ общего доступа, принимающий запрос (а также тип приглашения на совместное использование).</span><span class="sxs-lookup"><span data-stu-id="d268f-131">A sharing response accepting a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d268f-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d268f-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d268f-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d268f-133">Protocol specifications</span></span>

<span data-ttu-id="d268f-134">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d268f-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d268f-135">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d268f-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d268f-136">[[MS — ОКСШАРЕ]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d268f-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d268f-137">Предоставляет общий доступ к папкам почтового ящика между клиентами.</span><span class="sxs-lookup"><span data-stu-id="d268f-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d268f-138">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d268f-138">Header files</span></span>

<span data-ttu-id="d268f-139">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d268f-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="d268f-140">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d268f-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d268f-141">См. также</span><span class="sxs-lookup"><span data-stu-id="d268f-141">See also</span></span>



[<span data-ttu-id="d268f-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d268f-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d268f-143">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="d268f-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d268f-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d268f-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d268f-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d268f-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

