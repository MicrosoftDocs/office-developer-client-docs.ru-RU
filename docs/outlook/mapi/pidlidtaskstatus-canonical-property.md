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
# <a name="pidlidtaskstatus-canonical-property"></a><span data-ttu-id="22f66-103">Каноническое свойство PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="22f66-103">PidLidTaskStatus Canonical Property</span></span>

  
  
<span data-ttu-id="22f66-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22f66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22f66-105">Указывает состояние выполнения пользователем задачи.</span><span class="sxs-lookup"><span data-stu-id="22f66-105">Specifies the status of the user's progress on the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22f66-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="22f66-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22f66-107">dispidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="22f66-107">dispidTaskStatus</span></span>  <br/> |
|<span data-ttu-id="22f66-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="22f66-108">Property set:</span></span>  <br/> |<span data-ttu-id="22f66-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="22f66-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="22f66-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="22f66-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="22f66-111">0x00008101</span><span class="sxs-lookup"><span data-stu-id="22f66-111">0x00008101</span></span>  <br/> |
|<span data-ttu-id="22f66-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="22f66-112">Data type:</span></span>  <br/> |<span data-ttu-id="22f66-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="22f66-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="22f66-114">Область:</span><span class="sxs-lookup"><span data-stu-id="22f66-114">Area:</span></span>  <br/> |<span data-ttu-id="22f66-115">Задача</span><span class="sxs-lookup"><span data-stu-id="22f66-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22f66-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="22f66-116">Remarks</span></span>

<span data-ttu-id="22f66-117">Значение этого свойства должно быть установлено в одном из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="22f66-117">The value of this property must be set to one of the following.</span></span>
  
|<span data-ttu-id="22f66-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="22f66-118">**Value**</span></span>|<span data-ttu-id="22f66-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="22f66-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="22f66-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22f66-120">0x00000000</span></span>  <br/> |<span data-ttu-id="22f66-121">Пользователь еще не приступил к работе над задачей.</span><span class="sxs-lookup"><span data-stu-id="22f66-121">The user has not started work on the task.</span></span> <span data-ttu-id="22f66-122">Если это значение установлено, **значение dispidPercentComplete** [(PidLidPercentComplete)](pidlidpercentcomplete-canonical-property.md)должно быть 0,0.</span><span class="sxs-lookup"><span data-stu-id="22f66-122">If this value is set, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) must be 0.0.</span></span>  <br/> |
|<span data-ttu-id="22f66-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="22f66-123">0x00000001</span></span>  <br/> |<span data-ttu-id="22f66-124">Работа пользователя над этой задачей продолжается.</span><span class="sxs-lookup"><span data-stu-id="22f66-124">The user's work on this task is in progress.</span></span> <span data-ttu-id="22f66-125">Если это значение установлено, **значение dispidPercentComplete** должно быть больше 0,0 и менее 1,0.</span><span class="sxs-lookup"><span data-stu-id="22f66-125">If this value is set, **dispidPercentComplete** must be greater than 0.0 and less than 1.0.</span></span>  <br/> |
|<span data-ttu-id="22f66-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="22f66-126">0x00000002</span></span>  <br/> |<span data-ttu-id="22f66-127">Работа пользователя над этой задачей завершена.</span><span class="sxs-lookup"><span data-stu-id="22f66-127">The user's work on this task is complete.</span></span> <span data-ttu-id="22f66-128">Если это значение заданной, **dispidPercentComplete** должно быть 1.0, **dispidTaskDateCompleted** [(PidLidTaskDateCompleted)](pidlidtaskdatecompleted-canonical-property.md)должно быть актуальной датой, а **dispidTaskComplete** [(PidLidTaskComplete)](pidlidtaskcomplete-canonical-property.md)должно быть TRUE.</span><span class="sxs-lookup"><span data-stu-id="22f66-128">If this value is set, **dispidPercentComplete** must be 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) must be the current date, and **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) must be TRUE.</span></span>  <br/> |
|<span data-ttu-id="22f66-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="22f66-129">0x00000003</span></span>  <br/> |<span data-ttu-id="22f66-130">Пользователь ждет другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="22f66-130">The user is waiting on somebody else.</span></span>  <br/> |
|<span data-ttu-id="22f66-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="22f66-131">0x00000004</span></span>  <br/> |<span data-ttu-id="22f66-132">Пользователь отложил работу над задачей.</span><span class="sxs-lookup"><span data-stu-id="22f66-132">The user has deferred work on the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="22f66-133">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="22f66-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="22f66-134">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="22f66-134">Protocol specifications</span></span>

<span data-ttu-id="22f66-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22f66-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22f66-136">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="22f66-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="22f66-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22f66-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22f66-138">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="22f66-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="22f66-139">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22f66-139">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22f66-140">Указывает свойства и операции, связанные с маркировкой.</span><span class="sxs-lookup"><span data-stu-id="22f66-140">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="22f66-141">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22f66-141">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22f66-142">Указывает свойства и операции для создания и размещения специальных папок в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="22f66-142">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="22f66-143">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22f66-143">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22f66-144">Преобразуется из стандартных конвенций электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="22f66-144">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="22f66-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22f66-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22f66-146">Преобразования между объектами IETF RFC2445, RFC2446 и RFC2447, а также объектами назначения и собраний.</span><span class="sxs-lookup"><span data-stu-id="22f66-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="22f66-147">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22f66-147">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22f66-148">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="22f66-148">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="22f66-149">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="22f66-149">Header files</span></span>

<span data-ttu-id="22f66-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22f66-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="22f66-151">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="22f66-151">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22f66-152">См. также</span><span class="sxs-lookup"><span data-stu-id="22f66-152">See also</span></span>



[<span data-ttu-id="22f66-153">Каноническое свойство PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="22f66-153">PidLidPercentComplete Canonical Property</span></span>](pidlidpercentcomplete-canonical-property.md)
  
[<span data-ttu-id="22f66-154">Каноническое свойство PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="22f66-154">PidLidTaskDateCompleted Canonical Property</span></span>](pidlidtaskdatecompleted-canonical-property.md)
  
[<span data-ttu-id="22f66-155">Каноническое свойство PidLidTaskComplete</span><span class="sxs-lookup"><span data-stu-id="22f66-155">PidLidTaskComplete Canonical Property</span></span>](pidlidtaskcomplete-canonical-property.md)


[<span data-ttu-id="22f66-156">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="22f66-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22f66-157">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="22f66-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22f66-158">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="22f66-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22f66-159">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="22f66-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

