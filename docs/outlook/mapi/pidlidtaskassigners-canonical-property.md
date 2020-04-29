---
title: Каноническое свойство PidLidTaskAssigners
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 97a4915d5422f6c5463ed399835172725b83407f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303068"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="f1771-103">Каноническое свойство PidLidTaskAssigners</span><span class="sxs-lookup"><span data-stu-id="f1771-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="f1771-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1771-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1771-105">Содержит стек записей, представляющих назначенные задачи.</span><span class="sxs-lookup"><span data-stu-id="f1771-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="f1771-106">В верхней части стека появится самый последний назначенный вам планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="f1771-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1771-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f1771-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1771-108">диспидтаскмиделегаторс</span><span class="sxs-lookup"><span data-stu-id="f1771-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="f1771-109">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="f1771-109">Property set:</span></span>  <br/> |<span data-ttu-id="f1771-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="f1771-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="f1771-111">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="f1771-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f1771-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="f1771-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="f1771-113">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f1771-113">Data type:</span></span>  <br/> |<span data-ttu-id="f1771-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f1771-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f1771-115">Область:</span><span class="sxs-lookup"><span data-stu-id="f1771-115">Area:</span></span>  <br/> |<span data-ttu-id="f1771-116">Задача</span><span class="sxs-lookup"><span data-stu-id="f1771-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1771-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="f1771-117">Remarks</span></span>

<span data-ttu-id="f1771-118">Когда клиент получает запрос задачи, он добавляется к этому свойству, какая структура определена в [[MS-оксотаск]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), запись, представляющая отправителя задачи.</span><span class="sxs-lookup"><span data-stu-id="f1771-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="f1771-119">Когда клиент получает отказ задачи, клиент удаляет из этого свойства последнюю запись о назначении задачи.</span><span class="sxs-lookup"><span data-stu-id="f1771-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="f1771-120">Когда клиент отправляет ответ задачи, клиент отправляет его последнему назначению задачи, указанному в значении этого свойства.</span><span class="sxs-lookup"><span data-stu-id="f1771-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f1771-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f1771-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f1771-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f1771-122">Protocol specifications</span></span>

<span data-ttu-id="f1771-123">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1771-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1771-124">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f1771-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f1771-125">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1771-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1771-126">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="f1771-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="f1771-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f1771-127">Header files</span></span>

<span data-ttu-id="f1771-128">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="f1771-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1771-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f1771-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1771-130">См. также</span><span class="sxs-lookup"><span data-stu-id="f1771-130">See also</span></span>



[<span data-ttu-id="f1771-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f1771-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1771-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="f1771-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1771-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f1771-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1771-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f1771-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

