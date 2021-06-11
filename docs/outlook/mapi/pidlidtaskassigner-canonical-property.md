---
title: Каноническое свойство PidLidTaskAssigner
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigner
api_type:
- COM
ms.assetid: f7047e4e-0fb3-476b-9568-8f1135e6d970
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ef5f78fa36632227311d037ee61085c677920fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340091"
---
# <a name="pidlidtaskassigner-canonical-property"></a><span data-ttu-id="e897c-103">Каноническое свойство PidLidTaskAssigner</span><span class="sxs-lookup"><span data-stu-id="e897c-103">PidLidTaskAssigner Canonical Property</span></span>

  
  
<span data-ttu-id="e897c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e897c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e897c-105">Имена пользователя, которому в последний раз была назначена задача.</span><span class="sxs-lookup"><span data-stu-id="e897c-105">Names the user who was last assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e897c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e897c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e897c-107">dispidTaskDelegator</span><span class="sxs-lookup"><span data-stu-id="e897c-107">dispidTaskDelegator</span></span>  <br/> |
|<span data-ttu-id="e897c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="e897c-108">Property set:</span></span>  <br/> |<span data-ttu-id="e897c-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e897c-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e897c-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e897c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e897c-111">0x00008121</span><span class="sxs-lookup"><span data-stu-id="e897c-111">0x00008121</span></span>  <br/> |
|<span data-ttu-id="e897c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e897c-112">Data type:</span></span>  <br/> |<span data-ttu-id="e897c-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e897c-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e897c-114">Область:</span><span class="sxs-lookup"><span data-stu-id="e897c-114">Area:</span></span>  <br/> |<span data-ttu-id="e897c-115">Задача</span><span class="sxs-lookup"><span data-stu-id="e897c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e897c-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e897c-116">Remarks</span></span>

<span data-ttu-id="e897c-117">Если задача не назначена, это свойство остается неустановленным.</span><span class="sxs-lookup"><span data-stu-id="e897c-117">If the task has not been assigned, this property is left unset.</span></span> <span data-ttu-id="e897c-118">Так как клиент задает это свойство после получения запроса задачи, свойство не будет заданной на копию задачи.</span><span class="sxs-lookup"><span data-stu-id="e897c-118">Because the client sets this property after the task assignee receives a task request, the property will not be set on the task assigner's copy of the task.</span></span> <span data-ttu-id="e897c-119">Когда клиент добавляет или удаляет назначение задачи из списка назначителей задач в свойстве **dispidTaskMyDelegators** [(PidLidTaskAssigners),](pidlidtaskassigners-canonical-property.md)свойство **dispidTaskDelegator** [(PidLidTaskAssigner)](pidlidtaskassigner-canonical-property.md)должно быть задано добавлено или удалено.</span><span class="sxs-lookup"><span data-stu-id="e897c-119">When the client adds or removes a task assigner from the task assigner list in the **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) property, the **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) property must be set to the added or removed task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e897c-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e897c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e897c-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e897c-121">Protocol specifications</span></span>

<span data-ttu-id="e897c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e897c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e897c-123">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="e897c-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e897c-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e897c-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e897c-125">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="e897c-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e897c-126">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="e897c-126">Header files</span></span>

<span data-ttu-id="e897c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e897c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e897c-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e897c-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e897c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="e897c-129">See also</span></span>



[<span data-ttu-id="e897c-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e897c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e897c-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e897c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e897c-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e897c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e897c-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="e897c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

