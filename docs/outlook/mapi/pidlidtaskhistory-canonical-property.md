---
title: Каноническое свойство PidLidTaskHistory
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 39f2e6aeb4026f0b33be08b3bd8123283e5df3e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303012"
---
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="db49b-103">Каноническое свойство PidLidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="db49b-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="db49b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db49b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db49b-105">Указывает тип изменений, которые в последний раз были сделаны в задачу.</span><span class="sxs-lookup"><span data-stu-id="db49b-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db49b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="db49b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="db49b-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="db49b-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="db49b-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="db49b-108">Property set:</span></span>  <br/> |<span data-ttu-id="db49b-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="db49b-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="db49b-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="db49b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="db49b-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="db49b-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="db49b-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="db49b-112">Data type:</span></span>  <br/> |<span data-ttu-id="db49b-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="db49b-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="db49b-114">Область:</span><span class="sxs-lookup"><span data-stu-id="db49b-114">Area:</span></span>  <br/> |<span data-ttu-id="db49b-115">Задача</span><span class="sxs-lookup"><span data-stu-id="db49b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db49b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="db49b-116">Remarks</span></span>

<span data-ttu-id="db49b-117">Когда значение этого свойства заданной, свойство **dispidTaskLastUpdate** [(PidLidTaskLastUpdate)](pidlidtasklastupdate-canonical-property.md)также должно быть задавано текущему времени.</span><span class="sxs-lookup"><span data-stu-id="db49b-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="db49b-118">В следующей таблице показаны **значения свойств dispidTaskHistory,** перечисленные в порядке уменьшения приоритета.</span><span class="sxs-lookup"><span data-stu-id="db49b-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="db49b-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="db49b-119">**Value**</span></span>|<span data-ttu-id="db49b-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="db49b-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="db49b-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="db49b-121">0x00000004</span></span>  <br/> |<span data-ttu-id="db49b-122">Изменено **свойство dispidTaskDueDate** [(PidLidTaskDueDate).](pidlidtaskduedate-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db49b-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="db49b-123">0x00000003</span><span class="sxs-lookup"><span data-stu-id="db49b-123">0x00000003</span></span>  <br/> |<span data-ttu-id="db49b-124">Другое свойство было изменено.</span><span class="sxs-lookup"><span data-stu-id="db49b-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="db49b-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="db49b-125">0x00000001</span></span>  <br/> |<span data-ttu-id="db49b-126">Назначение задачи согласилось с этой задачей.</span><span class="sxs-lookup"><span data-stu-id="db49b-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="db49b-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="db49b-127">0x00000002</span></span>  <br/> |<span data-ttu-id="db49b-128">Назначение задачи отклоняет эту задачу.</span><span class="sxs-lookup"><span data-stu-id="db49b-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="db49b-129">0x00000005</span><span class="sxs-lookup"><span data-stu-id="db49b-129">0x00000005</span></span>  <br/> |<span data-ttu-id="db49b-130">Задача была назначена назначено назначить задачу.</span><span class="sxs-lookup"><span data-stu-id="db49b-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="db49b-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db49b-131">0x00000000</span></span>  <br/> |<span data-ttu-id="db49b-132">Изменения не были внесены.</span><span class="sxs-lookup"><span data-stu-id="db49b-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="db49b-133">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="db49b-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="db49b-134">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="db49b-134">Protocol specifications</span></span>

<span data-ttu-id="db49b-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db49b-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db49b-136">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="db49b-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="db49b-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db49b-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db49b-138">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="db49b-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="db49b-139">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="db49b-139">Header files</span></span>

<span data-ttu-id="db49b-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="db49b-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="db49b-141">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="db49b-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db49b-142">См. также</span><span class="sxs-lookup"><span data-stu-id="db49b-142">See also</span></span>



[<span data-ttu-id="db49b-143">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="db49b-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="db49b-144">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="db49b-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="db49b-145">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="db49b-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="db49b-146">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="db49b-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

