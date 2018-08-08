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
ms.openlocfilehash: 17f3ac0c5cd6005329212d0dcb458b37bb75f41d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810619"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="eb55c-103">Каноническое свойство PidLidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="eb55c-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="eb55c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb55c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb55c-105">Указывает роли текущего пользователя относительно задачи.</span><span class="sxs-lookup"><span data-stu-id="eb55c-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb55c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="eb55c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb55c-107">dispidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="eb55c-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="eb55c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="eb55c-108">Property set:</span></span>  <br/> |<span data-ttu-id="eb55c-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="eb55c-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="eb55c-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="eb55c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="eb55c-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="eb55c-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="eb55c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="eb55c-112">Data type:</span></span>  <br/> |<span data-ttu-id="eb55c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="eb55c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="eb55c-114">Область:</span><span class="sxs-lookup"><span data-stu-id="eb55c-114">Area:</span></span>  <br/> |<span data-ttu-id="eb55c-115">Task</span><span class="sxs-lookup"><span data-stu-id="eb55c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb55c-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="eb55c-116">Remarks</span></span>

<span data-ttu-id="eb55c-117">Это свойство должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="eb55c-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="eb55c-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="eb55c-118">**Value**</span></span>|<span data-ttu-id="eb55c-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eb55c-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb55c-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb55c-120">0x00000000</span></span>  <br/> |<span data-ttu-id="eb55c-121">Не назначена задача.</span><span class="sxs-lookup"><span data-stu-id="eb55c-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="eb55c-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="eb55c-122">0x00000001</span></span>  <br/> |<span data-ttu-id="eb55c-123">Задача — назначено задач копия задачи.</span><span class="sxs-lookup"><span data-stu-id="eb55c-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="eb55c-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="eb55c-124">0x00000002</span></span>  <br/> |<span data-ttu-id="eb55c-125">Является задача назначена задача копия задачи.</span><span class="sxs-lookup"><span data-stu-id="eb55c-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="eb55c-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="eb55c-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eb55c-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="eb55c-127">Protocol specifications</span></span>

<span data-ttu-id="eb55c-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb55c-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb55c-129">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="eb55c-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eb55c-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb55c-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb55c-131">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="eb55c-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eb55c-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="eb55c-132">Header files</span></span>

<span data-ttu-id="eb55c-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb55c-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb55c-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="eb55c-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb55c-135">См. также</span><span class="sxs-lookup"><span data-stu-id="eb55c-135">See also</span></span>



[<span data-ttu-id="eb55c-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eb55c-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb55c-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eb55c-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb55c-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="eb55c-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb55c-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="eb55c-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

