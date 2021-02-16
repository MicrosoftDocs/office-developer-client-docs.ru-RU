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
ms.openlocfilehash: aec9dd328e802e185c870d3ecd94cbd1d10ac67d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303054"
---
# <a name="pidlidtaskfrecurring-canonical-property"></a><span data-ttu-id="3e60b-103">Каноническое свойство PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="3e60b-103">PidLidTaskFRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="3e60b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e60b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e60b-105">Указывает, включает ли задача шаблон повторения.</span><span class="sxs-lookup"><span data-stu-id="3e60b-105">Indicates whether the task includes a recurrence pattern.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3e60b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3e60b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3e60b-107">dispidTaskFRecur</span><span class="sxs-lookup"><span data-stu-id="3e60b-107">dispidTaskFRecur</span></span>  <br/> |
|<span data-ttu-id="3e60b-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="3e60b-108">Property set:</span></span>  <br/> |<span data-ttu-id="3e60b-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="3e60b-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="3e60b-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="3e60b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3e60b-111">0x00008126</span><span class="sxs-lookup"><span data-stu-id="3e60b-111">0x00008126</span></span>  <br/> |
|<span data-ttu-id="3e60b-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3e60b-112">Data type:</span></span>  <br/> |<span data-ttu-id="3e60b-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3e60b-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="3e60b-114">Область:</span><span class="sxs-lookup"><span data-stu-id="3e60b-114">Area:</span></span>  <br/> |<span data-ttu-id="3e60b-115">Task</span><span class="sxs-lookup"><span data-stu-id="3e60b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e60b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="3e60b-116">Remarks</span></span>

<span data-ttu-id="3e60b-117">Если это свойство не заданной, по умолчанию предполагается значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="3e60b-117">If this property is left unset, a default value of FALSE is assumed.</span></span> <span data-ttu-id="3e60b-118">Если задано true, свойства **dispidTaskRecur** ([PidLidTaskRecurrence)](pidlidtaskrecurrence-canonical-property.md)и **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence)](pidlidtaskdeadoccurrence-canonical-property.md)также должны быть заданы в [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3e60b-118">If it is set to TRUE, the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) and **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) properties must also be set as specified in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3e60b-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3e60b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3e60b-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3e60b-120">Protocol specifications</span></span>

<span data-ttu-id="3e60b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e60b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e60b-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="3e60b-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3e60b-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e60b-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e60b-124">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="3e60b-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3e60b-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="3e60b-125">Header files</span></span>

<span data-ttu-id="3e60b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3e60b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="3e60b-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3e60b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e60b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="3e60b-128">See also</span></span>



[<span data-ttu-id="3e60b-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3e60b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3e60b-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3e60b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3e60b-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3e60b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3e60b-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3e60b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

