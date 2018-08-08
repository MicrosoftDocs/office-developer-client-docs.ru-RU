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
ms.openlocfilehash: b4bab1948bc563b92dafa16922da3b9760cf1a1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810618"
---
# <a name="pidlidtaskstate-canonical-property"></a><span data-ttu-id="b60d1-103">Каноническое свойство PidLidTaskState</span><span class="sxs-lookup"><span data-stu-id="b60d1-103">PidLidTaskState Canonical Property</span></span>

  
  
<span data-ttu-id="b60d1-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b60d1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b60d1-105">Указывает состояние назначения задачи.</span><span class="sxs-lookup"><span data-stu-id="b60d1-105">Indicates the current assignment state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b60d1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b60d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b60d1-107">dispidTaskState</span><span class="sxs-lookup"><span data-stu-id="b60d1-107">dispidTaskState</span></span>  <br/> |
|<span data-ttu-id="b60d1-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b60d1-108">Property set:</span></span>  <br/> |<span data-ttu-id="b60d1-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b60d1-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b60d1-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="b60d1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b60d1-111">0x00008113</span><span class="sxs-lookup"><span data-stu-id="b60d1-111">0x00008113</span></span>  <br/> |
|<span data-ttu-id="b60d1-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b60d1-112">Data type:</span></span>  <br/> |<span data-ttu-id="b60d1-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b60d1-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b60d1-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b60d1-114">Area:</span></span>  <br/> |<span data-ttu-id="b60d1-115">Task</span><span class="sxs-lookup"><span data-stu-id="b60d1-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b60d1-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="b60d1-116">Remarks</span></span>

<span data-ttu-id="b60d1-117">Значение этого свойства должно быть одно из следующих.</span><span class="sxs-lookup"><span data-stu-id="b60d1-117">The value of this property must be one of the following.</span></span>
  
|<span data-ttu-id="b60d1-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b60d1-118">**Value**</span></span>|<span data-ttu-id="b60d1-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b60d1-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b60d1-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b60d1-120">0x00000000</span></span>  <br/> |<span data-ttu-id="b60d1-121">Эта задача была создана в соответствии с задача, которая была встроена в Отклонение задачи, но не удалось найти локально.</span><span class="sxs-lookup"><span data-stu-id="b60d1-121">This task was created to correspond to a task that was embedded in a task rejection but could not be found locally.</span></span>  <br/> |
|<span data-ttu-id="b60d1-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b60d1-122">0x00000001</span></span>  <br/> |<span data-ttu-id="b60d1-123">Не назначена задача.</span><span class="sxs-lookup"><span data-stu-id="b60d1-123">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="b60d1-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b60d1-124">0x00000002</span></span>  <br/> |<span data-ttu-id="b60d1-125">Задача — назначена задача копия назначенной задачи.</span><span class="sxs-lookup"><span data-stu-id="b60d1-125">The task is the task assignee's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="b60d1-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b60d1-126">0x00000003</span></span>  <br/> |<span data-ttu-id="b60d1-127">Задача — назначено задач копия назначенной задачи.</span><span class="sxs-lookup"><span data-stu-id="b60d1-127">The task is the task assigner's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="b60d1-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b60d1-128">0x00000004</span></span>  <br/> |<span data-ttu-id="b60d1-129">Задача является назначено задач копию Отклоненные задачи.</span><span class="sxs-lookup"><span data-stu-id="b60d1-129">The task is the task assigner's copy of a rejected task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b60d1-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b60d1-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b60d1-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b60d1-131">Protocol specifications</span></span>

<span data-ttu-id="b60d1-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b60d1-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b60d1-133">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b60d1-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b60d1-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b60d1-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b60d1-135">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="b60d1-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="b60d1-136">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b60d1-136">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b60d1-137">Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="b60d1-137">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="b60d1-138">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b60d1-138">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b60d1-139">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="b60d1-139">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="b60d1-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b60d1-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b60d1-141">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="b60d1-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b60d1-142">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b60d1-142">Header files</span></span>

<span data-ttu-id="b60d1-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b60d1-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="b60d1-144">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b60d1-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b60d1-145">См. также</span><span class="sxs-lookup"><span data-stu-id="b60d1-145">See also</span></span>



[<span data-ttu-id="b60d1-146">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b60d1-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b60d1-147">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b60d1-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b60d1-148">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b60d1-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b60d1-149">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b60d1-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

