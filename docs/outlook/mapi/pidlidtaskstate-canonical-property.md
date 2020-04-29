---
title: Каноническое свойство PidLidTaskState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskState
api_type:
- COM
ms.assetid: 06d1f8a3-53e1-4c9a-9703-75de7a11a772
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 149f238ea53e0669f4d95c8e6c2b17a2b5a1c209
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316537"
---
# <a name="pidlidtaskstate-canonical-property"></a><span data-ttu-id="1010d-103">Каноническое свойство PidLidTaskState</span><span class="sxs-lookup"><span data-stu-id="1010d-103">PidLidTaskState Canonical Property</span></span>

  
  
<span data-ttu-id="1010d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1010d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1010d-105">Указывает текущее состояние назначения задачи.</span><span class="sxs-lookup"><span data-stu-id="1010d-105">Indicates the current assignment state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1010d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1010d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1010d-107">диспидтаскстате</span><span class="sxs-lookup"><span data-stu-id="1010d-107">dispidTaskState</span></span>  <br/> |
|<span data-ttu-id="1010d-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="1010d-108">Property set:</span></span>  <br/> |<span data-ttu-id="1010d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="1010d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="1010d-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="1010d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1010d-111">0x00008113</span><span class="sxs-lookup"><span data-stu-id="1010d-111">0x00008113</span></span>  <br/> |
|<span data-ttu-id="1010d-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1010d-112">Data type:</span></span>  <br/> |<span data-ttu-id="1010d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1010d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1010d-114">Область:</span><span class="sxs-lookup"><span data-stu-id="1010d-114">Area:</span></span>  <br/> |<span data-ttu-id="1010d-115">Задача</span><span class="sxs-lookup"><span data-stu-id="1010d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1010d-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="1010d-116">Remarks</span></span>

<span data-ttu-id="1010d-117">Значение этого свойства должно быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="1010d-117">The value of this property must be one of the following.</span></span>
  
|<span data-ttu-id="1010d-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="1010d-118">**Value**</span></span>|<span data-ttu-id="1010d-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1010d-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1010d-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1010d-120">0x00000000</span></span>  <br/> |<span data-ttu-id="1010d-121">Эта задача была создана в соответствии с задачей, которая была внедрена в отклонение задачи и не может быть найдена локально.</span><span class="sxs-lookup"><span data-stu-id="1010d-121">This task was created to correspond to a task that was embedded in a task rejection but could not be found locally.</span></span>  <br/> |
|<span data-ttu-id="1010d-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1010d-122">0x00000001</span></span>  <br/> |<span data-ttu-id="1010d-123">Задача не назначена.</span><span class="sxs-lookup"><span data-stu-id="1010d-123">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="1010d-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1010d-124">0x00000002</span></span>  <br/> |<span data-ttu-id="1010d-125">Задача является копией назначенной задачи, назначенной ей.</span><span class="sxs-lookup"><span data-stu-id="1010d-125">The task is the task assignee's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="1010d-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="1010d-126">0x00000003</span></span>  <br/> |<span data-ttu-id="1010d-127">Задача — это копия назначенной задачи, назначенная задаче.</span><span class="sxs-lookup"><span data-stu-id="1010d-127">The task is the task assigner's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="1010d-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="1010d-128">0x00000004</span></span>  <br/> |<span data-ttu-id="1010d-129">Задача — это копия отклонения задачи, назначенная ей.</span><span class="sxs-lookup"><span data-stu-id="1010d-129">The task is the task assigner's copy of a rejected task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1010d-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1010d-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1010d-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1010d-131">Protocol specifications</span></span>

<span data-ttu-id="1010d-132">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1010d-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1010d-133">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1010d-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1010d-134">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1010d-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1010d-135">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="1010d-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="1010d-136">[[MS — ОКСОСФЛД]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1010d-136">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1010d-137">Задает свойства и операции для создания и поиска специальных папок в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="1010d-137">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="1010d-138">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1010d-138">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1010d-139">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="1010d-139">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="1010d-140">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1010d-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1010d-141">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="1010d-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1010d-142">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1010d-142">Header files</span></span>

<span data-ttu-id="1010d-143">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="1010d-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="1010d-144">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1010d-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1010d-145">См. также</span><span class="sxs-lookup"><span data-stu-id="1010d-145">See also</span></span>



[<span data-ttu-id="1010d-146">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1010d-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1010d-147">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="1010d-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1010d-148">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1010d-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1010d-149">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1010d-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

