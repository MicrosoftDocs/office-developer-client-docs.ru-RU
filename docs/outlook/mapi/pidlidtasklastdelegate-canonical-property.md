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
ms.openlocfilehash: 8e1a343486e78daae45ca7315ba4d29d44b688bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810591"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="0a17a-103">Каноническое свойство PidLidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="0a17a-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="0a17a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0a17a-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="0a17a-105">Имя пользователя, который последним назначенных или была назначена задача.</span><span class="sxs-lookup"><span data-stu-id="0a17a-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a17a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0a17a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a17a-107">dispidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="0a17a-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="0a17a-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="0a17a-108">Property set:</span></span>  <br/> |<span data-ttu-id="0a17a-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0a17a-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0a17a-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="0a17a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0a17a-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="0a17a-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="0a17a-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0a17a-112">Data type:</span></span>  <br/> |<span data-ttu-id="0a17a-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0a17a-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0a17a-114">Область:</span><span class="sxs-lookup"><span data-stu-id="0a17a-114">Area:</span></span>  <br/> |<span data-ttu-id="0a17a-115">Task</span><span class="sxs-lookup"><span data-stu-id="0a17a-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a17a-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="0a17a-116">Remarks</span></span>

<span data-ttu-id="0a17a-117">Перед отправкой запроса на задачу, клиент этому свойству присваивается имя назначено задач.</span><span class="sxs-lookup"><span data-stu-id="0a17a-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="0a17a-118">До отправки ответа задач, клиент этому свойству присваивается имя исполнителя задачи.</span><span class="sxs-lookup"><span data-stu-id="0a17a-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0a17a-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0a17a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0a17a-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0a17a-120">Protocol specifications</span></span>

<span data-ttu-id="0a17a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a17a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a17a-122">Содержит определение набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0a17a-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0a17a-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a17a-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a17a-124">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="0a17a-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0a17a-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0a17a-125">Header files</span></span>

<span data-ttu-id="0a17a-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a17a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a17a-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0a17a-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a17a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0a17a-128">See also</span></span>



[<span data-ttu-id="0a17a-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0a17a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a17a-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0a17a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a17a-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0a17a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a17a-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0a17a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

