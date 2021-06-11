---
title: Каноническое свойство PidLidTaskMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMode
api_type:
- COM
ms.assetid: 185db683-301a-4d91-a583-6959853fa1ad
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d0ae319a6b5fa4c901ec7d318c7ebdd216a2adeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357941"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="b91fc-103">Каноническое свойство PidLidTaskMode</span><span class="sxs-lookup"><span data-stu-id="b91fc-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="b91fc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b91fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b91fc-105">Указывает состояние назначения задачи.</span><span class="sxs-lookup"><span data-stu-id="b91fc-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b91fc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b91fc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b91fc-107">dispidTaskMode</span><span class="sxs-lookup"><span data-stu-id="b91fc-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="b91fc-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b91fc-108">Property set:</span></span>  <br/> |<span data-ttu-id="b91fc-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b91fc-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b91fc-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b91fc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b91fc-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="b91fc-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="b91fc-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b91fc-112">Data type:</span></span>  <br/> |<span data-ttu-id="b91fc-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b91fc-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b91fc-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b91fc-114">Area:</span></span>  <br/> |<span data-ttu-id="b91fc-115">Задача</span><span class="sxs-lookup"><span data-stu-id="b91fc-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b91fc-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b91fc-116">Remarks</span></span>

<span data-ttu-id="b91fc-117">Значение должно быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="b91fc-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="b91fc-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b91fc-118">**Value**</span></span>|<span data-ttu-id="b91fc-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b91fc-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b91fc-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b91fc-120">0x00000000</span></span>  <br/> |<span data-ttu-id="b91fc-121">Задача не назначена.</span><span class="sxs-lookup"><span data-stu-id="b91fc-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="b91fc-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b91fc-122">0x00000001</span></span>  <br/> |<span data-ttu-id="b91fc-123">Задача встроена в запрос задачи.</span><span class="sxs-lookup"><span data-stu-id="b91fc-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="b91fc-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b91fc-124">0x00000002</span></span>  <br/> |<span data-ttu-id="b91fc-125">Задача была принята назначением задачи.</span><span class="sxs-lookup"><span data-stu-id="b91fc-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="b91fc-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b91fc-126">0x00000003</span></span>  <br/> |<span data-ttu-id="b91fc-127">Задача была отклонена назначаемой задачей.</span><span class="sxs-lookup"><span data-stu-id="b91fc-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="b91fc-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b91fc-128">0x00000004</span></span>  <br/> |<span data-ttu-id="b91fc-129">Задача встроена в обновление задачи.</span><span class="sxs-lookup"><span data-stu-id="b91fc-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="b91fc-130">0x00000005</span><span class="sxs-lookup"><span data-stu-id="b91fc-130">0x00000005</span></span>  <br/> |<span data-ttu-id="b91fc-131">Задача была назначена назначению задачи.</span><span class="sxs-lookup"><span data-stu-id="b91fc-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b91fc-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b91fc-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b91fc-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b91fc-133">Protocol specifications</span></span>

<span data-ttu-id="b91fc-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b91fc-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b91fc-135">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="b91fc-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b91fc-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b91fc-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b91fc-137">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="b91fc-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b91fc-138">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="b91fc-138">Header files</span></span>

<span data-ttu-id="b91fc-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b91fc-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="b91fc-140">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b91fc-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b91fc-141">См. также</span><span class="sxs-lookup"><span data-stu-id="b91fc-141">See also</span></span>



[<span data-ttu-id="b91fc-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b91fc-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b91fc-143">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b91fc-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b91fc-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b91fc-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b91fc-145">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="b91fc-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

