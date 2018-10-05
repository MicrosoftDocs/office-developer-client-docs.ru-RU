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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385076"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="a5798-103">Каноническое свойство PidLidTaskAssigners</span><span class="sxs-lookup"><span data-stu-id="a5798-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="a5798-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5798-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5798-105">Содержит стек записей, которые представляют assigners задач.</span><span class="sxs-lookup"><span data-stu-id="a5798-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="a5798-106">Самые последние назначено задач отображается в верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="a5798-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5798-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a5798-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5798-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="a5798-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="a5798-109">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="a5798-109">Property set:</span></span>  <br/> |<span data-ttu-id="a5798-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="a5798-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="a5798-111">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="a5798-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a5798-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="a5798-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="a5798-113">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a5798-113">Data type:</span></span>  <br/> |<span data-ttu-id="a5798-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a5798-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a5798-115">Область:</span><span class="sxs-lookup"><span data-stu-id="a5798-115">Area:</span></span>  <br/> |<span data-ttu-id="a5798-116">Task</span><span class="sxs-lookup"><span data-stu-id="a5798-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5798-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="a5798-117">Remarks</span></span>

<span data-ttu-id="a5798-118">Если клиент получает запроса на задачу, добавляет с этим свойством, структура которого определяется в [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), запись, который представляет задачу отправителя.</span><span class="sxs-lookup"><span data-stu-id="a5798-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="a5798-119">Когда клиент получает Отклонение задачи, клиента удаляется последняя запись назначено задач из этого свойства.</span><span class="sxs-lookup"><span data-stu-id="a5798-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="a5798-120">Когда клиент отправляет ответ задач, клиент отправляет его последнего назначено задачи, перечисленные в значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="a5798-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a5798-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a5798-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5798-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a5798-122">Protocol specifications</span></span>

<span data-ttu-id="a5798-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5798-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5798-124">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a5798-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5798-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5798-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5798-126">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач</span><span class="sxs-lookup"><span data-stu-id="a5798-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="a5798-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a5798-127">Header files</span></span>

<span data-ttu-id="a5798-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5798-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5798-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a5798-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5798-130">См. также</span><span class="sxs-lookup"><span data-stu-id="a5798-130">See also</span></span>



[<span data-ttu-id="a5798-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a5798-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5798-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a5798-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5798-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a5798-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5798-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a5798-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

