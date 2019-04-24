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
ms.openlocfilehash: b42be4b42d085aba8999a8c3f1a780ed972fa136
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331292"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a><span data-ttu-id="a8c1b-103">Каноническое свойство PidLidTaskAcceptanceState</span><span class="sxs-lookup"><span data-stu-id="a8c1b-103">PidLidTaskAcceptanceState Canonical Property</span></span>

  
  
<span data-ttu-id="a8c1b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8c1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8c1b-105">Указывает состояние принятия задачи.</span><span class="sxs-lookup"><span data-stu-id="a8c1b-105">Indicates the acceptance state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8c1b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a8c1b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a8c1b-107">Диспидтаскделегвалуе</span><span class="sxs-lookup"><span data-stu-id="a8c1b-107">dispidTaskDelegValue</span></span>  <br/> |
|<span data-ttu-id="a8c1b-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="a8c1b-108">Property set:</span></span>  <br/> |<span data-ttu-id="a8c1b-109">Псетид_таск</span><span class="sxs-lookup"><span data-stu-id="a8c1b-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="a8c1b-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="a8c1b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a8c1b-111">0x0000812A</span><span class="sxs-lookup"><span data-stu-id="a8c1b-111">0x0000812A</span></span>  <br/> |
|<span data-ttu-id="a8c1b-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a8c1b-112">Data type:</span></span>  <br/> |<span data-ttu-id="a8c1b-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a8c1b-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a8c1b-114">Область:</span><span class="sxs-lookup"><span data-stu-id="a8c1b-114">Area:</span></span>  <br/> |<span data-ttu-id="a8c1b-115">Задача</span><span class="sxs-lookup"><span data-stu-id="a8c1b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8c1b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8c1b-116">Remarks</span></span>

<span data-ttu-id="a8c1b-117">В следующей таблице приведены возможные значения для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="a8c1b-117">The following table shows the possible values for this property.</span></span>
  
|<span data-ttu-id="a8c1b-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="a8c1b-118">**Value**</span></span>|<span data-ttu-id="a8c1b-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a8c1b-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8c1b-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8c1b-120">0x00000000</span></span>  <br/> |<span data-ttu-id="a8c1b-121">Задача не назначена.</span><span class="sxs-lookup"><span data-stu-id="a8c1b-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="a8c1b-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a8c1b-122">0x00000001</span></span>  <br/> |<span data-ttu-id="a8c1b-123">Состояние принятия задачи неизвестно.</span><span class="sxs-lookup"><span data-stu-id="a8c1b-123">The task's acceptance status is unknown.</span></span>  <br/> |
|<span data-ttu-id="a8c1b-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a8c1b-124">0x00000002</span></span>  <br/> |<span data-ttu-id="a8c1b-125">Уполномоченная задача приняла задачу.</span><span class="sxs-lookup"><span data-stu-id="a8c1b-125">The task assignee accepted the task.</span></span> <span data-ttu-id="a8c1b-126">Это значение задается, когда клиент обрабатывает принятие задачи.</span><span class="sxs-lookup"><span data-stu-id="a8c1b-126">This value is set when the client processes a task acceptance.</span></span>  <br/> |
|<span data-ttu-id="a8c1b-127">0x00000003</span><span class="sxs-lookup"><span data-stu-id="a8c1b-127">0x00000003</span></span>  <br/> |<span data-ttu-id="a8c1b-128">Поручение отклонило задачу.</span><span class="sxs-lookup"><span data-stu-id="a8c1b-128">The task assignee rejected the task.</span></span> <span data-ttu-id="a8c1b-129">Это значение задается, когда клиент обрабатывает отклонение задачи.</span><span class="sxs-lookup"><span data-stu-id="a8c1b-129">This value is set when the client processes a task rejection.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a8c1b-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a8c1b-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a8c1b-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a8c1b-131">Protocol specifications</span></span>

<span data-ttu-id="a8c1b-132">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8c1b-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8c1b-133">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a8c1b-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a8c1b-134">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8c1b-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8c1b-135">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="a8c1b-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a8c1b-136">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="a8c1b-136">Header files</span></span>

<span data-ttu-id="a8c1b-137">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="a8c1b-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="a8c1b-138">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a8c1b-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8c1b-139">См. также</span><span class="sxs-lookup"><span data-stu-id="a8c1b-139">See also</span></span>



[<span data-ttu-id="a8c1b-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a8c1b-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a8c1b-141">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="a8c1b-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a8c1b-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a8c1b-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a8c1b-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a8c1b-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

