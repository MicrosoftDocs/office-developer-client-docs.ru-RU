---
title: Каноническое свойство PidLidTaskLastDelegate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastDelegate
api_type:
- COM
ms.assetid: 5eb8c1ce-063f-4273-acba-e6f9c994e7d3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f33443531e5affd358669225044b2d63c909aff1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575058"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="4fc63-103">Каноническое свойство PidLidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="4fc63-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="4fc63-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fc63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4fc63-105">Имя пользователя, который последним назначенных или была назначена задача.</span><span class="sxs-lookup"><span data-stu-id="4fc63-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4fc63-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4fc63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4fc63-107">dispidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="4fc63-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="4fc63-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="4fc63-108">Property set:</span></span>  <br/> |<span data-ttu-id="4fc63-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="4fc63-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="4fc63-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="4fc63-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4fc63-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="4fc63-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="4fc63-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4fc63-112">Data type:</span></span>  <br/> |<span data-ttu-id="4fc63-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4fc63-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4fc63-114">Область:</span><span class="sxs-lookup"><span data-stu-id="4fc63-114">Area:</span></span>  <br/> |<span data-ttu-id="4fc63-115">Task</span><span class="sxs-lookup"><span data-stu-id="4fc63-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fc63-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="4fc63-116">Remarks</span></span>

<span data-ttu-id="4fc63-117">Перед отправкой запроса на задачу, клиент этому свойству присваивается имя назначено задач.</span><span class="sxs-lookup"><span data-stu-id="4fc63-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="4fc63-118">До отправки ответа задач, клиент этому свойству присваивается имя исполнителя задачи.</span><span class="sxs-lookup"><span data-stu-id="4fc63-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4fc63-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4fc63-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4fc63-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4fc63-120">Protocol specifications</span></span>

<span data-ttu-id="4fc63-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4fc63-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4fc63-122">Содержит определение набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4fc63-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4fc63-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4fc63-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4fc63-124">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="4fc63-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4fc63-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4fc63-125">Header files</span></span>

<span data-ttu-id="4fc63-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4fc63-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4fc63-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4fc63-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4fc63-128">См. также</span><span class="sxs-lookup"><span data-stu-id="4fc63-128">See also</span></span>



[<span data-ttu-id="4fc63-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4fc63-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4fc63-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4fc63-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4fc63-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4fc63-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4fc63-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4fc63-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

