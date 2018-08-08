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
ms.openlocfilehash: 6e53d91a80d7e3b3bb4bf02ff3446eb385293c6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810605"
---
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="99c37-103">Каноническое свойство PidLidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="99c37-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="99c37-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99c37-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99c37-105">Указывает тип изменения, внесенные последнего к задаче.</span><span class="sxs-lookup"><span data-stu-id="99c37-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="99c37-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="99c37-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="99c37-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="99c37-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="99c37-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="99c37-108">Property set:</span></span>  <br/> |<span data-ttu-id="99c37-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="99c37-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="99c37-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="99c37-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="99c37-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="99c37-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="99c37-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="99c37-112">Data type:</span></span>  <br/> |<span data-ttu-id="99c37-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="99c37-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="99c37-114">Область:</span><span class="sxs-lookup"><span data-stu-id="99c37-114">Area:</span></span>  <br/> |<span data-ttu-id="99c37-115">Task</span><span class="sxs-lookup"><span data-stu-id="99c37-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99c37-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="99c37-116">Remarks</span></span>

<span data-ttu-id="99c37-117">Если значение этого свойства, свойство **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) необходимо также установить для текущего времени.</span><span class="sxs-lookup"><span data-stu-id="99c37-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="99c37-118">В следующей таблице показаны **dispidTaskHistory** значения свойств, перечисленных в порядке убывания приоритета.</span><span class="sxs-lookup"><span data-stu-id="99c37-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="99c37-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="99c37-119">**Value**</span></span>|<span data-ttu-id="99c37-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="99c37-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99c37-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="99c37-121">0x00000004</span></span>  <br/> |<span data-ttu-id="99c37-122">Изменения свойства **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="99c37-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="99c37-123">0x00000003</span><span class="sxs-lookup"><span data-stu-id="99c37-123">0x00000003</span></span>  <br/> |<span data-ttu-id="99c37-124">Свойство был изменен.</span><span class="sxs-lookup"><span data-stu-id="99c37-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="99c37-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="99c37-125">0x00000001</span></span>  <br/> |<span data-ttu-id="99c37-126">Назначена задача принимаются этой задачи.</span><span class="sxs-lookup"><span data-stu-id="99c37-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="99c37-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="99c37-127">0x00000002</span></span>  <br/> |<span data-ttu-id="99c37-128">Назначена задача отклонено этой задачи.</span><span class="sxs-lookup"><span data-stu-id="99c37-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="99c37-129">0x00000005</span><span class="sxs-lookup"><span data-stu-id="99c37-129">0x00000005</span></span>  <br/> |<span data-ttu-id="99c37-130">Задача назначена назначена задача.</span><span class="sxs-lookup"><span data-stu-id="99c37-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="99c37-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99c37-131">0x00000000</span></span>  <br/> |<span data-ttu-id="99c37-132">Не были изменены.</span><span class="sxs-lookup"><span data-stu-id="99c37-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="99c37-133">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="99c37-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="99c37-134">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="99c37-134">Protocol specifications</span></span>

<span data-ttu-id="99c37-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99c37-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99c37-136">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="99c37-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="99c37-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99c37-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99c37-138">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="99c37-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="99c37-139">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="99c37-139">Header files</span></span>

<span data-ttu-id="99c37-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="99c37-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="99c37-141">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="99c37-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99c37-142">См. также</span><span class="sxs-lookup"><span data-stu-id="99c37-142">See also</span></span>



[<span data-ttu-id="99c37-143">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="99c37-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="99c37-144">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="99c37-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="99c37-145">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="99c37-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="99c37-146">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="99c37-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

