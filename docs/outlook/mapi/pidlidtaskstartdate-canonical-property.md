---
title: Каноническое свойство PidLidTaskStartDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStartDate
api_type:
- COM
ms.assetid: fe87eb3d-21d1-45bb-b848-e141ce1be6a0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3bc475292e47a9ad8dd9565e17640ef95e7b3c76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316683"
---
# <a name="pidlidtaskstartdate-canonical-property"></a><span data-ttu-id="eb955-103">Каноническое свойство PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="eb955-103">PidLidTaskStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="eb955-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb955-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb955-105">Дата начала задачи пользователем.</span><span class="sxs-lookup"><span data-stu-id="eb955-105">The date when the user expects to begin the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb955-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="eb955-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb955-107">dispidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="eb955-107">dispidTaskStartDate</span></span>  <br/> |
|<span data-ttu-id="eb955-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="eb955-108">Property set:</span></span>  <br/> |<span data-ttu-id="eb955-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="eb955-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="eb955-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="eb955-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="eb955-111">0x00008104</span><span class="sxs-lookup"><span data-stu-id="eb955-111">0x00008104</span></span>  <br/> |
|<span data-ttu-id="eb955-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="eb955-112">Data type:</span></span>  <br/> |<span data-ttu-id="eb955-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="eb955-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="eb955-114">Область:</span><span class="sxs-lookup"><span data-stu-id="eb955-114">Area:</span></span>  <br/> |<span data-ttu-id="eb955-115">Task</span><span class="sxs-lookup"><span data-stu-id="eb955-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb955-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="eb955-116">Remarks</span></span>

<span data-ttu-id="eb955-117">Если значение этого свойства не заданной, задача не имеет даты начала.</span><span class="sxs-lookup"><span data-stu-id="eb955-117">If this property value is left unset, the task does not have a start date.</span></span> <span data-ttu-id="eb955-118">Значение "0x5AE980E0" (1 525 252 320) также означает, что задача не имеет даты начала.</span><span class="sxs-lookup"><span data-stu-id="eb955-118">A value of "0x5AE980E0" (1,525,252,320) also means that the task does not have a start date.</span></span> <span data-ttu-id="eb955-119">Если задача имеет даты начала, значение должно иметь компонент времени полуночи, а свойства **dispidTaskDueDate** ([PidLidTaskDueDate)](pidlidtaskduedate-canonical-property.md)и **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) также должны быть установлены.</span><span class="sxs-lookup"><span data-stu-id="eb955-119">If the task has a start date, the value must have a time component of midnight, and the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) and **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) properties must also be set.</span></span>
  
<span data-ttu-id="eb955-120">Это свойство совместно с спецификацией протокола информационного помеления и спецификацией протокола Task-Related, расположенной [в [MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="eb955-120">This property is shared by the Informational Flagging Protocol Specification and Task-Related Object Protocol Specification located in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eb955-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="eb955-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eb955-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="eb955-122">Protocol specifications</span></span>

<span data-ttu-id="eb955-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb955-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb955-124">Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="eb955-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eb955-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb955-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb955-126">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="eb955-126">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eb955-127">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="eb955-127">Header files</span></span>

<span data-ttu-id="eb955-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb955-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb955-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="eb955-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb955-130">См. также</span><span class="sxs-lookup"><span data-stu-id="eb955-130">See also</span></span>



[<span data-ttu-id="eb955-131">������������ �������� PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="eb955-131">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
  
[<span data-ttu-id="eb955-132">������������ �������� PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="eb955-132">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)


[<span data-ttu-id="eb955-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eb955-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb955-134">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eb955-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb955-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="eb955-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb955-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="eb955-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

