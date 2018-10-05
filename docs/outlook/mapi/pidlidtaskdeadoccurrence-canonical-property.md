---
title: Каноническое свойство PidLidTaskDeadOccurrence
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDeadOccurrence
api_type:
- COM
ms.assetid: e78287ff-f8cc-45ea-8da8-e7a7359e651c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0b740368aae43549e81cf3f4f6de40526c505b6b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401518"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a><span data-ttu-id="02378-103">Каноническое свойство PidLidTaskDeadOccurrence</span><span class="sxs-lookup"><span data-stu-id="02378-103">PidLidTaskDeadOccurrence Canonical Property</span></span>

  
  
<span data-ttu-id="02378-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02378-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02378-105">Указывает, должен быть создан новый вхождений.</span><span class="sxs-lookup"><span data-stu-id="02378-105">Indicates whether new occurrences must be generated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02378-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="02378-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02378-107">dispidTaskDeadOccur</span><span class="sxs-lookup"><span data-stu-id="02378-107">dispidTaskDeadOccur</span></span>  <br/> |
|<span data-ttu-id="02378-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="02378-108">Property set:</span></span>  <br/> |<span data-ttu-id="02378-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="02378-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="02378-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="02378-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="02378-111">0x00008109</span><span class="sxs-lookup"><span data-stu-id="02378-111">0x00008109</span></span>  <br/> |
|<span data-ttu-id="02378-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="02378-112">Data type:</span></span>  <br/> |<span data-ttu-id="02378-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="02378-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="02378-114">Область:</span><span class="sxs-lookup"><span data-stu-id="02378-114">Area:</span></span>  <br/> |<span data-ttu-id="02378-115">Task</span><span class="sxs-lookup"><span data-stu-id="02378-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02378-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="02378-116">Remarks</span></span>

<span data-ttu-id="02378-117">Шаблон повторения больше не фактически при его последнюю строку в прошлом или создала его заданное количество экземпляров.</span><span class="sxs-lookup"><span data-stu-id="02378-117">A recurrence pattern is no longer in effect when its final instance is in the past or its specified number of instances has been generated.</span></span> <span data-ttu-id="02378-118">Клиента этому свойству значение FALSE для новой задачи или значение TRUE, если он создает последний экземпляр повторяющейся задачи.</span><span class="sxs-lookup"><span data-stu-id="02378-118">The client sets this property to FALSE for a new task or to TRUE when it generates the last instance of a recurring task.</span></span> <span data-ttu-id="02378-119">При копировании задач для создания нового экземпляра, это свойство имеет значение TRUE в копии, которая является завершенных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="02378-119">When you copy a task to generate a new instance, this property is set to TRUE on the copy, which is the completed instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="02378-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="02378-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="02378-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="02378-121">Protocol specifications</span></span>

<span data-ttu-id="02378-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02378-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02378-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="02378-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="02378-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02378-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02378-125">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="02378-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="02378-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="02378-126">Header files</span></span>

<span data-ttu-id="02378-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02378-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="02378-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="02378-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02378-129">См. также</span><span class="sxs-lookup"><span data-stu-id="02378-129">See also</span></span>



[<span data-ttu-id="02378-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="02378-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02378-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="02378-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02378-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="02378-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02378-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="02378-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

