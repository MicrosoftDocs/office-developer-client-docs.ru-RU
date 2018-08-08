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
ms.openlocfilehash: d26a686573a9dc178a46b7dfdc5c18485303b7ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810594"
---
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="7e792-103">Каноническое свойство PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="7e792-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="7e792-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7e792-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7e792-105">Представляет дату, когда необходима для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="7e792-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e792-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7e792-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7e792-107">dispidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="7e792-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="7e792-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="7e792-108">Property set:</span></span>  <br/> |<span data-ttu-id="7e792-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="7e792-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="7e792-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="7e792-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7e792-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="7e792-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="7e792-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7e792-112">Data type:</span></span>  <br/> |<span data-ttu-id="7e792-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7e792-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7e792-114">Область:</span><span class="sxs-lookup"><span data-stu-id="7e792-114">Area:</span></span>  <br/> |<span data-ttu-id="7e792-115">Task</span><span class="sxs-lookup"><span data-stu-id="7e792-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e792-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="7e792-116">Remarks</span></span>

<span data-ttu-id="7e792-117">Задача имеет нет даты, если это свойство соответствует удалить или переместить в 0x5AE980E0 (1,525,252,320).</span><span class="sxs-lookup"><span data-stu-id="7e792-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="7e792-118">Тем не менее Дата завершения является необязательным только в том случае, если нет даты начала указывается в свойстве **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7e792-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="7e792-119">Если дата завершения задачи, значение должно иметь компонент времени в полночь и необходимо также установить свойство **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7e792-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="7e792-120">Если **dispidTaskStartDate** имеет дату начала, значение свойства **dispidTaskDueDate** должно быть больше или равно значению **dispidTaskStartDate**.</span><span class="sxs-lookup"><span data-stu-id="7e792-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7e792-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7e792-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7e792-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7e792-122">Protocol specifications</span></span>

<span data-ttu-id="7e792-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e792-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e792-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7e792-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7e792-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e792-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e792-126">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="7e792-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="7e792-127">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e792-127">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e792-128">Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.</span><span class="sxs-lookup"><span data-stu-id="7e792-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7e792-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7e792-129">Header files</span></span>

<span data-ttu-id="7e792-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7e792-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="7e792-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7e792-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e792-132">См. также</span><span class="sxs-lookup"><span data-stu-id="7e792-132">See also</span></span>



[<span data-ttu-id="7e792-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7e792-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7e792-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7e792-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7e792-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7e792-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7e792-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7e792-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

