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
ms.openlocfilehash: b4c497e77b9dfcea13742535148180275495717d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581869"
---
# <a name="pidlidtaskassigner-canonical-property"></a><span data-ttu-id="687ac-103">Каноническое свойство PidLidTaskAssigner</span><span class="sxs-lookup"><span data-stu-id="687ac-103">PidLidTaskAssigner Canonical Property</span></span>

  
  
<span data-ttu-id="687ac-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="687ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="687ac-105">Имена пользователя, Дата и время последнего назначена задача.</span><span class="sxs-lookup"><span data-stu-id="687ac-105">Names the user who was last assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="687ac-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="687ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="687ac-107">dispidTaskDelegator</span><span class="sxs-lookup"><span data-stu-id="687ac-107">dispidTaskDelegator</span></span>  <br/> |
|<span data-ttu-id="687ac-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="687ac-108">Property set:</span></span>  <br/> |<span data-ttu-id="687ac-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="687ac-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="687ac-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="687ac-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="687ac-111">0x00008121</span><span class="sxs-lookup"><span data-stu-id="687ac-111">0x00008121</span></span>  <br/> |
|<span data-ttu-id="687ac-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="687ac-112">Data type:</span></span>  <br/> |<span data-ttu-id="687ac-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="687ac-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="687ac-114">Область:</span><span class="sxs-lookup"><span data-stu-id="687ac-114">Area:</span></span>  <br/> |<span data-ttu-id="687ac-115">Task</span><span class="sxs-lookup"><span data-stu-id="687ac-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="687ac-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="687ac-116">Remarks</span></span>

<span data-ttu-id="687ac-117">Если не была назначена задача, оставить это свойство определено.</span><span class="sxs-lookup"><span data-stu-id="687ac-117">If the task has not been assigned, this property is left unset.</span></span> <span data-ttu-id="687ac-118">Так как этому свойству клиента после назначена задача получает запрос задачи, свойство не будет установлен на копию назначено задач задачи.</span><span class="sxs-lookup"><span data-stu-id="687ac-118">Because the client sets this property after the task assignee receives a task request, the property will not be set on the task assigner's copy of the task.</span></span> <span data-ttu-id="687ac-119">Когда клиент добавляет или удаляет назначено задач из списка задач назначено в свойстве **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)), свойство **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) должно быть присвоено значение добавлены или назначено удаленных задач.</span><span class="sxs-lookup"><span data-stu-id="687ac-119">When the client adds or removes a task assigner from the task assigner list in the **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) property, the **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) property must be set to the added or removed task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="687ac-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="687ac-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="687ac-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="687ac-121">Protocol specifications</span></span>

<span data-ttu-id="687ac-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="687ac-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="687ac-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="687ac-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="687ac-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="687ac-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="687ac-125">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="687ac-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="687ac-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="687ac-126">Header files</span></span>

<span data-ttu-id="687ac-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="687ac-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="687ac-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="687ac-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="687ac-129">См. также</span><span class="sxs-lookup"><span data-stu-id="687ac-129">See also</span></span>



[<span data-ttu-id="687ac-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="687ac-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="687ac-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="687ac-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="687ac-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="687ac-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="687ac-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="687ac-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

