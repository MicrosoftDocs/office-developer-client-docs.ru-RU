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
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="d8961-103">Каноническое свойство PidLidTaskMode</span><span class="sxs-lookup"><span data-stu-id="d8961-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="d8961-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8961-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8961-105">Указывает состояние назначения задачи.</span><span class="sxs-lookup"><span data-stu-id="d8961-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8961-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d8961-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d8961-107">диспидтаскмоде</span><span class="sxs-lookup"><span data-stu-id="d8961-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="d8961-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d8961-108">Property set:</span></span>  <br/> |<span data-ttu-id="d8961-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d8961-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d8961-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="d8961-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d8961-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="d8961-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="d8961-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d8961-112">Data type:</span></span>  <br/> |<span data-ttu-id="d8961-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d8961-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d8961-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d8961-114">Area:</span></span>  <br/> |<span data-ttu-id="d8961-115">Задача</span><span class="sxs-lookup"><span data-stu-id="d8961-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8961-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="d8961-116">Remarks</span></span>

<span data-ttu-id="d8961-117">Значение должно быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="d8961-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="d8961-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d8961-118">**Value**</span></span>|<span data-ttu-id="d8961-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d8961-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8961-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d8961-120">0x00000000</span></span>  <br/> |<span data-ttu-id="d8961-121">Задача не назначена.</span><span class="sxs-lookup"><span data-stu-id="d8961-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="d8961-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d8961-122">0x00000001</span></span>  <br/> |<span data-ttu-id="d8961-123">Задача внедрена в запрос задачи.</span><span class="sxs-lookup"><span data-stu-id="d8961-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="d8961-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d8961-124">0x00000002</span></span>  <br/> |<span data-ttu-id="d8961-125">Задача принята уполномоченной задачей.</span><span class="sxs-lookup"><span data-stu-id="d8961-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="d8961-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="d8961-126">0x00000003</span></span>  <br/> |<span data-ttu-id="d8961-127">Задача была отклонена уполномоченной задачей.</span><span class="sxs-lookup"><span data-stu-id="d8961-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="d8961-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d8961-128">0x00000004</span></span>  <br/> |<span data-ttu-id="d8961-129">Задача внедрена в обновление задачи.</span><span class="sxs-lookup"><span data-stu-id="d8961-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="d8961-130">0x00000005</span><span class="sxs-lookup"><span data-stu-id="d8961-130">0x00000005</span></span>  <br/> |<span data-ttu-id="d8961-131">Задача назначена назначению задачи.</span><span class="sxs-lookup"><span data-stu-id="d8961-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d8961-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d8961-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d8961-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d8961-133">Protocol specifications</span></span>

<span data-ttu-id="d8961-134">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8961-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8961-135">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d8961-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d8961-136">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8961-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8961-137">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="d8961-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d8961-138">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d8961-138">Header files</span></span>

<span data-ttu-id="d8961-139">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d8961-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="d8961-140">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d8961-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8961-141">См. также</span><span class="sxs-lookup"><span data-stu-id="d8961-141">See also</span></span>



[<span data-ttu-id="d8961-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d8961-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d8961-143">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="d8961-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d8961-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d8961-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d8961-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d8961-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

