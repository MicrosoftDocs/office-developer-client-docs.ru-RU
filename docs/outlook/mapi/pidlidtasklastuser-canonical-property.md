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
ms.openlocfilehash: 76311a76001b122bdfd984b9dedc37c2ff878fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360447"
---
# <a name="pidlidtasklastuser-canonical-property"></a><span data-ttu-id="6834b-103">Каноническое свойство PidLidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="6834b-103">PidLidTaskLastUser Canonical Property</span></span>

  
  
<span data-ttu-id="6834b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6834b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6834b-105">Имя последнего пользователя, который был владельцем задачи.</span><span class="sxs-lookup"><span data-stu-id="6834b-105">Names the most recent user who was the task owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6834b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6834b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6834b-107">dispidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="6834b-107">dispidTaskLastUser</span></span>  <br/> |
|<span data-ttu-id="6834b-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="6834b-108">Property set:</span></span>  <br/> |<span data-ttu-id="6834b-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="6834b-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="6834b-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="6834b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6834b-111">0x00008122</span><span class="sxs-lookup"><span data-stu-id="6834b-111">0x00008122</span></span>  <br/> |
|<span data-ttu-id="6834b-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6834b-112">Data type:</span></span>  <br/> |<span data-ttu-id="6834b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6834b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6834b-114">Область:</span><span class="sxs-lookup"><span data-stu-id="6834b-114">Area:</span></span>  <br/> |<span data-ttu-id="6834b-115">Task</span><span class="sxs-lookup"><span data-stu-id="6834b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6834b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="6834b-116">Remarks</span></span>

<span data-ttu-id="6834b-117">Перед отправкой запроса задачи клиент задает для этого свойства имя назначения задачи.</span><span class="sxs-lookup"><span data-stu-id="6834b-117">Before a client sends a task request, it sets this property to the name of the task assigner.</span></span> <span data-ttu-id="6834b-118">Перед отправкой приемки задачи клиент присваивает этому свойству имя его.</span><span class="sxs-lookup"><span data-stu-id="6834b-118">Before a client sends a task acceptance, it sets this property to the name of the task assignee.</span></span> <span data-ttu-id="6834b-119">Прежде чем клиент отправит отклонение задачи, он присваивает этому свойству имя назначения задачи.</span><span class="sxs-lookup"><span data-stu-id="6834b-119">Before a client sends a task rejection, it sets this property to the name of the task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6834b-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6834b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6834b-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6834b-121">Protocol specifications</span></span>

<span data-ttu-id="6834b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6834b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6834b-123">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="6834b-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6834b-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6834b-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6834b-125">Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.</span><span class="sxs-lookup"><span data-stu-id="6834b-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6834b-126">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="6834b-126">Header files</span></span>

<span data-ttu-id="6834b-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6834b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6834b-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6834b-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6834b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="6834b-129">See also</span></span>



[<span data-ttu-id="6834b-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6834b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6834b-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6834b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6834b-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6834b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6834b-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6834b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

