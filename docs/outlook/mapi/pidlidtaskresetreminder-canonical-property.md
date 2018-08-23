---
title: Каноническое свойство PidLidTaskResetReminder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskResetReminder
api_type:
- COM
ms.assetid: f6da69ff-a913-4a65-bb07-8ad3c5685e5e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e16c1b46b5a8181b1225c706dbed6cd1bb3f486f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583178"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a><span data-ttu-id="fe0d9-103">Каноническое свойство PidLidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="fe0d9-103">PidLidTaskResetReminder Canonical Property</span></span>

  
  
<span data-ttu-id="fe0d9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe0d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe0d9-105">Указывает, необходимости будущих экземпляры повторяющейся задачи напоминаний, несмотря на то, что **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-105">Indicates whether future instances of recurring tasks need reminders, even though **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) is FALSE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe0d9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fe0d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe0d9-107">dispidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="fe0d9-107">dispidTaskResetReminder</span></span>  <br/> |
|<span data-ttu-id="fe0d9-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="fe0d9-108">Property set:</span></span>  <br/> |<span data-ttu-id="fe0d9-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="fe0d9-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="fe0d9-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="fe0d9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fe0d9-111">0x00008107</span><span class="sxs-lookup"><span data-stu-id="fe0d9-111">0x00008107</span></span>  <br/> |
|<span data-ttu-id="fe0d9-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="fe0d9-112">Data type:</span></span>  <br/> |<span data-ttu-id="fe0d9-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fe0d9-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fe0d9-114">Область:</span><span class="sxs-lookup"><span data-stu-id="fe0d9-114">Area:</span></span>  <br/> |<span data-ttu-id="fe0d9-115">Task</span><span class="sxs-lookup"><span data-stu-id="fe0d9-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe0d9-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="fe0d9-116">Remarks</span></span>

<span data-ttu-id="fe0d9-117">Это значение имеет значение TRUE, если закрытия напоминания о задаче, а в противном случае — значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-117">This value is set to TRUE when the task's reminder is dismissed, and set to FALSE otherwise.</span></span> <span data-ttu-id="fe0d9-118">Если ничего не определено, предполагается значение по умолчанию FALSE.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-118">If left unset, a default of FALSE is assumed.</span></span>
  
<span data-ttu-id="fe0d9-119">Как указано в [[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)свойство **dispidReminderSet** указывает, установил ли напоминания для задачи.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-119">As specified in [[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), the **dispidReminderSet** property indicates whether a reminder is set on the task.</span></span> <span data-ttu-id="fe0d9-120">Тем не менее это свойство показывает только присутствия напоминание на одну задачу.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-120">However, this property only indicates the presence of a reminder on a single task.</span></span> <span data-ttu-id="fe0d9-121">Он не может использоваться отдельно, чтобы определить, должна ли будущих экземпляр повторяющейся задачи напоминание.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-121">It cannot be used alone to determine whether a future instance of a recurring task needs a reminder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fe0d9-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fe0d9-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fe0d9-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="fe0d9-123">Protocol specifications</span></span>

<span data-ttu-id="fe0d9-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe0d9-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe0d9-125">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fe0d9-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe0d9-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe0d9-127">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-127">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="fe0d9-128">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe0d9-128">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe0d9-129">Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-129">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fe0d9-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="fe0d9-130">Header files</span></span>

<span data-ttu-id="fe0d9-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe0d9-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe0d9-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe0d9-133">См. также</span><span class="sxs-lookup"><span data-stu-id="fe0d9-133">See also</span></span>



[<span data-ttu-id="fe0d9-134">������������ �������� PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="fe0d9-134">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)


[<span data-ttu-id="fe0d9-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fe0d9-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe0d9-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fe0d9-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe0d9-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fe0d9-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe0d9-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="fe0d9-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

