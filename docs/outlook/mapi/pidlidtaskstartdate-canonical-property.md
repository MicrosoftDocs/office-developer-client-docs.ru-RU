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
ms.openlocfilehash: 486b1f913e7c3c76886232c48fa842e25e1f7905
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810608"
---
# <a name="pidlidtaskstartdate-canonical-property"></a><span data-ttu-id="0199c-103">Каноническое свойство PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="0199c-103">PidLidTaskStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="0199c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0199c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0199c-105">Дата, когда пользователь ожидает начала выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="0199c-105">The date when the user expects to begin the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0199c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0199c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0199c-107">dispidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="0199c-107">dispidTaskStartDate</span></span>  <br/> |
|<span data-ttu-id="0199c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="0199c-108">Property set:</span></span>  <br/> |<span data-ttu-id="0199c-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0199c-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0199c-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="0199c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0199c-111">0x00008104</span><span class="sxs-lookup"><span data-stu-id="0199c-111">0x00008104</span></span>  <br/> |
|<span data-ttu-id="0199c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0199c-112">Data type:</span></span>  <br/> |<span data-ttu-id="0199c-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="0199c-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="0199c-114">Область:</span><span class="sxs-lookup"><span data-stu-id="0199c-114">Area:</span></span>  <br/> |<span data-ttu-id="0199c-115">Task</span><span class="sxs-lookup"><span data-stu-id="0199c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0199c-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="0199c-116">Remarks</span></span>

<span data-ttu-id="0199c-117">Если значение этого свойства не определено, задача не имеет дату начала.</span><span class="sxs-lookup"><span data-stu-id="0199c-117">If this property value is left unset, the task does not have a start date.</span></span> <span data-ttu-id="0199c-118">Значение «0x5AE980E0» (1,525,252,320) также означает, что задачу не имеет дату начала.</span><span class="sxs-lookup"><span data-stu-id="0199c-118">A value of "0x5AE980E0" (1,525,252,320) also means that the task does not have a start date.</span></span> <span data-ttu-id="0199c-119">Если дата начала задачи, значение должно иметь компонент времени полночь, а также необходимо задать свойства **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) и **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0199c-119">If the task has a start date, the value must have a time component of midnight, and the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) and **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) properties must also be set.</span></span>
  
<span data-ttu-id="0199c-120">Это свойство используется совместно спецификацией информационные Пометка протокола и спецификация протокола Task-Related объект находится в [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0199c-120">This property is shared by the Informational Flagging Protocol Specification and Task-Related Object Protocol Specification located in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0199c-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0199c-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0199c-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0199c-122">Protocol specifications</span></span>

<span data-ttu-id="0199c-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0199c-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0199c-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0199c-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0199c-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0199c-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0199c-126">Задает свойства и операции, допустимые на контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="0199c-126">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0199c-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0199c-127">Header files</span></span>

<span data-ttu-id="0199c-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0199c-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0199c-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0199c-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0199c-130">См. также</span><span class="sxs-lookup"><span data-stu-id="0199c-130">See also</span></span>



[<span data-ttu-id="0199c-131">������������ �������� PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="0199c-131">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
  
[<span data-ttu-id="0199c-132">������������ �������� PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="0199c-132">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)


[<span data-ttu-id="0199c-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0199c-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0199c-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0199c-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0199c-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0199c-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0199c-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0199c-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

