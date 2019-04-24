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
ms.openlocfilehash: 9a438fb2b1862d44905a63fda3e5f68b7878cd99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316620"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a><span data-ttu-id="47c96-103">Каноническое свойство PidLidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="47c96-103">PidLidTaskResetReminder Canonical Property</span></span>

  
  
<span data-ttu-id="47c96-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47c96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47c96-105">Указывает, требуются ли напоминания будущим экземплярам повторяющихся задач, даже если **диспидреминдерсет** ([PIDLIDREMINDERSET](pidlidreminderset-canonical-property.md)) имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="47c96-105">Indicates whether future instances of recurring tasks need reminders, even though **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) is FALSE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47c96-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="47c96-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47c96-107">Диспидтаскресетреминдер</span><span class="sxs-lookup"><span data-stu-id="47c96-107">dispidTaskResetReminder</span></span>  <br/> |
|<span data-ttu-id="47c96-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="47c96-108">Property set:</span></span>  <br/> |<span data-ttu-id="47c96-109">Псетид_таск</span><span class="sxs-lookup"><span data-stu-id="47c96-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="47c96-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="47c96-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="47c96-111">0x00008107</span><span class="sxs-lookup"><span data-stu-id="47c96-111">0x00008107</span></span>  <br/> |
|<span data-ttu-id="47c96-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="47c96-112">Data type:</span></span>  <br/> |<span data-ttu-id="47c96-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="47c96-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="47c96-114">Область:</span><span class="sxs-lookup"><span data-stu-id="47c96-114">Area:</span></span>  <br/> |<span data-ttu-id="47c96-115">Задача</span><span class="sxs-lookup"><span data-stu-id="47c96-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47c96-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="47c96-116">Remarks</span></span>

<span data-ttu-id="47c96-117">Это значение задается равным TRUE при закрытии напоминания задачи и имеет значение FALSE в противном случае.</span><span class="sxs-lookup"><span data-stu-id="47c96-117">This value is set to TRUE when the task's reminder is dismissed, and set to FALSE otherwise.</span></span> <span data-ttu-id="47c96-118">Если не оставить, то предполагается значение FALSE по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47c96-118">If left unset, a default of FALSE is assumed.</span></span>
  
<span data-ttu-id="47c96-119">Как указано в [[MS-оксормдр]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), свойство **диспидреминдерсет** указывает, задано ли для задачи напоминание.</span><span class="sxs-lookup"><span data-stu-id="47c96-119">As specified in [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), the **dispidReminderSet** property indicates whether a reminder is set on the task.</span></span> <span data-ttu-id="47c96-120">Однако это свойство указывает только на присутствие напоминания для одной задачи.</span><span class="sxs-lookup"><span data-stu-id="47c96-120">However, this property only indicates the presence of a reminder on a single task.</span></span> <span data-ttu-id="47c96-121">Он не может использоваться отдельно для определения необходимости напоминания будущему экземпляру повторяющейся задачи.</span><span class="sxs-lookup"><span data-stu-id="47c96-121">It cannot be used alone to determine whether a future instance of a recurring task needs a reminder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="47c96-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="47c96-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47c96-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="47c96-123">Protocol specifications</span></span>

<span data-ttu-id="47c96-124">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47c96-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47c96-125">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="47c96-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="47c96-126">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47c96-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47c96-127">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="47c96-127">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="47c96-128">[[MS — ОКСОРМДР]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47c96-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47c96-129">Задает свойства и модель взаимодействия для сообщений электронной почты и других объектов.</span><span class="sxs-lookup"><span data-stu-id="47c96-129">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47c96-130">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="47c96-130">Header files</span></span>

<span data-ttu-id="47c96-131">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="47c96-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="47c96-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="47c96-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47c96-133">См. также</span><span class="sxs-lookup"><span data-stu-id="47c96-133">See also</span></span>



[<span data-ttu-id="47c96-134">������������ �������� PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="47c96-134">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)


[<span data-ttu-id="47c96-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="47c96-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47c96-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="47c96-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47c96-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="47c96-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47c96-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="47c96-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

