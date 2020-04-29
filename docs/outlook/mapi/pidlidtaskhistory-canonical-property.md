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
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="6ade9-103">Каноническое свойство PidLidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="6ade9-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="6ade9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ade9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ade9-105">Указывает тип изменения, который был выполнен последним в задаче.</span><span class="sxs-lookup"><span data-stu-id="6ade9-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ade9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6ade9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ade9-107">диспидтаскхистори</span><span class="sxs-lookup"><span data-stu-id="6ade9-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="6ade9-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="6ade9-108">Property set:</span></span>  <br/> |<span data-ttu-id="6ade9-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="6ade9-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="6ade9-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="6ade9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6ade9-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="6ade9-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="6ade9-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6ade9-112">Data type:</span></span>  <br/> |<span data-ttu-id="6ade9-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6ade9-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6ade9-114">Область:</span><span class="sxs-lookup"><span data-stu-id="6ade9-114">Area:</span></span>  <br/> |<span data-ttu-id="6ade9-115">Задача</span><span class="sxs-lookup"><span data-stu-id="6ade9-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ade9-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="6ade9-116">Remarks</span></span>

<span data-ttu-id="6ade9-117">Если значение этого свойства задано, свойству **диспидтаскластупдате** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) также должно быть присвоено текущее время.</span><span class="sxs-lookup"><span data-stu-id="6ade9-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="6ade9-118">В следующей таблице приведены значения свойств **диспидтаскхистори** , перечисленные в порядке убывания приоритета.</span><span class="sxs-lookup"><span data-stu-id="6ade9-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="6ade9-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="6ade9-119">**Value**</span></span>|<span data-ttu-id="6ade9-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6ade9-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ade9-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="6ade9-121">0x00000004</span></span>  <br/> |<span data-ttu-id="6ade9-122">Изменено свойство **диспидтаскдуедате** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6ade9-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="6ade9-123">0x00000003</span><span class="sxs-lookup"><span data-stu-id="6ade9-123">0x00000003</span></span>  <br/> |<span data-ttu-id="6ade9-124">Изменено другое свойство.</span><span class="sxs-lookup"><span data-stu-id="6ade9-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="6ade9-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6ade9-125">0x00000001</span></span>  <br/> |<span data-ttu-id="6ade9-126">Уполномоченная задача приняла эту задачу.</span><span class="sxs-lookup"><span data-stu-id="6ade9-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="6ade9-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6ade9-127">0x00000002</span></span>  <br/> |<span data-ttu-id="6ade9-128">Задача, которой назначена задача, отклонила эту задачу.</span><span class="sxs-lookup"><span data-stu-id="6ade9-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="6ade9-129">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6ade9-129">0x00000005</span></span>  <br/> |<span data-ttu-id="6ade9-130">Задача назначена уполномоченному пользователю задачи.</span><span class="sxs-lookup"><span data-stu-id="6ade9-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="6ade9-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ade9-131">0x00000000</span></span>  <br/> |<span data-ttu-id="6ade9-132">Изменения не были внесены.</span><span class="sxs-lookup"><span data-stu-id="6ade9-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6ade9-133">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6ade9-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ade9-134">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6ade9-134">Protocol specifications</span></span>

<span data-ttu-id="6ade9-135">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ade9-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ade9-136">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6ade9-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6ade9-137">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ade9-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ade9-138">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="6ade9-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6ade9-139">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6ade9-139">Header files</span></span>

<span data-ttu-id="6ade9-140">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="6ade9-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ade9-141">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6ade9-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ade9-142">См. также</span><span class="sxs-lookup"><span data-stu-id="6ade9-142">See also</span></span>



[<span data-ttu-id="6ade9-143">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6ade9-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ade9-144">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="6ade9-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ade9-145">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6ade9-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ade9-146">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6ade9-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

