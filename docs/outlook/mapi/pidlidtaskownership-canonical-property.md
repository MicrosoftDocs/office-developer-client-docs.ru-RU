---
title: Каноническое свойство PidLidTaskOwnership
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOwnership
api_type:
- COM
ms.assetid: 805dcb6c-f405-4c4d-8bca-af4bd9cd44fa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 45fcba3f18aeb9092b71e28a6b68e42ad1abe77d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332111"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="b1292-103">Каноническое свойство PidLidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="b1292-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="b1292-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1292-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1292-105">Указывает роль текущего пользователя относительно задачи.</span><span class="sxs-lookup"><span data-stu-id="b1292-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1292-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b1292-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1292-107">dispidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="b1292-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="b1292-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b1292-108">Property set:</span></span>  <br/> |<span data-ttu-id="b1292-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b1292-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b1292-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b1292-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b1292-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="b1292-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="b1292-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b1292-112">Data type:</span></span>  <br/> |<span data-ttu-id="b1292-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b1292-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b1292-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b1292-114">Area:</span></span>  <br/> |<span data-ttu-id="b1292-115">Задача</span><span class="sxs-lookup"><span data-stu-id="b1292-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1292-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b1292-116">Remarks</span></span>

<span data-ttu-id="b1292-117">Это свойство должно быть одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b1292-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="b1292-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b1292-118">**Value**</span></span>|<span data-ttu-id="b1292-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b1292-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1292-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1292-120">0x00000000</span></span>  <br/> |<span data-ttu-id="b1292-121">Задача не назначена.</span><span class="sxs-lookup"><span data-stu-id="b1292-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="b1292-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b1292-122">0x00000001</span></span>  <br/> |<span data-ttu-id="b1292-123">Задача — это копия задачи, которую назначит назначитель задачи.</span><span class="sxs-lookup"><span data-stu-id="b1292-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="b1292-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b1292-124">0x00000002</span></span>  <br/> |<span data-ttu-id="b1292-125">Задача — это копия задачи, которую назначает назначить.</span><span class="sxs-lookup"><span data-stu-id="b1292-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b1292-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b1292-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1292-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b1292-127">Protocol specifications</span></span>

<span data-ttu-id="b1292-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1292-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1292-129">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="b1292-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b1292-130">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1292-130">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1292-131">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="b1292-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b1292-132">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="b1292-132">Header files</span></span>

<span data-ttu-id="b1292-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1292-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1292-134">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b1292-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1292-135">См. также</span><span class="sxs-lookup"><span data-stu-id="b1292-135">See also</span></span>



[<span data-ttu-id="b1292-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b1292-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1292-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b1292-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1292-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b1292-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1292-139">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="b1292-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

