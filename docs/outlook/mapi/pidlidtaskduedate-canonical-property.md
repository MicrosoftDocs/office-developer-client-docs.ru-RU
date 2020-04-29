---
title: Каноническое свойство PidLidTaskDueDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDueDate
api_type:
- COM
ms.assetid: 69ed3d48-3741-4a9a-8f98-51382b850c27
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2e21d164cbb9403d3fa1dc05cf474359a517d64b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303327"
---
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="68beb-103">Каноническое свойство PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="68beb-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="68beb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68beb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68beb-105">Представляет дату, когда пользователь ожидает завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="68beb-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68beb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="68beb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="68beb-107">диспидтаскдуедате</span><span class="sxs-lookup"><span data-stu-id="68beb-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="68beb-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="68beb-108">Property set:</span></span>  <br/> |<span data-ttu-id="68beb-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="68beb-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="68beb-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="68beb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="68beb-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="68beb-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="68beb-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="68beb-112">Data type:</span></span>  <br/> |<span data-ttu-id="68beb-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="68beb-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="68beb-114">Область:</span><span class="sxs-lookup"><span data-stu-id="68beb-114">Area:</span></span>  <br/> |<span data-ttu-id="68beb-115">Задача</span><span class="sxs-lookup"><span data-stu-id="68beb-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68beb-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="68beb-116">Remarks</span></span>

<span data-ttu-id="68beb-117">У задачи нет даты завершения, если это свойство не задано или установлено значение 0x5AE980E0 (1 525 252 320).</span><span class="sxs-lookup"><span data-stu-id="68beb-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="68beb-118">Однако Дата выполнения является необязательной, только если в свойстве **диспидтаскстартдате** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) не указана дата начала.</span><span class="sxs-lookup"><span data-stu-id="68beb-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="68beb-119">Если у задачи есть Дата выполнения, то значение должно быть компонентом времени полуночи, а также должно быть задано свойство **диспидкоммоненд** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="68beb-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="68beb-120">Если **диспидтаскстартдате** имеет дату начала, то значение свойства **диспидтаскдуедате** должно быть больше или равно значению **диспидтаскстартдате**.</span><span class="sxs-lookup"><span data-stu-id="68beb-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="68beb-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="68beb-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="68beb-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="68beb-122">Protocol specifications</span></span>

<span data-ttu-id="68beb-123">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68beb-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68beb-124">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="68beb-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="68beb-125">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68beb-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68beb-126">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="68beb-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="68beb-127">[[MS — ОКСОРМДР]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68beb-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68beb-128">Задает свойства и модель взаимодействия для сообщений электронной почты и других объектов.</span><span class="sxs-lookup"><span data-stu-id="68beb-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="68beb-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="68beb-129">Header files</span></span>

<span data-ttu-id="68beb-130">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="68beb-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="68beb-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="68beb-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68beb-132">См. также</span><span class="sxs-lookup"><span data-stu-id="68beb-132">See also</span></span>



[<span data-ttu-id="68beb-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="68beb-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="68beb-134">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="68beb-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="68beb-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="68beb-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="68beb-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="68beb-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

