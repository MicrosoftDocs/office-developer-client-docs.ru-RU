---
title: Каноническое свойство PidLidTaskDueDueDate
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
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="0acca-103">Каноническое свойство PidLidTaskDueDueDate</span><span class="sxs-lookup"><span data-stu-id="0acca-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="0acca-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0acca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0acca-105">Представляет дату выполнения задачи пользователем.</span><span class="sxs-lookup"><span data-stu-id="0acca-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0acca-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0acca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0acca-107">dispidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="0acca-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="0acca-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="0acca-108">Property set:</span></span>  <br/> |<span data-ttu-id="0acca-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0acca-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0acca-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0acca-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0acca-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="0acca-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="0acca-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0acca-112">Data type:</span></span>  <br/> |<span data-ttu-id="0acca-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="0acca-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="0acca-114">Область:</span><span class="sxs-lookup"><span data-stu-id="0acca-114">Area:</span></span>  <br/> |<span data-ttu-id="0acca-115">Задача</span><span class="sxs-lookup"><span data-stu-id="0acca-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0acca-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="0acca-116">Remarks</span></span>

<span data-ttu-id="0acca-117">Задача не имеет даты, если это свойство не установлено или 0x5AE980E0 (1 525 252 320).</span><span class="sxs-lookup"><span data-stu-id="0acca-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="0acca-118">Однако срок действия является необязательным только в том случае, если дата начала не указана в свойстве **dispidTaskStartDate** [(PidLidTaskStartDate).](pidlidtaskstartdate-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="0acca-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="0acca-119">Если для задачи назначена дата, значение должно иметь компонент времени в полночь, а свойство **dispidCommonEnd** [(PidLidCommonEnd)](pidlidcommonend-canonical-property.md)также должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="0acca-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="0acca-120">Если **у dispidTaskStartDate** есть дата начала, то значение свойства **dispidTaskDueDate** должно быть больше или равно значению **dispidTaskStartDate**.</span><span class="sxs-lookup"><span data-stu-id="0acca-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0acca-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0acca-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0acca-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0acca-122">Protocol specifications</span></span>

<span data-ttu-id="0acca-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0acca-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0acca-124">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="0acca-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0acca-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0acca-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0acca-126">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="0acca-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="0acca-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0acca-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0acca-128">Указывает свойства и модель взаимодействия для электронной почты и других напоминаний объектов.</span><span class="sxs-lookup"><span data-stu-id="0acca-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0acca-129">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="0acca-129">Header files</span></span>

<span data-ttu-id="0acca-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0acca-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="0acca-131">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0acca-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0acca-132">См. также</span><span class="sxs-lookup"><span data-stu-id="0acca-132">See also</span></span>



[<span data-ttu-id="0acca-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0acca-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0acca-134">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0acca-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0acca-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0acca-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0acca-136">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="0acca-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

