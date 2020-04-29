---
title: Каноническое свойство PidLidTaskStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStatus
api_type:
- COM
ms.assetid: 809776b7-ff00-4a52-84b9-8b5fb5f5c3e3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d058b42ad7d1a1b8387aa5b9a1a65ea160d90b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316669"
---
# <a name="pidlidtaskstatus-canonical-property"></a><span data-ttu-id="b8a59-103">Каноническое свойство PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="b8a59-103">PidLidTaskStatus Canonical Property</span></span>

  
  
<span data-ttu-id="b8a59-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8a59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8a59-105">Указывает состояние хода выполнения действия пользователя для задачи.</span><span class="sxs-lookup"><span data-stu-id="b8a59-105">Specifies the status of the user's progress on the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b8a59-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b8a59-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b8a59-107">диспидтаскстатус</span><span class="sxs-lookup"><span data-stu-id="b8a59-107">dispidTaskStatus</span></span>  <br/> |
|<span data-ttu-id="b8a59-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b8a59-108">Property set:</span></span>  <br/> |<span data-ttu-id="b8a59-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b8a59-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b8a59-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="b8a59-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b8a59-111">0x00008101</span><span class="sxs-lookup"><span data-stu-id="b8a59-111">0x00008101</span></span>  <br/> |
|<span data-ttu-id="b8a59-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b8a59-112">Data type:</span></span>  <br/> |<span data-ttu-id="b8a59-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b8a59-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b8a59-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b8a59-114">Area:</span></span>  <br/> |<span data-ttu-id="b8a59-115">Задача</span><span class="sxs-lookup"><span data-stu-id="b8a59-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8a59-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b8a59-116">Remarks</span></span>

<span data-ttu-id="b8a59-117">Значение этого свойства должно быть равно одному из следующих элементов.</span><span class="sxs-lookup"><span data-stu-id="b8a59-117">The value of this property must be set to one of the following.</span></span>
  
|<span data-ttu-id="b8a59-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b8a59-118">**Value**</span></span>|<span data-ttu-id="b8a59-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b8a59-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b8a59-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8a59-120">0x00000000</span></span>  <br/> |<span data-ttu-id="b8a59-121">Пользователь не начал работу над задачей.</span><span class="sxs-lookup"><span data-stu-id="b8a59-121">The user has not started work on the task.</span></span> <span data-ttu-id="b8a59-122">Если задано это значение, **диспидперценткомплете** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) должно быть 0,0.</span><span class="sxs-lookup"><span data-stu-id="b8a59-122">If this value is set, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) must be 0.0.</span></span>  <br/> |
|<span data-ttu-id="b8a59-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b8a59-123">0x00000001</span></span>  <br/> |<span data-ttu-id="b8a59-124">Выполняются действия пользователя в этой задаче.</span><span class="sxs-lookup"><span data-stu-id="b8a59-124">The user's work on this task is in progress.</span></span> <span data-ttu-id="b8a59-125">Если задано это значение, **диспидперценткомплете** должно быть больше 0,0 и меньше 1,0.</span><span class="sxs-lookup"><span data-stu-id="b8a59-125">If this value is set, **dispidPercentComplete** must be greater than 0.0 and less than 1.0.</span></span>  <br/> |
|<span data-ttu-id="b8a59-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b8a59-126">0x00000002</span></span>  <br/> |<span data-ttu-id="b8a59-127">Трудозатраты пользователя по этой задаче завершены.</span><span class="sxs-lookup"><span data-stu-id="b8a59-127">The user's work on this task is complete.</span></span> <span data-ttu-id="b8a59-128">Если задано это значение, значение **диспидперценткомплете** должно быть 1,0 **, диспидтаскдатекомплетед** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) — текущей датой, а **диспидтасккомплете** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) — true.</span><span class="sxs-lookup"><span data-stu-id="b8a59-128">If this value is set, **dispidPercentComplete** must be 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) must be the current date, and **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) must be TRUE.</span></span>  <br/> |
|<span data-ttu-id="b8a59-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b8a59-129">0x00000003</span></span>  <br/> |<span data-ttu-id="b8a59-130">Пользователь ожидает кого-либо.</span><span class="sxs-lookup"><span data-stu-id="b8a59-130">The user is waiting on somebody else.</span></span>  <br/> |
|<span data-ttu-id="b8a59-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b8a59-131">0x00000004</span></span>  <br/> |<span data-ttu-id="b8a59-132">Пользователь отложил работу по задаче.</span><span class="sxs-lookup"><span data-stu-id="b8a59-132">The user has deferred work on the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b8a59-133">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b8a59-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b8a59-134">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b8a59-134">Protocol specifications</span></span>

<span data-ttu-id="b8a59-135">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8a59-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8a59-136">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b8a59-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b8a59-137">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8a59-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8a59-138">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="b8a59-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="b8a59-139">[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8a59-139">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8a59-140">Задает свойства и операции, связанные с пометкой.</span><span class="sxs-lookup"><span data-stu-id="b8a59-140">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="b8a59-141">[[MS — ОКСОСФЛД]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8a59-141">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8a59-142">Задает свойства и операции для создания и поиска специальных папок в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="b8a59-142">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="b8a59-143">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8a59-143">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8a59-144">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="b8a59-144">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="b8a59-145">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8a59-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8a59-146">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="b8a59-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="b8a59-147">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8a59-147">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8a59-148">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="b8a59-148">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b8a59-149">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b8a59-149">Header files</span></span>

<span data-ttu-id="b8a59-150">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b8a59-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="b8a59-151">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b8a59-151">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b8a59-152">См. также</span><span class="sxs-lookup"><span data-stu-id="b8a59-152">See also</span></span>



[<span data-ttu-id="b8a59-153">Каноническое свойство PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="b8a59-153">PidLidPercentComplete Canonical Property</span></span>](pidlidpercentcomplete-canonical-property.md)
  
[<span data-ttu-id="b8a59-154">Каноническое свойство PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="b8a59-154">PidLidTaskDateCompleted Canonical Property</span></span>](pidlidtaskdatecompleted-canonical-property.md)
  
[<span data-ttu-id="b8a59-155">Каноническое свойство PidLidTaskComplete</span><span class="sxs-lookup"><span data-stu-id="b8a59-155">PidLidTaskComplete Canonical Property</span></span>](pidlidtaskcomplete-canonical-property.md)


[<span data-ttu-id="b8a59-156">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b8a59-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b8a59-157">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b8a59-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b8a59-158">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b8a59-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b8a59-159">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b8a59-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

