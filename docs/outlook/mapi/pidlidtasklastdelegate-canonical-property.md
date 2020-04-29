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
ms.openlocfilehash: ddf4b81ed35f500dad0029ea6375e9a75a996186
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355673"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="49eb6-103">Каноническое свойство PidLidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="49eb6-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="49eb6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49eb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="49eb6-105">Имя пользователя, который последним назначен задаче или назначен ему.</span><span class="sxs-lookup"><span data-stu-id="49eb6-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49eb6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="49eb6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="49eb6-107">диспидтаскластделегате</span><span class="sxs-lookup"><span data-stu-id="49eb6-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="49eb6-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="49eb6-108">Property set:</span></span>  <br/> |<span data-ttu-id="49eb6-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="49eb6-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="49eb6-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="49eb6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="49eb6-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="49eb6-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="49eb6-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="49eb6-112">Data type:</span></span>  <br/> |<span data-ttu-id="49eb6-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="49eb6-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="49eb6-114">Область:</span><span class="sxs-lookup"><span data-stu-id="49eb6-114">Area:</span></span>  <br/> |<span data-ttu-id="49eb6-115">Задача</span><span class="sxs-lookup"><span data-stu-id="49eb6-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49eb6-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="49eb6-116">Remarks</span></span>

<span data-ttu-id="49eb6-117">Перед отправкой запроса задачи клиент задает для этого свойства имя назначения задачи.</span><span class="sxs-lookup"><span data-stu-id="49eb6-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="49eb6-118">Перед отправкой ответа задачи клиент задает для этого свойства имя уполномоченного задачи.</span><span class="sxs-lookup"><span data-stu-id="49eb6-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="49eb6-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="49eb6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="49eb6-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="49eb6-120">Protocol specifications</span></span>

<span data-ttu-id="49eb6-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49eb6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49eb6-122">Предоставляет определение набора свойств и ссылки на соответствующие спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="49eb6-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="49eb6-123">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49eb6-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49eb6-124">Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="49eb6-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="49eb6-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="49eb6-125">Header files</span></span>

<span data-ttu-id="49eb6-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="49eb6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="49eb6-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="49eb6-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49eb6-128">См. также</span><span class="sxs-lookup"><span data-stu-id="49eb6-128">See also</span></span>



[<span data-ttu-id="49eb6-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="49eb6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49eb6-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="49eb6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49eb6-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="49eb6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49eb6-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="49eb6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

