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
ms.openlocfilehash: bc8e4dfe934d516c07d5532ba6a95e51a3cbf962
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578082"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="ed435-103">Каноническое свойство PidLidTaskMode</span><span class="sxs-lookup"><span data-stu-id="ed435-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="ed435-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed435-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed435-105">Указывает состояние назначения задачи.</span><span class="sxs-lookup"><span data-stu-id="ed435-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed435-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ed435-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed435-107">dispidTaskMode</span><span class="sxs-lookup"><span data-stu-id="ed435-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="ed435-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="ed435-108">Property set:</span></span>  <br/> |<span data-ttu-id="ed435-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ed435-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ed435-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="ed435-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ed435-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="ed435-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="ed435-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ed435-112">Data type:</span></span>  <br/> |<span data-ttu-id="ed435-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ed435-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ed435-114">Область:</span><span class="sxs-lookup"><span data-stu-id="ed435-114">Area:</span></span>  <br/> |<span data-ttu-id="ed435-115">Task</span><span class="sxs-lookup"><span data-stu-id="ed435-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed435-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="ed435-116">Remarks</span></span>

<span data-ttu-id="ed435-117">Значение должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ed435-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="ed435-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ed435-118">**Value**</span></span>|<span data-ttu-id="ed435-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ed435-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ed435-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed435-120">0x00000000</span></span>  <br/> |<span data-ttu-id="ed435-121">Не назначена задача.</span><span class="sxs-lookup"><span data-stu-id="ed435-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="ed435-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ed435-122">0x00000001</span></span>  <br/> |<span data-ttu-id="ed435-123">Задачи встраивается в запроса на задачу.</span><span class="sxs-lookup"><span data-stu-id="ed435-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="ed435-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ed435-124">0x00000002</span></span>  <br/> |<span data-ttu-id="ed435-125">Задачи принят назначена задача.</span><span class="sxs-lookup"><span data-stu-id="ed435-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="ed435-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="ed435-126">0x00000003</span></span>  <br/> |<span data-ttu-id="ed435-127">Задачи было отклонено сервером назначена задача.</span><span class="sxs-lookup"><span data-stu-id="ed435-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="ed435-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ed435-128">0x00000004</span></span>  <br/> |<span data-ttu-id="ed435-129">Задачи встраивается в обновления задач.</span><span class="sxs-lookup"><span data-stu-id="ed435-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="ed435-130">0x00000005</span><span class="sxs-lookup"><span data-stu-id="ed435-130">0x00000005</span></span>  <br/> |<span data-ttu-id="ed435-131">Задача назначена задача назначено.</span><span class="sxs-lookup"><span data-stu-id="ed435-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ed435-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ed435-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ed435-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ed435-133">Protocol specifications</span></span>

<span data-ttu-id="ed435-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed435-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed435-135">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ed435-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ed435-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed435-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed435-137">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="ed435-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed435-138">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ed435-138">Header files</span></span>

<span data-ttu-id="ed435-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed435-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed435-140">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ed435-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed435-141">См. также</span><span class="sxs-lookup"><span data-stu-id="ed435-141">See also</span></span>



[<span data-ttu-id="ed435-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ed435-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed435-143">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ed435-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed435-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ed435-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed435-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ed435-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

