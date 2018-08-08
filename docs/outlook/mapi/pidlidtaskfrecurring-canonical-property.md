---
title: Каноническое свойство PidLidTaskFRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFRecurring
api_type:
- COM
ms.assetid: 47c9ccbb-161c-4829-8ffb-201f3b54cd45
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eb97d278640b4cdd2b14152bf4745f883fe2edba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810581"
---
# <a name="pidlidtaskfrecurring-canonical-property"></a><span data-ttu-id="d4d9b-103">Каноническое свойство PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="d4d9b-103">PidLidTaskFRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="d4d9b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4d9b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4d9b-105">Указывает, является ли задача включает в себя шаблон повторения.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-105">Indicates whether the task includes a recurrence pattern.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d4d9b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d4d9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4d9b-107">dispidTaskFRecur</span><span class="sxs-lookup"><span data-stu-id="d4d9b-107">dispidTaskFRecur</span></span>  <br/> |
|<span data-ttu-id="d4d9b-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d4d9b-108">Property set:</span></span>  <br/> |<span data-ttu-id="d4d9b-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="d4d9b-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="d4d9b-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="d4d9b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d4d9b-111">0x00008126</span><span class="sxs-lookup"><span data-stu-id="d4d9b-111">0x00008126</span></span>  <br/> |
|<span data-ttu-id="d4d9b-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d4d9b-112">Data type:</span></span>  <br/> |<span data-ttu-id="d4d9b-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d4d9b-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d4d9b-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d4d9b-114">Area:</span></span>  <br/> |<span data-ttu-id="d4d9b-115">Task</span><span class="sxs-lookup"><span data-stu-id="d4d9b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4d9b-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="d4d9b-116">Remarks</span></span>

<span data-ttu-id="d4d9b-117">Если оставить это свойство определено, предполагается значение по умолчанию FALSE.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-117">If this property is left unset, a default value of FALSE is assumed.</span></span> <span data-ttu-id="d4d9b-118">Если он имеет значение TRUE, **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)), а также необходимо задать свойства **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) как указано в [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d4d9b-118">If it is set to TRUE, the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) and **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) properties must also be set as specified in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d4d9b-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d4d9b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4d9b-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d4d9b-120">Protocol specifications</span></span>

<span data-ttu-id="d4d9b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4d9b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4d9b-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d4d9b-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4d9b-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4d9b-124">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4d9b-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d4d9b-125">Header files</span></span>

<span data-ttu-id="d4d9b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4d9b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4d9b-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4d9b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d4d9b-128">See also</span></span>



[<span data-ttu-id="d4d9b-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d4d9b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4d9b-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d4d9b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4d9b-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d4d9b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4d9b-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d4d9b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

