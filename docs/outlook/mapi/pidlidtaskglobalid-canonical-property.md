---
title: Каноническое свойство PidLidTaskGlobalId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskGlobalId
api_type:
- COM
ms.assetid: 369d8c78-3cf6-4a55-ba14-9da0377d6ccf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 33f3b8e7d3d0e0d4461c947aa8e9b3ee66373d2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810580"
---
# <a name="pidlidtaskglobalid-canonical-property"></a><span data-ttu-id="cbd83-103">Каноническое свойство PidLidTaskGlobalId</span><span class="sxs-lookup"><span data-stu-id="cbd83-103">PidLidTaskGlobalId Canonical Property</span></span>

  
  
<span data-ttu-id="cbd83-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cbd83-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cbd83-105">Поиск существующей задачи, с помощью GUID, после получения ответа задач или обновление задачи.</span><span class="sxs-lookup"><span data-stu-id="cbd83-105">Locates an existing task, by using a GUID, upon receipt of a task response or task update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cbd83-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cbd83-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cbd83-107">dispidTaskGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="cbd83-107">dispidTaskGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="cbd83-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="cbd83-108">Property set:</span></span>  <br/> |<span data-ttu-id="cbd83-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="cbd83-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="cbd83-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="cbd83-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cbd83-111">0x00008519</span><span class="sxs-lookup"><span data-stu-id="cbd83-111">0x00008519</span></span>  <br/> |
|<span data-ttu-id="cbd83-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cbd83-112">Data type:</span></span>  <br/> |<span data-ttu-id="cbd83-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cbd83-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cbd83-114">Область:</span><span class="sxs-lookup"><span data-stu-id="cbd83-114">Area:</span></span>  <br/> |<span data-ttu-id="cbd83-115">Task</span><span class="sxs-lookup"><span data-stu-id="cbd83-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbd83-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="cbd83-116">Remarks</span></span>

<span data-ttu-id="cbd83-117">Оставить это свойство определено для неназначенных задач.</span><span class="sxs-lookup"><span data-stu-id="cbd83-117">This property is left unset for unassigned tasks.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cbd83-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cbd83-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cbd83-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cbd83-119">Protocol specifications</span></span>

<span data-ttu-id="cbd83-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbd83-120">[[MS-OXPROPS] ](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbd83-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cbd83-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cbd83-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbd83-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbd83-123">Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.</span><span class="sxs-lookup"><span data-stu-id="cbd83-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cbd83-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="cbd83-124">Header files</span></span>

<span data-ttu-id="cbd83-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cbd83-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="cbd83-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cbd83-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cbd83-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cbd83-127">See also</span></span>



[<span data-ttu-id="cbd83-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cbd83-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cbd83-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cbd83-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cbd83-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cbd83-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cbd83-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cbd83-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

