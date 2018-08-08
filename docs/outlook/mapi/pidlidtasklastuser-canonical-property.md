---
title: Каноническое свойство PidLidTaskLastUser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastUser
api_type:
- COM
ms.assetid: 914c55e9-cb36-46a4-b5ee-382413fa25f9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6dc2bcf2003ee16fa4a6c66689b6af79653e2d04
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810596"
---
# <a name="pidlidtasklastuser-canonical-property"></a><span data-ttu-id="d6747-103">Каноническое свойство PidLidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="d6747-103">PidLidTaskLastUser Canonical Property</span></span>

  
  
<span data-ttu-id="d6747-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d6747-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d6747-105">Имя последнего пользователя, который был владелец задачи.</span><span class="sxs-lookup"><span data-stu-id="d6747-105">Names the most recent user who was the task owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d6747-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d6747-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6747-107">dispidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="d6747-107">dispidTaskLastUser</span></span>  <br/> |
|<span data-ttu-id="d6747-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d6747-108">Property set:</span></span>  <br/> |<span data-ttu-id="d6747-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="d6747-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="d6747-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="d6747-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d6747-111">0x00008122</span><span class="sxs-lookup"><span data-stu-id="d6747-111">0x00008122</span></span>  <br/> |
|<span data-ttu-id="d6747-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d6747-112">Data type:</span></span>  <br/> |<span data-ttu-id="d6747-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d6747-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d6747-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d6747-114">Area:</span></span>  <br/> |<span data-ttu-id="d6747-115">Task</span><span class="sxs-lookup"><span data-stu-id="d6747-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6747-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="d6747-116">Remarks</span></span>

<span data-ttu-id="d6747-117">Перед клиента отправляет запрос задачи, это свойство присваивается имя назначено задач.</span><span class="sxs-lookup"><span data-stu-id="d6747-117">Before a client sends a task request, it sets this property to the name of the task assigner.</span></span> <span data-ttu-id="d6747-118">Перед клиента отправляет Принятие задачи, это свойство присваивается имя исполнителя задачи.</span><span class="sxs-lookup"><span data-stu-id="d6747-118">Before a client sends a task acceptance, it sets this property to the name of the task assignee.</span></span> <span data-ttu-id="d6747-119">Перед клиента отправляет Отклонение задачи, это свойство присваивается имя назначено задач.</span><span class="sxs-lookup"><span data-stu-id="d6747-119">Before a client sends a task rejection, it sets this property to the name of the task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d6747-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d6747-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6747-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d6747-121">Protocol specifications</span></span>

<span data-ttu-id="d6747-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6747-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6747-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d6747-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d6747-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6747-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6747-125">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="d6747-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6747-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d6747-126">Header files</span></span>

<span data-ttu-id="d6747-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6747-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6747-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d6747-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6747-129">См. также</span><span class="sxs-lookup"><span data-stu-id="d6747-129">See also</span></span>



[<span data-ttu-id="d6747-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d6747-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6747-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d6747-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6747-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d6747-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6747-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d6747-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

