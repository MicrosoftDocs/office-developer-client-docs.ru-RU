---
title: Каноническое свойство PidLidTaskDeadOccurrence
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDeadOccurrence
api_type:
- COM
ms.assetid: e78287ff-f8cc-45ea-8da8-e7a7359e651c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0b740368aae43549e81cf3f4f6de40526c505b6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303432"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a><span data-ttu-id="1b3c4-103">Каноническое свойство PidLidTaskDeadOccurrence</span><span class="sxs-lookup"><span data-stu-id="1b3c4-103">PidLidTaskDeadOccurrence Canonical Property</span></span>

  
  
<span data-ttu-id="1b3c4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b3c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b3c4-105">Указывает, должны ли создаваться новые экземпляры.</span><span class="sxs-lookup"><span data-stu-id="1b3c4-105">Indicates whether new occurrences must be generated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b3c4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1b3c4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b3c4-107">Диспидтаскдеадоккур</span><span class="sxs-lookup"><span data-stu-id="1b3c4-107">dispidTaskDeadOccur</span></span>  <br/> |
|<span data-ttu-id="1b3c4-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="1b3c4-108">Property set:</span></span>  <br/> |<span data-ttu-id="1b3c4-109">Псетид_таск</span><span class="sxs-lookup"><span data-stu-id="1b3c4-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="1b3c4-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="1b3c4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1b3c4-111">0x00008109</span><span class="sxs-lookup"><span data-stu-id="1b3c4-111">0x00008109</span></span>  <br/> |
|<span data-ttu-id="1b3c4-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1b3c4-112">Data type:</span></span>  <br/> |<span data-ttu-id="1b3c4-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1b3c4-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1b3c4-114">Область:</span><span class="sxs-lookup"><span data-stu-id="1b3c4-114">Area:</span></span>  <br/> |<span data-ttu-id="1b3c4-115">Задача</span><span class="sxs-lookup"><span data-stu-id="1b3c4-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b3c4-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="1b3c4-116">Remarks</span></span>

<span data-ttu-id="1b3c4-117">Шаблон повторения больше не действует, если последний экземпляр находится в прошлое, или если было создано заданное число экземпляров.</span><span class="sxs-lookup"><span data-stu-id="1b3c4-117">A recurrence pattern is no longer in effect when its final instance is in the past or its specified number of instances has been generated.</span></span> <span data-ttu-id="1b3c4-118">Клиент задает для этого свойства значение FALSE для новой задачи или значение TRUE при создании последнего экземпляра повторяющейся задачи.</span><span class="sxs-lookup"><span data-stu-id="1b3c4-118">The client sets this property to FALSE for a new task or to TRUE when it generates the last instance of a recurring task.</span></span> <span data-ttu-id="1b3c4-119">При копировании задачи для создания нового экземпляра этому свойству присваивается значение TRUE для копии, которая является завершенным экземпляром.</span><span class="sxs-lookup"><span data-stu-id="1b3c4-119">When you copy a task to generate a new instance, this property is set to TRUE on the copy, which is the completed instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1b3c4-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1b3c4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1b3c4-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1b3c4-121">Protocol specifications</span></span>

<span data-ttu-id="1b3c4-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b3c4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b3c4-123">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1b3c4-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1b3c4-124">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b3c4-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b3c4-125">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="1b3c4-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="1b3c4-126">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="1b3c4-126">Header files</span></span>

<span data-ttu-id="1b3c4-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="1b3c4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b3c4-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1b3c4-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b3c4-129">См. также</span><span class="sxs-lookup"><span data-stu-id="1b3c4-129">See also</span></span>



[<span data-ttu-id="1b3c4-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1b3c4-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b3c4-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="1b3c4-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b3c4-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1b3c4-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b3c4-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1b3c4-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

