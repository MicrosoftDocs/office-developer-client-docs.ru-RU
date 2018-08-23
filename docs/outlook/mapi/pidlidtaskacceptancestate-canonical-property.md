---
title: Каноническое свойство PidLidTaskAcceptanceState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAcceptanceState
api_type:
- COM
ms.assetid: 7012f524-bc66-48ea-85b5-163e05029d35
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b4124a319f378ff2c60de7a1fddaa549aeb08a05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583332"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a><span data-ttu-id="0e4de-103">Каноническое свойство PidLidTaskAcceptanceState</span><span class="sxs-lookup"><span data-stu-id="0e4de-103">PidLidTaskAcceptanceState Canonical Property</span></span>

  
  
<span data-ttu-id="0e4de-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e4de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e4de-105">Указывает состояние приемки задачи.</span><span class="sxs-lookup"><span data-stu-id="0e4de-105">Indicates the acceptance state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e4de-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0e4de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e4de-107">dispidTaskDelegValue</span><span class="sxs-lookup"><span data-stu-id="0e4de-107">dispidTaskDelegValue</span></span>  <br/> |
|<span data-ttu-id="0e4de-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="0e4de-108">Property set:</span></span>  <br/> |<span data-ttu-id="0e4de-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0e4de-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0e4de-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="0e4de-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0e4de-111">0x0000812A</span><span class="sxs-lookup"><span data-stu-id="0e4de-111">0x0000812A</span></span>  <br/> |
|<span data-ttu-id="0e4de-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0e4de-112">Data type:</span></span>  <br/> |<span data-ttu-id="0e4de-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0e4de-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0e4de-114">Область:</span><span class="sxs-lookup"><span data-stu-id="0e4de-114">Area:</span></span>  <br/> |<span data-ttu-id="0e4de-115">Task</span><span class="sxs-lookup"><span data-stu-id="0e4de-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e4de-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="0e4de-116">Remarks</span></span>

<span data-ttu-id="0e4de-117">В следующей таблице представлены возможные значения для данного свойства.</span><span class="sxs-lookup"><span data-stu-id="0e4de-117">The following table shows the possible values for this property.</span></span>
  
|<span data-ttu-id="0e4de-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0e4de-118">**Value**</span></span>|<span data-ttu-id="0e4de-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0e4de-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0e4de-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e4de-120">0x00000000</span></span>  <br/> |<span data-ttu-id="0e4de-121">Не назначена задача.</span><span class="sxs-lookup"><span data-stu-id="0e4de-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="0e4de-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0e4de-122">0x00000001</span></span>  <br/> |<span data-ttu-id="0e4de-123">Состояние задачи приемки не известен.</span><span class="sxs-lookup"><span data-stu-id="0e4de-123">The task's acceptance status is unknown.</span></span>  <br/> |
|<span data-ttu-id="0e4de-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0e4de-124">0x00000002</span></span>  <br/> |<span data-ttu-id="0e4de-125">Назначена задача принятия задачи.</span><span class="sxs-lookup"><span data-stu-id="0e4de-125">The task assignee accepted the task.</span></span> <span data-ttu-id="0e4de-126">Это значение при клиент обрабатывает Принятие задачи.</span><span class="sxs-lookup"><span data-stu-id="0e4de-126">This value is set when the client processes a task acceptance.</span></span>  <br/> |
|<span data-ttu-id="0e4de-127">0x00000003</span><span class="sxs-lookup"><span data-stu-id="0e4de-127">0x00000003</span></span>  <br/> |<span data-ttu-id="0e4de-128">Назначена задача отклоненной задачи.</span><span class="sxs-lookup"><span data-stu-id="0e4de-128">The task assignee rejected the task.</span></span> <span data-ttu-id="0e4de-129">Это значение при клиент обрабатывает Отклонение задачи.</span><span class="sxs-lookup"><span data-stu-id="0e4de-129">This value is set when the client processes a task rejection.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0e4de-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0e4de-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e4de-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0e4de-131">Protocol specifications</span></span>

<span data-ttu-id="0e4de-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e4de-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e4de-133">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0e4de-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e4de-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e4de-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e4de-135">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="0e4de-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e4de-136">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0e4de-136">Header files</span></span>

<span data-ttu-id="0e4de-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e4de-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e4de-138">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0e4de-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e4de-139">См. также</span><span class="sxs-lookup"><span data-stu-id="0e4de-139">See also</span></span>



[<span data-ttu-id="0e4de-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0e4de-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e4de-141">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0e4de-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e4de-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0e4de-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e4de-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0e4de-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

